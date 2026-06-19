# Therapist Workflow — Sukoon AI

**Section:** 03 — Therapist Portal  
**Document:** THERAPIST_WORKFLOW.md  
**Audience:** Therapists, Therapist Relations Team, Operations, Clinical Team

---

## Executive Summary

Once approved, a Sukoon AI therapist follows a structured weekly and monthly workflow: maintaining their profile, managing their calendar, accepting and delivering sessions, communicating with clients, writing clinical notes, logging safety incidents, and submitting payout requests. This document maps the complete operational cycle of an active therapist on the platform.

---

## Purpose

To define the day-to-day and week-to-week workflow that active therapists follow on the Sukoon AI platform, enabling therapist relations teams to train and support therapists effectively.

---

## Stakeholders

- Active therapists (primary users of this workflow)
- Therapist relations team (support and training)
- Clinical supervisors (quality oversight)
- Finance team (payout processing)

---

## 1. Weekly Workflow Overview

```
MONDAY–FRIDAY: Core Operating Cycle

Morning:
  ├── Check notifications for new bookings
  ├── Review upcoming session schedule
  └── Respond to any direct messages from clients

Session Days:
  ├── Conduct scheduled sessions (audio/video/chat)
  ├── Write therapy notes immediately after sessions
  └── Log any safety incidents during sessions

End of Day:
  ├── Update calendar availability for the following week
  └── Review any pending client requests

MONTHLY:
  └── Submit payout request for accumulated earnings
```

---

## 2. Calendar Management

### Setting Availability
Therapists manage their schedule by creating **calendar slots** — specific date/time blocks they are available for sessions. Each slot includes:
- Date
- Time
- Session duration
- Status (available, booked, pending)
- Session type (CBT, General Talk, Mindfulness, etc.)

### Calendar Rules
- Therapists should set availability at least one week in advance
- Booked slots are locked once a session is confirmed
- Unavailable times should be blocked to prevent incorrect bookings

### Booking Notifications
When a client books a slot:
1. The slot changes from "available" to "pending" (payment under review)
2. Once admin approves the payment, the slot becomes "booked"
3. The therapist receives a notification at each stage

---

## 3. Client Bookings — Receiving and Confirming

### How Bookings Arrive
Clients choose a therapist from the directory, select an available slot, and submit their booking with payment proof. Therapists do not directly accept or reject bookings — the admin team handles payment verification.

### What Therapists See
Therapists can see all their bookings in the **Session Management** section of their dashboard, with statuses:
- Payment Under Review
- Confirmed
- Completed
- Cancelled

### Pre-Session Communication
Therapists can use the **Direct Messages** feature to:
- Confirm the session format with the client
- Ask the client to prepare (e.g., complete a morning journal beforehand)
- Clarify any questions about the session

---

## 4. Conducting Sessions

### Session Types
Therapists deliver sessions through three modes:
- **Audio** — Voice-only call
- **Video** — Video call
- **Chat/Text** — Text-based therapeutic session

Note: The platform facilitates the booking and scheduling. The actual session delivery may use the platform's built-in communication tools or an external meeting tool agreed upon between the therapist and client.

### Session Notes
After each session, therapists are expected to write **therapy notes** documenting:
- Session title and date
- Progress observed
- Areas of concern
- Mark type (Progress, Warning, Needs Follow-up)
- Next reminder / follow-up date

These notes are stored securely and visible to the therapist and the admin clinical team. They are **not** visible to the client by default.

---

## 5. Safety Incident Logging

### What Is a Safety Incident?
During a session, a therapist may encounter a situation requiring formal documentation:
- Client expresses suicidal ideation or self-harm risk
- Harassment or abusive language from client
- Privacy violation
- Inappropriate behavior

### How to Log
Therapists log safety incidents directly from their dashboard. Each incident record includes:
- Client name
- Incident type
- Time of incident
- Detailed description
- Current status (Reported, Under Review, Resolved)

### Who Sees These Reports
Safety incidents are immediately visible to the admin and clinical oversight team. They may trigger a review of the client account, notification to emergency contacts, or intervention by the platform's crisis team.

---

## 6. Paid Chat Pricing

### What It Is
Beyond standard session bookings, therapists can set specific pricing for **paid chat access** — time-gated text chat access for clients who want to message them outside of formal sessions.

### Pricing Tiers
Therapists can set three chat access prices:
- **1-Day Access** — Short-term access fee
- **7-Day Access** — Weekly access fee
- **1-Month Access** — Monthly access fee

