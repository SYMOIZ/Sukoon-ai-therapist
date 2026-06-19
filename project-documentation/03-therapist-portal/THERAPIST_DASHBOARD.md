# Therapist Dashboard — Sukoon AI

**Section:** 03 — Therapist Portal  
**Document:** THERAPIST_DASHBOARD.md  
**Audience:** Therapists, Therapist Relations Team, Product Team

---

## Executive Summary

The Therapist Dashboard is the central control panel for all licensed therapists on the Sukoon AI platform. It provides a unified view of sessions, clients, earnings, notes, safety incidents, and administrative actions. This document describes every section of the Therapist Dashboard and its purpose.

---

## Purpose

To give therapists and the teams that support them a clear reference for every capability available through the Therapist Dashboard.

---

## Stakeholders

- Active therapists (primary users)
- Therapist relations team (training and support)
- Product team (dashboard design decisions)
- Clinical team (oversight features)

---

## Dashboard Sections

The Therapist Dashboard is organized into multiple views accessible through a navigation sidebar. The active view is selected using the `therapist-[view]` navigation pattern.

---

## Section 1: Overview

### What It Shows
The **Overview** is the landing screen when a therapist logs in. It displays:
- Total session count (all time)
- Upcoming confirmed sessions (next 7 days)
- Recent notifications
- Unread direct messages count
- Current earnings balance
- Rating summary
- Any pending safety incidents requiring attention

### Purpose
Gives therapists a complete snapshot of their practice state at a glance. Everything critical is surfaced here so therapists can prioritize their day without navigating multiple sections.

---

## Section 2: Clients (Client Management)

### What It Shows
A list of all clients connected to the therapist, including:
- Client name and profile picture
- Connection status (Active, Disputed, Ended)
- Number of completed sessions
- Last session date
- Meeting link (if applicable)
- Chat expiry date (for time-limited direct messaging)

### Actions Available
- View detailed client profile
- Navigate to direct message thread
- Log a safety incident for a specific client
- View session history with the client

### Business Significance
This section is the therapist's primary client relationship management view. It mirrors the function of a patient roster in a traditional clinical setting.

---

## Section 3: Calendar (Schedule Management)

### What It Shows
A calendar view of the therapist's available and booked slots.

### What Therapists Can Do
- Add new available time slots (date, time, duration, session type)
- View all upcoming booked sessions with client names
- See slot status: available, booked, pending, cancelled
- Block unavailable time periods

### Session Slot Details
Each calendar slot includes:
- Date and time
- Duration (minutes)
- Status
- Client name (if booked)
- Session type (CBT, Mindfulness, General Talk, etc.)

---

## Section 4: Notes (Therapy Notes)

### What It Shows
All therapy notes written by the therapist, organized chronologically.

### Note Fields
Each note contains:
- **Title** — Short label for the session
- **Client** — Which client the note refers to
- **Date of note**
- **Note type** — Progress, Warning, or Needs Follow-up
- **Details** — Full clinical narrative
- **Next reminder date** — When to follow up with this client

### Purpose
Therapy notes provide clinical continuity — the ability to reference what was discussed in previous sessions and track a client's progress over time. Notes are also evidence of professional practice if questions arise about care quality.

---

## Section 5: Safety Incidents

### What It Shows
A log of all safety incidents reported by the therapist, with their current status.

### Incident Fields
- Client name
- Incident type (e.g., Suicide Risk, Harassment, Privacy Violation)
- Time of incident
- Description
- Status (Reported, Under Review, Resolved)

### Actions
- Log a new incident
- Update the status of an existing incident
- Add additional notes to an open incident

### Clinical Importance
Proper safety incident logging protects both the client and the therapist. It creates an auditable record of how serious situations were handled and enables the admin team to escalate appropriately.

---

## Section 6: Reviews

### What It Shows
All client reviews received by the therapist, in chronological order.

### Review Information
- Client name
- Star rating (1–5)
- Written comment
- Date of review
- Therapist reply (if provided)

### Actions
- Reply to a review
- View rating trend over time

### Business Value
Reviews are the primary trust signal for new clients browsing the directory. Therapists who actively manage and respond to reviews project professionalism and build faster booking pipelines.

---

