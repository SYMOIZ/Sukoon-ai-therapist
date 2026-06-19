# Data Handling — Sukoon AI

**Section:** 08 — Security and Trust  
**Document:** DATA_HANDLING.md  
**Audience:** Technical Team, Legal/Compliance Team, Investors, Operations Team

---

## Executive Summary

Data handling at Sukoon AI covers how personal and clinical data is stored, accessed, retained, and protected throughout its lifecycle. Given that the platform deals with sensitive mental health data, data handling practices must meet the highest standards of care, security, and accountability. This document defines the data categories on the platform, how each is stored and protected, who can access it, and how long it is retained.

---

## Purpose

To provide a complete reference for how data flows through the Sukoon AI platform — from collection to storage to access to deletion — for compliance, audit, and operational purposes.

---

## Stakeholders

- Technical team (implementation of data controls)
- Legal/compliance team (regulatory review)
- Operations team (operational data practices)
- Investors (data governance assurance)
- Auditors (compliance verification)

---

## 1. Data Categories

| Category | Examples | Sensitivity |
|---|---|---|
| **Identity Data** | Name, email, phone number | Standard |
| **Authentication Data** | Password hash, Google OAuth token | High |
| **Clinical Data** | AI chat messages, journal entries, mood check-in responses | Very High |
| **Financial Data** | Payment screenshots, transaction IDs, payout records | High |
| **Behavioral Data** | Login activity, feature usage, streak/gamification data | Standard |
| **Operational Data** | Support tickets, admin audit logs, therapist applications | High |
| **AI Memory Data** | Extracted summaries from conversations | Very High |

---

## 2. Data Storage Architecture

### Database
The platform uses:
- **SQLite** during development (single-file local database)
- **PostgreSQL via Supabase** in production (cloud-hosted, managed relational database)

Supabase (the production database host) provides:
- Automated backups
- Connection encryption (TLS/SSL)
- Row-level security (database access control)
- Geo-redundant storage

### File Storage
Payment screenshots uploaded by clients and therapists are stored securely. These files:
- Are stored with access controls preventing unauthorized download
- Are not publicly accessible via URL
- Can only be accessed by admin personnel with verified access

---

## 3. Data Security Measures

### Encryption
| Layer | Encryption Applied |
|---|---|
| **Data in transit** | TLS/HTTPS on all connections between client, server, and database |
| **Authentication tokens** | JWT tokens with expiry; not stored client-side beyond session |
| **Passwords** | Never stored in plain text; hashed before storage |
| **Database connections** | Encrypted connections to production database |

### Access Control
| Data Category | Who Can Access |
|---|---|
| **Identity Data** | Admin team (for account management) |
| **Clinical Data (chat, journal)** | Clinical supervisor, Super Admin only (with documented justification) |
| **Financial Data** | Finance team, Admin Lead |
| **AI Memory Data** | Clinical supervisor, Super Admin |
| **Operational Data (logs, tickets)** | Admin team (role-appropriate access) |

### Authentication
- All admin accounts require strong passwords
- Admin access to sensitive data should require two-factor authentication (2FA) — recommended for immediate implementation
- API keys (Gemini API, Supabase) are stored as environment variables on the server, never in code or client-side

---

## 4. Data Retention Policy

| Data Type | Retention Period | Rationale |
|---|---|---|
| **AI chat messages** | Until account deletion | Clinical continuity; crisis review |
| **Journal entries** | Until account deletion | User wellbeing record |
| **Payment records** | 7 years minimum | Financial compliance |
| **Support ticket content** | 3 years | Dispute reference; quality review |
| **Admin audit logs** | 3 years | Accountability and compliance |
| **Therapist application records** | 5 years | Professional reference |
| **Safety incident logs** | 7 years | Legal and clinical protection |
| **Risk alert records** | 3 years | Clinical safety review |

### Tarash Zone Exception
Tarash Zone data is **never stored** — there is no retention period because nothing is written to the database during these sessions.

### Account Deletion
When a user requests account deletion:
- Personally identifiable information (name, email, phone number) is removed
- Clinical data (chat, journal) is deleted
- Financial records are anonymized (payment amount and date retained; PII removed)
- Support ticket history is anonymized
- The account record is marked deleted (not physically removed for database integrity)

---

## 5. Data Backup

### Automated Backups
Production database backups are managed by Supabase:
- Daily automated backups
- Point-in-time recovery capability
- Backups stored in geo-redundant locations

