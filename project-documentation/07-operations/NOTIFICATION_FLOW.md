# Notification Flow — Sukoon AI

**Section:** 07 — Operations  
**Document:** NOTIFICATION_FLOW.md  
**Audience:** Operations Team, Product Team, Admin Team

---

## Executive Summary

The notification system is the primary communication channel between the Sukoon AI platform and its users (clients and therapists). Notifications inform users of important platform events — booking confirmations, payment approvals, new messages, risk alerts (for admins), and admin broadcasts. Understanding the notification flow ensures that all stakeholders know when users are informed, how they are informed, and what to do if notification-related issues arise.

---

## Purpose

To document all notification types on the Sukoon AI platform, the events that trigger them, who receives them, and how the notification system is managed.

---

## Stakeholders

- Product team (notification feature development)
- Operations team (governance and monitoring)
- Admin team (broadcast sender and notification recipient for risk alerts)
- Clients and therapists (notification recipients)

---

## 1. Notification Channels

### In-App Notifications
All standard notifications appear in the **Notifications section** of the app (accessible from the top navigation). Notifications:
- Display in real time if the user is active
- Are stored in the notification inbox for users who are not active at the time of sending
- Show a red badge count on the notification icon when unread notifications exist
- Can be marked as read individually or all at once

### Email Notifications (Future / Recommended)
For critical events (especially booking confirmations, payment approved, and payout processed), email notifications should be sent as a secondary channel. Users who are not regularly opening the app will still receive important updates through email.

---

## 2. Client Notifications

The following events generate in-app notifications to clients:

| Event | Notification Content |
|---|---|
| **Registration confirmed** | Welcome message; invitation to start first AI chat |
| **Subscription activated** | Plan name, start date, expiry date, features unlocked |
| **Subscription expiring soon** | Reminder 7 days and 1 day before expiry |
| **Subscription expired** | Access downgraded; renewal instructions |
| **Session booking submitted** | Confirmation that booking was received; payment under review |
| **Payment approved** | Session confirmed; session date and time |
| **Payment rejected** | Rejection reason; instructions to resubmit |
| **Session reminder** | 24 hours before scheduled session; 1 hour before |
| **Session completed** | Invitation to leave a review |
| **New direct message from therapist** | Message preview; link to DM thread |
| **Risk alert actioned** | (If admin assigns a crisis therapist) — "A care specialist has been assigned to you" |
| **Support ticket update** | Admin reply to their open support ticket |
| **Broadcast message** | Sent when admin broadcasts to all clients or all users |
| **New badge earned** | Gamification achievement notification |
| **Streak milestone** | Day streak achievement (e.g., "7-day streak!") |
| **Mood check-in reminder** | Daily nudge to complete their check-in |
| **Journal reminder** | Daily nudge to write in their journal |

---

## 3. Therapist Notifications

The following events generate in-app notifications to therapists:

| Event | Notification Content |
|---|---|
| **Application approved** | Approval message; instructions to complete profile |
| **Application rejected** | Rejection message with reason |
| **New session booking received** | Client name, session date, session type, status: Pending Payment |
| **Booking payment approved** | Session confirmed; client name and date |
| **Booking payment rejected** | Session will not proceed; slot released |
| **Session reminder** | 24 hours before scheduled session |
| **Session marked completed** | Prompt to write therapy notes |
| **New direct message from client** | Message preview; link to DM thread |
| **Payout processed** | Amount received; payout date |
| **Payout request rejected** | Reason; instructions to resubmit |
| **New client review** | Client has left a review; link to respond |
| **Safety incident update** | Status change on a reported safety incident |
| **Risk assignment** | "You have been assigned as a crisis therapist for [client]" |
| **Broadcast message** | Sent when admin broadcasts to all therapists or all users |
| **Boost status update** | Boost tier changed |

---

## 4. Admin Notifications

The following events generate in-app notifications to admins:

| Event | Notification Content |
|---|---|
| **New therapist application** | Therapist name; link to review application |
| **New session payment submission** | Client name, booking ID, amount; link to verify payment |
| **New subscription payment submission** | Client name, plan; link to activate |
| **New payout request** | Therapist name, amount requested |
| **New support ticket** | Ticket subject, category, priority |
| **Risk alert created** | User name, alert message; link to assign crisis therapist |
| **Safety incident reported** | Therapist name, incident type; link to review |

