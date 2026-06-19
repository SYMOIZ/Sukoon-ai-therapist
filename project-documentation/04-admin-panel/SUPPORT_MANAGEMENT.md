# Support Management — Sukoon AI

**Section:** 04 — Admin Panel  
**Document:** SUPPORT_MANAGEMENT.md  
**Audience:** Support Team, Admin Team, Operations Team, Customer Experience

---

## Executive Summary

Support Management on Sukoon AI is a centralized ticketing system that handles all client and therapist requests for assistance, dispute resolution, refund claims, technical issues, and therapist complaints. Every support interaction is tracked through a structured ticket system with defined categories, priorities, statuses, and resolution workflows. This document describes how the support team operates, handles tickets, and measures performance.

---

## Purpose

To define the complete support management process — how tickets are received, categorized, assigned, handled, escalated, and resolved — enabling the support team to deliver consistent, timely assistance.

---

## Stakeholders

- Support team (primary ticket handlers)
- Admin team (escalated tickets and account actions)
- Clinical team (safety-related tickets)
- Finance team (refund and payout tickets)
- Clients and therapists (ticket submitters)

---

## 1. Ticket Submission

### How Clients Submit Tickets
Clients can submit a support ticket from:
- The **Support** page in their app (Settings → Support)
- The **Contact** or **Help** section in the app menu

### How Therapists Submit Tickets
Therapists can submit tickets related to:
- Payout disputes
- Booking issues
- Profile or account problems
- Technical issues

### Ticket Submission Form
When creating a ticket, the user provides:
- **Subject** — Short description of the issue
- **Category** — Selected from predefined list (see Section 2)
- **Priority** — Selected by the user (Low, Medium, High, Critical)
- **Description** — Full explanation of the issue
- **Attachments** — Screenshots, receipts, or evidence (optional)

---

## 2. Ticket Categories

| Category | Typical Issues |
|---|---|
| **Technical Issue** | App crashes, features not loading, error messages |
| **Billing / Payment** | Incorrect charge, payment not recognized, receipt issues |
| **Booking Issue** | Booking not confirmed, session not delivered, cancellation dispute |
| **Account Issue** | Cannot log in, account suspended, deletion request |
| **Therapist Complaint** | Inappropriate behavior, missed session, quality concern |
| **Refund Request** | Claiming refund for cancelled or undelivered session |
| **Other / General** | Any issue not fitting the above categories |

---

## 3. Ticket Statuses

| Status | Meaning |
|---|---|
| **Open** | Submitted; awaiting admin review |
| **In Progress** | Admin has reviewed and is actively working on resolution |
| **Awaiting User Response** | Admin replied and is waiting for more information from user |
| **Escalated** | Referred to a senior team member or specialist |
| **Resolved** | Issue addressed; user notified |
| **Closed** | Resolution confirmed; ticket archived |

### Status Flow

```
User Submits Ticket
      │
      ▼
   Open
      │
Admin Reviews
      │
  ┌───┴──────────────────┐
  │                        │
Simple Issue           Complex Issue
  │                        │
  ▼                        ▼
In Progress            Escalated
  │                        │
Admin Acts             Senior Admin /
  │                   Finance / Clinical
  ▼                   Team Reviews
Awaiting User                │
Response (if needed)         ▼
  │                     Resolution
  ▼
Resolved
  │
  ▼
Closed (after confirmation)
```

---

## 4. Admin Support Workflow

### Daily Ticket Review
Every working day, the support team:
1. Reviews all **Open** tickets (newest and highest-priority first)
2. Assigns each ticket to an appropriate team member
3. Categorizes any incorrectly categorized tickets
4. Begins working through **In Progress** tickets
5. Closes resolved tickets that have had confirmation or after 3 days without user response

### Responding to a Ticket
Admins reply through the ticket thread in the Admin Support Dashboard. Each reply:
- Is timestamped and attributed to the responding admin
- Triggers an in-app notification to the user
- Advances the ticket status (e.g., from Open to In Progress)
- Can include internal notes (visible only to admins, not the user)

### Internal Notes
Admins can add **internal notes** to a ticket visible only to the admin team. This is used to:
- Record investigation steps taken
- Note consultations with other team members
- Document reasons for decisions (especially for refunds and bans)

---

## 5. Priority Levels and SLAs

| Priority | Description | Target First Response |
|---|---|---|
| **Critical** | Platform-wide outage, safety emergency | Within 1 hour |
| **High** | Billing error, confirmed booking dispute | Within 4 hours |
| **Medium** | General inquiry, account issue | Within 24 hours |
| **Low** | Feature request, minor cosmetic issue | Within 72 hours |

