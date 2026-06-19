# Client Assignment — Sukoon AI

**Section:** 03 — Therapist Portal  
**Document:** CLIENT_ASSIGNMENT.md  
**Audience:** Admin Team, Clinical Team, Therapists, Operations

---

## Executive Summary

Client assignment on the Sukoon AI platform can occur through two pathways: self-directed client booking (where clients choose their own therapist from the directory) and admin-managed manual assignment (where the admin team matches a client to a therapist based on clinical need, availability, or crisis escalation). This document covers both pathways and the complete lifecycle of a therapist-client connection.

---

## Purpose

To document how clients are connected to therapists on the Sukoon AI platform, including the self-booking pathway, manual admin assignment, and crisis-triggered emergency assignment.

---

## Stakeholders

- Admin team (manual assignment and crisis escalation)
- Clinical team (crisis-triggered assignments)
- Therapists (receiving assigned clients)
- Clients (choosing or being assigned therapists)

---

## 1. Self-Directed Booking (Primary Pathway)

### How It Works
The most common pathway. A client independently:
1. Browses the Therapist Directory
2. Reviews therapist profiles, specializations, ratings, and pricing
3. Selects a therapist who matches their needs
4. Books an available time slot
5. Completes payment

This creates a booking record and, upon payment approval and session confirmation, establishes a formal **Therapist Connection** between the client and therapist.

### What Gets Created
When a booking is confirmed:
- A **Session Booking** record (links client_id and therapist_id)
- A **Therapist Connection** record (formal relationship object)
- A **Direct Message** channel between client and therapist
- A **Calendar Slot** update (slot marked as "booked")

---

## 2. Manual Admin Assignment

### What It Is
The admin team can manually assign a client to a therapist. This is used when:
- A client submits a support request for therapist matching help
- A client's profile indicates needs that require a specific type of therapist
- A risk alert requires immediate professional intervention
- A previous therapist is unavailable and the client needs a replacement

### How Admins Perform Manual Assignment
Admins use the **Manual Assign Modal** in the Admin Dashboard:
1. Search for and select the **client** (by name or ID)
2. Search for and select the **therapist** (by name or ID, using a searchable dropdown)
3. Set connection details (session type, date, notes)
4. Confirm the assignment

This creates the same Therapist Connection record as a self-booked session, but without going through the standard booking/payment flow.

### Searchable Selection
Both client and therapist selection use a **SearchableSelect** component — a type-ahead search tool that queries the live user database, allowing admins to find users quickly without scrolling through long lists.

---

## 3. Crisis-Triggered Assignment