These prices are publicly visible on the therapist's profile and give clients a flexible way to access follow-up support.

---

## 7. Reviews and Ratings

### How Reviews Work
After a session is marked **"Completed"**, clients are invited to leave a rating (1–5 stars) and a written comment about their experience.

### Therapist Response
Therapists can reply to reviews from their dashboard. This allows them to:
- Thank clients for positive feedback
- Address concerns from neutral or negative reviews professionally

### Impact of Ratings
- Rating and review count are displayed on the therapist's public profile
- Higher ratings increase booking likelihood
- Consistently low ratings may trigger a quality review by the admin team

---

## 8. Earnings Tracking

### How Earnings Accumulate
Every time a session payment is approved, the therapist's earning is recorded in the **Wallet Transactions** system. The therapist earns **85% of the session fee**; 15% goes to the platform as commission.

### Viewing Earnings
Therapists can see:
- Total accumulated earnings
- Individual transaction records
- Payout history

### Submitting a Payout Request
Therapists submit a payout request from their dashboard when they are ready to withdraw accumulated earnings:
1. Specify the amount requested
2. Select or confirm payment method (bank account details)
3. Submit the request

The admin/finance team processes payout requests. The status moves from "Pending" to "Processed" once the transfer is made. Payouts are tracked against a configurable payout cycle (e.g., bi-weekly or monthly).

---

## 9. Direct Messaging

### Use of Direct Messages
Between sessions, therapists use the **Direct Messages** channel for:
- Checking in with clients
- Sending mindfulness exercises or homework
- Confirming appointment logistics
- Responding to client questions

### Boundaries
Direct messaging is professional in nature. Therapists are expected to maintain clinical boundaries in all written communications, as these are logged and may be reviewed.

---

## 10. Therapist Follow-Up System

### Follow-Up Conversations
The platform supports structured **follow-up conversations** — formally tracked chat threads between therapist and client that are linked to a specific booking or risk alert. These are distinct from informal direct messages.

### Follow-Up Request Process
1. A follow-up request is created (either by the therapist, admin, or via a risk alert)
2. The therapist accepts the follow-up
3. A dedicated conversation thread opens with an expiry date
4. The message count is tracked
5. At expiry, the follow-up is closed or renewed

---

## Process Flow (Weekly)

```
Start of Week
     │
     ▼
Review Calendar → Add/Adjust Availability Slots
     │
     ▼
Check Notifications → New Bookings / DMs / Alerts
     │
     ▼
Session Days:
  Confirm Client → Conduct Session → Write Notes
                                     │
                                     ▼
                               Safety Incident? → Log Incident
                                     │
                                     ▼
                                No Incident → Normal Close
     │
     ▼
Review Earnings → (Monthly) Submit Payout Request
     │
     ▼
Respond to Reviews → Update Profile if Needed
```

---

## Business Impact

| Activity | Business Impact |
|---|---|
| **Calendar completeness** | Empty calendars = no bookings = no revenue |
| **Session completion rate** | Directly drives commission revenue |
| **Therapy notes quality** | Enables clinical oversight and quality assurance |
| **Safety incident logging** | Protects platform from liability; supports crisis response |
| **Review responses** | Improves therapist profile attractiveness |
| **Payout requests** | Must be processed promptly to retain therapist satisfaction |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **No-show sessions** | Therapist or client doesn't attend | No-show policy; admin mediates disputes |
| **Undocumented incidents** | Therapist omits safety incident logging | Training on mandatory reporting; admin audit |
| **Delayed payouts** | Finance team slow to process | Payout SLA of 5–7 business days |
| **Boundary violations** | Inappropriate DMs between therapist and client | Message monitoring by admin; clear professional conduct guidelines |
| **Profile abandonment** | Therapist stops updating calendar | Auto-deactivation after 30 days of no availability |

---

## Recommendations

1. **Create a weekly digest notification** that summarizes a therapist's upcoming week — bookings, unread messages, pending notes — in a single notification.
2. **Implement automated session reminders** sent to both therapist and client 24 hours and 1 hour before a scheduled session.
3. **Build a session completion workflow** that automatically prompts the therapist to write notes after a session is marked complete.
4. **Create a therapist handbook** — a detailed guide to professional standards, boundary expectations, and incident reporting procedures.
5. **Introduce a peer review system** where senior therapists periodically review session notes of newer therapists to maintain clinical standards.
