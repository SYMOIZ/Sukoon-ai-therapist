# Session Management — Sukoon AI

**Section:** 03 — Therapist Portal  
**Document:** SESSION_MANAGEMENT.md  
**Audience:** Therapists, Admin Team, Finance Team, Operations

---

## Executive Summary

Session management on Sukoon AI covers the complete lifecycle of a therapy session — from the initial booking through payment verification, session delivery, completion, rating, and payout. This document describes every step, the roles involved, and the status changes that move a session from intent to completion.

---

## Purpose

To provide a complete operational reference for how therapy sessions are created, managed, verified, delivered, and closed on the Sukoon AI platform.

---

## Stakeholders

- Clients (initiating bookings)
- Therapists (receiving and delivering sessions)
- Admin team (payment verification, dispute resolution)
- Finance team (payout processing)
- Operations team (SLA monitoring)

---

## 1. Session Types

| Type | Description |
|---|---|
| **Audio** | Voice-only session — call-based |
| **Video** | Full video session — camera-enabled call |
| **Chat / Text** | Written text conversation session |

Therapists decide which session types they offer on their profile. Clients select from the available options during booking.

---

## 2. Session Duration Options

Standard session durations:
- **45 minutes** — Brief session (check-in, follow-up)
- **60 minutes** — Standard full session
- **90 minutes** — Extended deep session

Pricing varies by duration and is set by each therapist independently.

---

## 3. Complete Session Lifecycle

### Status Definitions

| Status | Who Sets It | Meaning |
|---|---|---|
| **Draft** | System (when booking starts) | Booking in progress, not yet submitted |
| **Pending Payment** | Client (on submission) | Client submitted booking; awaiting payment proof upload |
| **Payment Under Review** | Admin | Payment screenshot uploaded; admin is reviewing |
| **Payment Approved** | Admin | Payment verified; booking confirmed |
| **Payment Rejected** | Admin | Payment could not be verified; client notified with reason |
| **Therapist Assigned** | Admin | Therapist confirmed for the session |
| **Session Confirmed** | Admin / System | Both parties notified; session is scheduled |
| **Session Completed** | Admin / Therapist | Session has been delivered successfully |
| **Cancelled** | Admin / Client / Therapist | Session cancelled before delivery |

### Status Flow Diagram

```
Client Starts Booking
        │
        ▼
      Draft
        │
Client Submits with Payment Proof
        │
        ▼
  Pending Payment
        │
Admin Reviews Payment Screenshot
        │
   ┌────┴────────────────────┐
   │                         │
Payment                   Payment
Approved                  Rejected
   │                         │
   ▼                         ▼
Payment Approved         Client Notified
   │                    (with reason)
   ▼
Therapist Assigned
   │
   ▼
Session Confirmed
(Both parties notified)
   │
   ▼
Session Delivered (on scheduled date)
   │
   ▼
Session Completed
   │
   ▼
Client Leaves Review
Therapist Writes Notes
Earnings Credited
```

---

## 4. Payment Verification Details

### What Admin Reviews
When reviewing a payment, the admin checks:
- Payment screenshot clarity (is the transfer clearly visible?)
- Transaction ID (can it be matched to expected payment methods?)
- Amount matches the session fee
- Transfer date is recent and plausible
- Recipient account matches platform payment details

### Approval Timeline
The target for payment verification is **24–48 hours** after submission. The admin team must prioritize payment reviews to avoid booking delays that frustrate both clients and therapists.

### Rejection Scenarios
Common rejection reasons:
- Screenshot is unclear or appears edited
- Amount does not match the session fee
- Transaction ID is invalid
- Payment account doesn't match expected details
- Payment made to wrong account

---

## 5. Session Notes

### Timing
Therapy notes are written **after** each session, ideally within 24 hours while details are fresh.

### Required Note Fields
| Field | Requirement |
|---|---|
| **Title** | Required — brief session label |
| **Details** | Required — clinical narrative |
| **Mark Type** | Required — Progress, Warning, or Needs Follow-up |
| **Date of Note** | Required — date the note was written |
| **Next Reminder** | Optional — follow-up scheduling |

### Note Privacy
- Therapy notes are visible to the therapist and admin/clinical team
- Notes are **not** visible to clients by default (privacy is essential for honest clinical documentation)
- Clients may request access to their notes; this is handled on a case-by-case basis by the admin team