### What It Is
The highest-priority assignment pathway. When a risk alert is generated (by the AI detecting crisis language in a client's chat), the admin team can assign a crisis-certified therapist to respond to the client.

### Process
1. AI detects crisis language in a client chat session
2. A **Risk Alert** is created and appears in the Admin Dashboard
3. The admin (or clinical supervisor) reviews the alert
4. The admin assigns a crisis-certified therapist to the client using the **Manual Assign** function
5. The assignment is tracked with an assignment status:
   - `none` — Not yet assigned
   - `pending` — Assignment sent; therapist not yet responded
   - `accepted` — Therapist has acknowledged the assignment
   - `rejected` — Therapist is unavailable; reassignment needed
6. The assigned therapist receives a notification with context
7. The therapist initiates contact with the client through direct messages or a follow-up conversation

### Response Deadline
Each crisis assignment includes a **response deadline** — the time by which the therapist must acknowledge and initiate contact. If the deadline is missed, the alert escalates to the next available crisis-certified therapist.

---

## 4. Therapist Connection Record

### What a Connection Represents
A Therapist Connection is the formal record of the relationship between a specific therapist and a specific client on the platform. It includes:

| Field | Description |
|---|---|
| **Connection ID** | Unique identifier |
| **Therapist ID** | Assigned therapist |
| **Client ID** | Connected client |
| **Status** | Active, Disputed, Ended |
| **Total Sessions** | Count of completed sessions in this connection |
| **Last Meeting** | Date of most recent session |
| **Meeting Link** | Video/audio call link (if applicable) |
| **Chat Expires At** | Expiry date for direct message access |

### Connection Status Lifecycle

```
Created (on booking confirmation or admin assignment)
    │
    ▼
  ACTIVE
    │
  ┌─┴───────────────────────┐
  │                         │
Dispute filed          Both parties agree
  │                    session is complete
  ▼                         │
DISPUTED                    ▼
  │                       ENDED
  ▼
Admin mediates
  │
  └── Resolved → ACTIVE or ENDED
```

---

## 5. Connection Details

### Admin View
From the Admin Dashboard, admins can view all therapist-client connections using the **Connection Details Modal**, which shows:
- All current connections
- Connection status
- Session count per connection
- Last meeting date
- Any disputed connections requiring intervention

### Therapist View
Therapists see their active client connections from the **Clients** section of their dashboard.

---

## 6. Multiple Connections

A client may have connections with multiple therapists — for example, if they:
- Tried one therapist and wanted to try another
- Have different therapists for different concerns
- Were re-assigned due to a previous therapist's unavailability

The system does not restrict the number of active connections a client can have. Admin oversight ensures connections remain appropriate.

---

## 7. Ending a Connection

A therapist-client connection is ended when:
- Both parties agree the therapeutic relationship is complete
- The session contract (number of sessions agreed) is fulfilled
- The client discontinues or cancels future bookings
- An admin ends the connection due to a policy violation or complaint
- A disputed connection is resolved through ending the relationship

Ended connections are archived but not deleted, preserving the session history and therapy notes for clinical reference.

---

## Process Flow

```
CLIENT SELF-BOOKING:
Client Browses Directory → Selects Therapist → Books Slot
  → Payment Approved → Session Confirmed → Connection Created

ADMIN MANUAL ASSIGNMENT:
Admin Receives Request / Risk Alert
  → Opens Manual Assign Modal
  → Selects Client + Therapist
  → Confirms Assignment → Connection Created

CRISIS ASSIGNMENT:
AI Detects Crisis → Risk Alert Created
  → Admin Reviews → Assigns Crisis Therapist
  → Assignment Status: Pending → Accepted
  → Therapist Contacts Client → Follow-up Opened
```

---

## Business Impact

| Metric | Business Significance |
|---|---|
| **Client-therapist match quality** | Poor matches lead to early session cancellation; quality matches drive rebooking |
| **Manual assignment speed** | Crisis assignments must be fast; delays have safety implications |
| **Connection retention** | Clients with long-term connections generate recurring revenue |
| **Disputed connections** | Disputes signal dissatisfaction; need rapid admin intervention |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Poor match quality** | Client and therapist are incompatible | Offer one session "trial" option; easy reassignment process |
| **Therapist rejection of crisis assignment** | Crisis goes unresponded | Require minimum on-call therapist coverage; automatic reassignment |
| **Connection without sessions** | Connection created but client never books again | Follow-up notification after 14 days of inactivity |
| **Disputed connections** | Unresolved disputes create negative experiences | Admin-mediated resolution process with defined timeline |

---

## Recommendations

1. **Implement an AI-assisted matching system** that suggests the top 3 best-fit therapists based on client language, presenting concerns, and therapist specializations — reducing trial-and-error in self-directed booking.
2. **Create a formal handover protocol** when a client is transferred from one therapist to another, ensuring clinical continuity.
3. **Add a crisis-certified therapist roster view** in the Admin Dashboard so the on-call team can quickly see who is available for urgent assignments.
4. **Define a "connection quality score"** based on session frequency, therapist rating, and client retention — helping the admin team identify struggling relationships before they end.
5. **Implement a connection satisfaction survey** sent to clients after their third session, gathering feedback on therapist fit.