---

## 6. Handling Specific Ticket Types

### Refund Requests
1. Admin verifies the booking record linked to the refund claim
2. Admin checks session status — was the session delivered?
3. If eligible for refund:
   - Refund is processed through the finance team
   - Session booking is marked as "Refunded"
   - Therapist's wallet is adjusted (earnings reversed)
4. If not eligible:
   - Admin explains why the refund cannot be processed
   - Offer alternatives (rescheduling, credit to platform wallet)

### Therapist Complaints
1. Admin reviews the complaint with the therapist's record and session history
2. Admin may access the relevant session notes or incident log
3. Admin investigates with the therapist through a separate communication channel
4. Resolution may include:
   - Warning issued to therapist
   - Session refunded to client
   - Therapist account suspended pending review
   - Complaint dismissed (if unfounded)

### Booking Disputes
1. Admin reviews the booking record (status history, payment proof, session notes)
2. Contacts both client and therapist if needed
3. Makes a determination based on evidence
4. Updates booking status accordingly
5. Issues any refund or credit as appropriate

### Account Issues
1. Admin verifies the account holder's identity
2. Takes appropriate action (unlock, reset, review suspension)
3. Communicates outcome to the user

---

## 7. Escalation Process

Some tickets require escalation beyond the first-line support team:

| Escalation Trigger | Escalates To |
|---|---|
| Client in active crisis | Clinical supervisor → crisis intervention |
| Fraudulent payment activity | Finance team + Super Admin |
| Legal threat or formal complaint | Management + Legal advisor |
| Therapist misconduct | Clinical supervisor + Super Admin |
| Data breach or privacy violation | Super Admin + Technical team |

Escalated tickets are flagged and assigned directly to the appropriate senior team member with a notification.

---

## 8. Ticket Metrics and Reporting

The support team tracks:

| Metric | Definition |
|---|---|
| **Average First Response Time** | Time from submission to first admin reply |
| **Average Resolution Time** | Time from submission to "Resolved" status |
| **Open Ticket Count** | Number of unresolved tickets at any moment |
| **Tickets by Category** | Volume breakdown by issue type |
| **User Satisfaction Rate** | Rating given after ticket resolution |
| **Escalation Rate** | Percentage of tickets requiring escalation |

---

## Process Flow (Support Ticket Lifecycle)

```
User Submits Ticket
      │
      ▼
Ticket Created (Open)
      │
      ▼
Admin Assigned
      │
      ▼
Admin Investigates
  ├── Reviews booking / account / payment records
  └── Contacts user for more info (→ Awaiting Response)
      │
      ▼
Admin Takes Action
  ├── Issues refund (Finance Team)
  ├── Sends account action (suspension, reinstatement)
  ├── Escalates (Clinical / Management)
  └── Provides information / closes query
      │
      ▼
Ticket Marked Resolved
      │
      ▼
User Confirmation (3-day window)
      │
      ▼
Ticket Closed
```

---

## Business Impact

| Support Quality | Business Impact |
|---|---|
| **Fast response times** | User satisfaction; reduced churn |
| **Fair refund policy** | Trust in platform; repeat usage |
| **Effective complaint resolution** | Protects therapist quality; client retention |
| **Escalation of safety issues** | Clinical responsibility; legal protection |
| **Ticket tracking** | Identifies recurring issues; informs product improvements |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Backlogged tickets** | Support team overwhelmed | Prioritization system; SLA monitoring; staffing review |
| **Inconsistent resolutions** | Different outcomes for similar cases | Documented resolution policy; case precedent library |
| **Delayed safety escalation** | Crisis ticket not escalated fast enough | Priority flag for any safety-related category; 1-hour SLA |
| **Fraudulent refund claims** | Users claiming refunds for sessions they attended | Cross-reference with session notes and therapist records |
| **Sensitive data exposure** | Support agents accessing data beyond their scope | Role-based data access; audit logging |

---

## Recommendations

1. **Build a ticket knowledge base** — a searchable internal reference for support agents with pre-written responses and resolution templates for the most common ticket types.
2. **Implement post-resolution satisfaction surveys** — a 1-3 question rating sent to users after their ticket is resolved, providing feedback on support quality.
3. **Add a ticket auto-categorizer** — an AI-assisted tool that suggests a category and priority for new tickets based on the subject and description, saving admin time.
4. **Set up a weekly support metrics review** — a standing 30-minute team meeting to review ticket volumes, SLA adherence, and recurring issues.
5. **Create a therapist support path** — a dedicated ticket channel or priority queue for therapist-submitted issues, recognizing that unresolved therapist issues directly impact session delivery capacity.