## Section 7: Earnings (Financial View)

### What It Shows
The therapist's complete earnings picture:
- Current accumulated balance (unpaid earnings)
- Total lifetime earnings
- Per-session breakdown of earnings

### Transaction Log
Each earning entry shows:
- Date
- Session / booking reference
- Client
- Full session fee
- Therapist's portion (85%)
- Platform commission (15%)

### Payout Request
From the Earnings section, therapists can:
- Submit a payout request for their accumulated balance
- Specify the payment method (bank account details)
- Track payout status (Pending → Processed)
- View payout history

---

## Section 8: Profile (Public-Facing View)

### What It Shows
A preview of the therapist's public profile as clients see it.

### Editable Profile Fields
- Professional photo
- Biography
- Years of experience
- Specializations list
- Session types offered (audio, video, chat)
- Pricing (45-min, 60-min, 90-min sessions)
- Paid chat pricing (1-day, 7-day, 1-month access)
- Bank/payout details (private, for payout processing)
- Notification preferences

### Boost Management
Therapists can view their current boost status (basic or professional) and apply for a boost upgrade through the admin team.

### Pro Subscription
Therapists can see the status of their Pro Subscription and renew it as needed.

---

## Section 9: Notifications

### What It Shows
All notifications sent to the therapist:
- New booking alerts
- Payment verified notifications
- Client direct messages
- Safety incident updates
- Admin communications
- Broadcast messages

### Actions
- Mark notifications as read
- Navigate directly to the referenced booking, session, or incident

---

## Section 10: Settings

### Therapist-Specific Settings
- Language preference for the interface
- Tone preference
- Notification settings (email alerts, in-platform alerts)
- Dark mode toggle

---

## Navigation Structure

The Therapist Dashboard uses a side navigation panel with views accessible via the `therapist-[view]` navigation pattern:

| Navigation Key | Section |
|---|---|
| `therapist-overview` | Overview (default landing) |
| `therapist-clients` | Client management |
| `therapist-calendar` | Calendar and scheduling |
| `therapist-notes` | Therapy notes |
| `therapist-incidents` | Safety incidents |
| `therapist-reviews` | Client reviews |
| `therapist-earnings` | Financial view |
| `therapist-profile` | Profile management |
| `notifications` | Notifications |
| `settings` | Account settings |

---

## Process Flow

```
Therapist Logs In
       │
       ▼
Overview Dashboard (daily briefing)
       │
  ┌────┼────────────────────────────────────┐
  │    │                │                   │
  ▼    ▼                ▼                   ▼
Calendar  Clients     Notes          Earnings
  │         │            │               │
  ▼         ▼            ▼               ▼
Add/     View Client  Write/View     Review Balance
Update   Details     Therapy Notes  Submit Payout
Slots       │
            ▼
         DM Client
         Log Incident
```

---

## Business Impact

| Dashboard Section | Business Value |
|---|---|
| Overview | Reduces therapist confusion; increases daily engagement |
| Calendar | Enables session booking capacity |
| Notes | Clinical quality assurance; evidence of care |
| Safety Incidents | Legal protection; clinical safety |
| Reviews | Therapist directory trust signal |
| Earnings | Therapist retention through transparent, timely payment |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Dashboard complexity** | Too many sections overwhelm new therapists | Clear onboarding guide; default to Overview view |
| **Missed notifications** | Therapist doesn't see new bookings | Email notification fallback for critical events |
| **Incomplete notes** | Sessions without therapy notes | Prompt therapist to write notes after session completion |
| **Earnings disputes** | Therapist disagrees with commission deduction | Transparent transaction log; clear commission policy |

---

## Recommendations

1. **Add a dashboard summary card** that shows the therapist's performance metrics for the current month (sessions completed, earnings, rating, client retention).
2. **Implement note templates** that therapists can customize for common session types (anxiety review, CBT homework check-in, follow-up assessment).
3. **Create a mobile-optimized therapist dashboard** so therapists can check notifications and manage their calendar from their phone.
4. **Add calendar integration** (Google Calendar, Outlook) so therapists can see Sukoon bookings alongside their other commitments.
5. **Implement end-to-end encrypted messaging** for Direct Messages to ensure clinical communication confidentiality.