### Backup Testing
Backups should be tested quarterly by restoring to a non-production environment to confirm they are complete and usable.

### Backup Retention
Backups are retained for:
- Daily backups: 30 days
- Weekly backups: 12 weeks

---

## 6. Data Access Logging (Audit Trail)

All access to sensitive data categories should be logged:

| Event | What Is Logged |
|---|---|
| **Admin accesses user clinical data** | Admin ID, user ID, timestamp, reason |
| **Admin modifies user account status** | Admin ID, action taken, user ID, timestamp |
| **Admin processes payment** | Admin ID, payment ID, action, timestamp |
| **Admin processes payout** | Admin ID, therapist ID, amount, timestamp |
| **API key used for AI call** | Timestamp, user session, token count |

This audit trail is critical for:
- Governance accountability
- Investigating complaints about data misuse
- Regulatory compliance

---

## 7. Third-Party Data Processors

| Third Party | Data Shared | Purpose | Location |
|---|---|---|---|
| **Google Gemini API** | AI chat messages (current session) | AI response generation | Google Cloud |
| **Google Firebase** | User email, display name | Authentication (Google OAuth) | Google Cloud |
| **Supabase** | All production database data | Database hosting | AWS/US-East (configurable) |

### Data Processing Agreements
For each third-party processor, a **Data Processing Agreement (DPA)** should be in place. These agreements define:
- What data is processed
- How it is protected
- What the processor is permitted to do with it

---

## 8. Incident Response (Data Breach)

If a data breach or unauthorized access is suspected:

### Immediate Steps (Within 1 Hour)
1. Identify the scope — which data, which users affected
2. Contain the breach — revoke compromised credentials, disable affected endpoints
3. Alert the technical lead and Operations Manager

### Short-Term Response (Within 24 Hours)
1. Conduct a full investigation
2. Identify root cause
3. Document all affected records
4. Begin notification preparation for affected users

### Notification
- Affected users must be notified of a breach that may affect their personal data
- Notification should include: what happened, what data was affected, what is being done, and what users should do
- Regulatory authorities must be notified as required by applicable law

---

## Process Flow (Data Lifecycle)

```
DATA COLLECTION:
User provides data at registration / during use
        │
        ▼
DATA STORAGE:
Stored in encrypted production database (Supabase / PostgreSQL)
        │
        ▼
DATA ACCESS:
Role-based access controls limit who can view
Audit log records every sensitive access
        │
        ▼
DATA RETENTION:
Retained per category-specific retention schedule
        │
        ▼
DATA DELETION:
User requests deletion → PII removed → Records anonymized
OR
Retention period expires → Automated deletion (recommended)
```

---

## Business Impact

| Data Handling Practice | Business Impact |
|---|---|
| **Encryption at rest and in transit** | Reduces breach risk; builds user trust |
| **Role-based access controls** | Prevents unauthorized internal access |
| **Clear retention policy** | Legal compliance; reduces storage costs |
| **Audit trail** | Governance accountability; investor confidence |
| **Backup and recovery** | Business continuity; protects against data loss |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Database breach** | Unauthorized access to all user data | Encryption; access controls; regular security testing |
| **API key exposure** | Gemini/Supabase keys leaked | Environment variables only; never in code; key rotation |
| **Inadequate audit logging** | Data misuse not traceable | Implement comprehensive audit logging from day one |
| **Regulatory non-compliance** | Data handled in a way that violates privacy law | Legal review; DPAs with third parties; privacy policy |
| **Backup failure** | Database corrupted with no recovery option | Test backups quarterly; maintain geo-redundant backups |

---

## Recommendations

1. **Engage a cybersecurity consultant** to conduct a penetration test of the production platform before launch, identifying vulnerabilities that internal teams may have missed.
2. **Implement 2FA for all admin accounts** as an immediate priority — admin credentials are the highest-value target for unauthorized access.
3. **Conduct a Data Protection Impact Assessment (DPIA)** — a structured process for identifying and mitigating privacy risks associated with each data category and processing activity.
4. **Set up key rotation schedules** for API keys and database credentials — rotating every 90 days ensures that any exposed credential has a limited validity window.
5. **Document all data flows** in a Data Flow Diagram — a visual map of how data moves between user, server, database, and third parties — as this is a requirement for regulatory review and useful for internal security awareness.