---

## 5. Notification Priority Levels

Not all notifications are equal in urgency. The platform treats notifications in three priority levels:

| Priority | Events | Delivery |
|---|---|---|
| **Critical** | Crisis risk alert; safety incident; platform outage | Immediate; may trigger push notification + email |
| **High** | Payment approved/rejected; booking confirmation; payout processed | Real-time in-app; email recommended |
| **Standard** | Session reminders; new messages; badge earned; broadcast | In-app; no special urgency |

---

## 6. Notification Preferences

### What Users Can Control
Users can manage notification preferences in their **Settings** section:
- Toggle on/off: email notifications
- Toggle on/off: mood check-in reminders
- Toggle on/off: journal reminders
- Toggle on/off: session reminders
- Other preferences configurable per user

### What Cannot Be Disabled
- Critical safety notifications (risk alerts actioned, crisis therapist assigned)
- Booking confirmation and payment status updates (these are core transactional notifications)
- Account status changes (suspension, reinstatement)

---

## 7. Broadcast Notifications

Admin broadcast messages are sent through the notification system as a special message type:

| Broadcast Audience | Who Receives It |
|---|---|
| **All Users** | Every client and therapist on the platform |
| **Clients Only** | All registered client accounts |
| **Therapists Only** | All approved therapist accounts |

Broadcasts appear in the notification inbox with a distinct label ("Platform Update," "Important Notice," etc.). Broadcast history is stored in the admin panel.

---

## 8. Notification Delivery Failure

If a notification fails to deliver (e.g., due to a system error):
- The failure is logged
- A retry is attempted
- If retries fail, the admin team is alerted
- For Critical notifications, manual follow-up (email or direct contact) may be required

---

## Process Flow (Notification Lifecycle)

```
Platform Event Occurs
(e.g., payment approved, new message, risk alert)
        │
        ▼
Notification Created in Database
(Type, Recipient, Content, Priority, Timestamp)
        │
        ▼
User Active?
  ├── YES → Notification displayed immediately (real-time)
  └── NO  → Notification stored in inbox
             Red badge updated on notification icon
             Email sent (if High/Critical priority)
        │
        ▼
User Opens Notification
        │
        ▼
Notification Marked as Read
        │
        ▼
User Takes Action (if applicable):
  ├── Clicks through to booking
  ├── Opens support ticket
  ├── Views assigned therapist
  └── Or dismisses
```

---

## Business Impact

| Notification Feature | Business Impact |
|---|---|
| **Timely payment notifications** | Reduces anxiety for clients waiting on approval |
| **Session reminders** | Reduces no-shows; increases session completion rate |
| **Subscription renewal reminders** | Reduces involuntary churn from forgotten renewals |
| **Risk alert notifications** | Speeds up admin response to safety events |
| **New message notifications** | Keeps DM conversations active; improves therapist-client relationship |
| **Gamification notifications** | Drives daily habit formation and retention |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Notification overload** | Too many notifications causes users to mute the app | Thoughtful notification grouping; user preference controls |
| **Critical notifications missed** | Admin not seeing risk alerts | Push notifications for Critical events; on-call coverage |
| **Notification delivery failure** | System error prevents delivery | Retry logic; failure logging; manual escalation for critical |
| **Broadcast sent to wrong audience** | All clients receive therapist-only message | Broadcast preview and confirmation before sending |
| **No email fallback** | Users away from app miss important notifications | Implement email notification for High and Critical events |

---

## Recommendations

1. **Implement push notifications** (mobile app) and email notifications as additional delivery channels for High and Critical priority events — in-app only is insufficient for time-sensitive matters.
2. **Batch low-priority notifications** — rather than sending individual notifications for each badge earned or each journal reminder, group them into a daily digest to reduce notification fatigue.
3. **Build a notification preference center** — a clear, organized settings page where users can see and control exactly which notifications they receive, with clear descriptions of what each type is.
4. **Monitor notification open rates** — tracking which notification types users actually open vs. dismiss provides insight into which communications are valuable and which are noise.
5. **Create a notification audit trail** — a log of every notification sent (type, recipient, timestamp, delivery status) accessible to admins for support ticket investigation.
