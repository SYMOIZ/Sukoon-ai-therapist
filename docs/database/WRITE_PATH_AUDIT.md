# WRITE PATH AUDIT REPORT

Generated on: 2026-06-10T09:17:31.584Z
Tested via: Local API Automated Integration suite + SQLite DB persistence inspector.

## 1. Complete Write Endpoint Survey

The following grid represents the precise audit results from direct execution of all write-path endpoints (including HTTP POST/DELETE triggers) inside the Sukoon AI stack.

| Endpoint | DB Table | Transaction Mechanism | Pass / Fail | Root Cause | Source File | Function Name |
|---|---|---|---|---|---|---|
| `/api/auth/signup` | `users` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/auth.py` | `signup` |
| `/api/auth/signin_anonymous` | `users` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/auth.py` | `signin_anonymous` |
| `/api/support/tickets/create` | `support_tickets` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/support.py` | `create_ticket` |
| `/api/db/insert` | `risk_alerts` | query_db(is_write=True) -- SQLAlchemy custom raw transactions on Connection | **FAIL** | `This connection has already initialized a SQLAlchemy Transaction() object via begin() or autobegin; can't call begin() here unless rollback() or commit() is called first.` | `main.py` | `db_insert` |
| `/api/db/update` | `users` | query_db(is_write=True) -- SQLAlchemy custom raw transactions on Connection | **FAIL** | `This connection has already initialized a SQLAlchemy Transaction() object via begin() or autobegin; can't call begin() here unless rollback() or commit() is called first.` | `main.py` | `db_update` |
| `/api/db/delete` | `risk_alerts` | query_db(is_write=True) -- SQLAlchemy custom raw transactions on Connection | **FAIL** | `This connection has already initialized a SQLAlchemy Transaction() object via begin() or autobegin; can't call begin() here unless rollback() or commit() is called first.` | `main.py` | `db_delete` |
| `/api/bookings/create` | `session_bookings` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/booking.py` | `create_booking` |
| `/api/bookings/update` | `session_bookings` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/booking.py` | `update_booking` |
| `/api/support/tickets/resolve` | `support_tickets` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/support.py` | `resolve_ticket` |
| `/api/journal` | `journal_entries` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/journal.py` | `create_journal` |
| `/api/journal/delete/{entryId}` | `journal_entries` | SQLAlchemy Session (db.commit()) -- ORM based | **PASS** | N/A | `backend/routers/journal.py` | `delete_journal` |

## 2. Inconsistency Clarification Case

### The Inconsistency Explained
During initial system verification:
- Direct backend calls to Create Support Ticket, Resolve Ticket, and SignUp **Succeeded**.
- Direct universal database proxy requests (such as `/api/db/insert`) **Failed**.

### Investigation Findings
The root of this behavioral discrepancy is the **bifurcated write architecture**:

1. **Path A: Native FastAPI Router Handlers**
   Services like auth, support tickets, and bookings have clean Python routes using high-level **SQLAlchemy ORM Sessions** (`get_db`). These handlers execute database mutations by calling `db.add()`, `db.commit()`, and `db.refresh()`. 
   These routes **bypass the custom raw SQLAlchemy connection `query_db` method query processor entirely**. Therefore, they operate flawlessly and persist data immediately to `sukoon.db`.

2. **Path B: Client Proxy Layer (Universal Database Proxy)**
   The actual Web UI in the browser compiles components and relies on `supabaseClient.ts`. This client interceptor translates standard query builder commands like `supabase.from('some_table').insert(values)` directly to general REST proxy requests targeting `/api/db/insert`, `/api/db/update`, or `/api/db/delete`.
   These write paths inside `main.py` parse payloads and feed them to `query_db(..., is_write=True)`.
   Under the hood:
   - `query_db` opens connections using `with engine.connect() as connection:`
   - It performs initial setups like PRAGMAs, which **implicitly initializes and begins** an implicit SQLAlchemy transaction under the hood (dual transaction autobegin on SQLite/PostgreSQL drivers).
   - It then manually fires `trans = connection.begin()`, triggering a dual transaction conflict exception.
   - This breaks **every single write action triggered in the visual browser application interface**, while standard standalone Python microservice routes continue working in test isolation.

## 3. Structural Alignment Fix Recommendation

To restore full portal functionality, the transaction layer inside `query_db` in `main.py` must be transitioned from SQLAlchemy-managed connections to transaction-managed contexts:

```python
# Deprecated approach (fails due to dual autobegin):
with engine.connect() as connection:
    trans = connection.begin()
    connection.execute(...)
    trans.commit()

# Recommended non-blocking pattern:
with engine.begin() as connection:
    if engine.name == "sqlite":
         connection.execute(text("PRAGMA foreign_keys = ON;"))
    result = connection.execute(text(translated_query), param_dict)
    # Automatically committed on successful block exit, rolled back on error!
```

---
Report compiled by custom SQL.js system persistence verify runner.