---

## 6. Session Completion and Post-Session Workflow

### Completing a Session
After the session occurs at the scheduled time:
1. Admin (or the system, if automated) marks the session status as **"Session Completed"**
2. The therapist writes session notes
3. The client is prompted to leave a rating and review
4. Earnings are credited to the therapist's wallet

### Client Rating
Clients rate their session on a 1–5 star scale and may leave an optional written comment. Ratings are:
- Public (visible on the therapist's directory profile)
- Tied to the specific booking for audit purposes

### Therapist Notes
Written immediately after the session. These form the therapist's clinical record and are critical for continuity in ongoing care relationships.

---

## 7. Cancellations

### Who Can Cancel
- **Clients** can cancel a session before the confirmed date (refund policy applies)
- **Therapists** can cancel a session if they have a legitimate reason (emergency, illness)
- **Admins** can cancel on behalf of either party

### Cancellation Impact
- Cancelled session status is marked "Cancelled"
- If payment was approved, a refund process is initiated
- The therapist's calendar slot is released back to "available"
- Both parties are notified

### Cancellation Policy
A formal cancellation policy should be defined by the operations team covering:
- How far in advance a cancellation is permitted without penalty
- Refund eligibility window
- Consequences for repeated no-shows

---

## 8. Disputes

### When Disputes Occur
Disputes can arise from:
- Session not delivered as described
- Therapist did not attend the session
- Client claims payment was made but rejected without cause
- Quality of session significantly below expectations

### Dispute Resolution
1. Client submits a support ticket under **"Booking Issue"**
2. Admin team reviews the booking record, payment screenshots, and session notes
3. Admin mediates between client and therapist
4. Resolution may include:
   - Refund to client
   - Rebooking at no extra charge
   - Session fee credited to client wallet
   - Therapist warning (if at fault)

---

## 9. Earnings and Payouts per Session

### Earning Calculation
For each confirmed and completed session:
- **Total Session Fee** = Set by therapist (example: PKR 150)
- **Platform Commission** = 15% of session fee (example: PKR 22.50)
- **Therapist Earnings** = 85% of session fee (example: PKR 127.50)

### Wallet Credit
Earnings are credited to the therapist's wallet as a **Wallet Transaction** record immediately upon session completion and payment verification.

### Payout Request
Therapists request withdrawal of accumulated earnings. The admin/finance team processes payouts on a defined cycle (recommended: bi-weekly or monthly).

---

## Process Flow Summary

```
Client Books → Payment Proof Uploaded
                    │
              Admin Verifies
                    │
         ┌──────────┴──────────┐
         │                     │
      Approved              Rejected
         │                     │
  Session Confirmed       Client Notified
         │
  Session Delivered
         │
  ┌──────┴──────────────────┐
  │                         │
Completed               Cancelled
  │                         │
  ▼                         ▼
Client Rates            Refund Process
Therapist Notes
Earnings Credited
Payout (monthly)
```

---

## Business Impact

| Activity | Revenue / Operational Impact |
|---|---|
| **Payment approval speed** | Faster approvals = higher client satisfaction = more repeat bookings |
| **Session completion rate** | Every completed session = commission income |
| **No-show rate** | High no-show rate = revenue leakage and therapist/client frustration |
| **Post-session reviews** | Higher review rates improve therapist directory trust |
| **Payout processing speed** | Slow payouts cause therapist attrition |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Payment fraud** | Fake screenshots to get free sessions | Manual admin review; cross-check transaction IDs |
| **Session not delivered** | Therapist no-show | Clear no-show policy; automatic client notification |
| **Earnings calculation error** | Commission miscalculated | Automated commission calculation with transparent breakdown |
| **Payout disputes** | Therapist disagrees with earnings credited | Transparent transaction log; formal dispute process |

---

## Recommendations

1. **Integrate a payment gateway** (JazzCash, Stripe) to automate payment verification and eliminate the screenshot review bottleneck.
2. **Implement automated session reminders** for both client and therapist 24 hours and 1 hour before each session.
3. **Build a session completion auto-trigger** that marks sessions as "Completed" automatically at the scheduled end time, reducing admin workload.
4. **Publish a clear cancellation and refund policy** that is visible to clients at the point of booking, reducing disputes.
5. **Add a no-show tracking system** that records instances of therapist or client non-attendance, enabling pattern detection and policy enforcement.
