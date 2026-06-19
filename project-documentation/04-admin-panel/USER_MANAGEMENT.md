# User Management — Sukoon AI

**Section:** 04 — Admin Panel  
**Document:** USER_MANAGEMENT.md  
**Audience:** Admins, Moderators, Operations Team, Compliance Team

---

## Executive Summary

User Management in Sukoon AI gives the admin team full oversight and control over all registered client accounts. Admins can view, search, filter, and act on client accounts — including suspending, banning, or reinstating users — based on reported issues, policy violations, or safety concerns. This document covers every aspect of how the admin team manages the client user base.

---

## Purpose

To define how admin staff monitor, manage, and take action on client user accounts — including account statuses, verification, and disciplinary actions.

---

## Stakeholders

- Platform admins and moderators (daily management)
- Compliance team (policy enforcement)
- Clinical team (safety-related account actions)
- Client support team (account assistance)

---

## 1. Viewing the User List

Admins access the user list from the **Users** section of the Admin Dashboard. This section shows all registered client accounts on the platform.

### Default View
The user list displays:
- Full name
- Email address
- Account status (Active, Suspended, Pending, Banned)
- Registration date
- Last active date
- Risk level (Low, Medium, High — based on AI-detected crisis signals)

### Pagination and Search
- Users are listed with pagination (large deployments may have thousands of accounts)
- Search by: name, email address, or user ID
- Filter by: account status, risk level, registration date range

---

## 2. User Account Statuses

| Status | Meaning | Who Sets It |
|---|---|---|
| **Active** | Normal account — full platform access | Default on registration |
| **Pending** | Account created but email not verified or onboarding not complete | System (automatic) |
| **Suspended** | Temporarily restricted — cannot log in | Admin |
| **Banned** | Permanently blocked from the platform | Admin |

### Status Lifecycle

```
Registration
    │
    ▼
 Pending (awaiting verification)
    │
Verified
    │
    ▼
 Active
    │
  ┌─┴──────────────────────┐
  │                         │
Violation              Policy breach
Reported               (severe)
  │                         │
  ▼                         ▼
Suspended               Banned
  │
Admin Review
  │
  ├── Reinstated → Active
  └── Escalated → Banned
```

---

## 3. Viewing a User's Profile

Clicking on a user record opens the **User Profile View**, which includes:

### Personal Information
- Full name, email, phone number (if provided)
- Registration date, last login date
- Account status

### Platform Activity
- Number of AI chat sessions
- Journal entry count
- Session bookings (list of all bookings)
- Current active therapist connection(s)
- Support tickets raised

### Risk Assessment
- Current risk level (set by AI crisis detection)
- Active risk alerts (if any)
- Safety incidents logged by their therapist (if any)

### Subscription
- Current subscription plan
- Plan expiry date
- Payment history

---

## 4. Account Status Actions

Admins can take the following actions on a user account:

### Suspend Account
- Temporarily prevents the user from logging in
- Must include a reason (displayed to the user if they attempt login)
- The account can be reinstated at any time by an admin
- All data is preserved during suspension

### Reinstate Account
- Reverses a suspension
- Account returns to "Active" status
- User receives a notification that their account has been reinstated

### Ban Account
- Permanently blocks the user from the platform
- Used for severe, repeated, or irreversible violations
- All active sessions are terminated
- User receives a ban notification with reason
- Data is retained for legal and compliance purposes

### Mark as Pending
- Can be used to require the user to re-verify their email or complete additional onboarding steps before accessing the platform

---

## 5. Account Deletion Policy

Clients may request account deletion through a support ticket. Admin must:
1. Verify the identity of the requester
2. Check if there are any active bookings, pending payouts, or open disputes linked to the account
3. If clear, mark the account for deletion
4. Remove personally identifiable information from the account record
5. Retain anonymized transaction data for financial compliance

Accounts with open disputes, pending payments, or safety incidents under investigation cannot be deleted until those matters are resolved.

---

## 6. Risk-Flagged Users

When the AI system detects crisis language in a user's chat, the user's risk level is elevated and a **Risk Alert** is created. In the User Profile view, admins can see:
- Current risk level (Low, Medium, High)
- History of risk alert events
- Whether a crisis therapist has been assigned

Admins can manually override the risk level in consultation with the clinical team.

---

## 7. Viewing User Chat and Journal Activity (Admin Access)

In cases where a risk alert requires clinical investigation, or a support dispute requires account history review, admins can access a limited view of the user's:
- AI chat history (including flagged messages)
- Journal entries (redacted for routine matters; full access for clinical investigations)

**Access to user chat and journal content is considered a sensitive action and should be:**
- Used only when there is a documented operational reason
- Recorded in admin audit logs
- Handled by authorized personnel only (clinical supervisor or Super Admin, not general moderators)

---

## 8. User Verification

### Email Verification
Standard email verification is required during registration. Unverified accounts cannot access the full platform.

### Phone Verification
Optional additional verification. If implemented, phone verification provides a secondary layer of identity confirmation and is used for account recovery.

### Manual Identity Verification
In cases of fraud or dispute, an admin can request that a user confirm their identity through the support ticket channel.

---

## 9. User Communication Channels

Admins can communicate with users through:

- **Broadcast Messages** — Platform-wide or targeted messages (all clients)
- **In-ticket Messages** — Replies to support tickets
- **Manual Notifications** — Direct notifications sent to a specific user

Admins do not have access to a user's private chat with the AI or their direct messages with therapists as a routine matter — only through escalated clinical review.

---

## Process Flow (Handling a Reported User)

```
Report Received (via support ticket or risk alert)
    │
    ▼
Admin Reviews User Profile
    │
    ▼
Review: AI chat activity, safety incidents, ticket history
    │
  ┌─┴──────────────────────┐
  │                         │
Minor Violation          Serious Violation
  │                         │
  ▼                         ▼
Warning / Suspend        Ban Account
  │                         │
  ▼                         ▼
User Notified           User Notified + Record Created
  │
  ▼
Admin Documents Action in Audit Log
```

---

## Business Impact

| Action | Business Relevance |
|---|---|
| **Fast suspension of bad actors** | Protects other users and therapists from harm |
| **Reinstatement process** | Allows recovery for users who made genuine mistakes |
| **Risk-level tracking** | Enables proactive safety management before incidents escalate |
| **Account deletion compliance** | Adherence to privacy regulations (GDPR-equivalent) builds user trust |
| **Audit trail** | Evidence of responsible platform governance for investors and regulators |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **False positive suspensions** | Innocent users suspended by mistake | Clear suspension criteria; easy reinstatement; appeal process |
| **Delayed action on bad actors** | Harmful users remain active too long | Priority alerts for high-risk accounts; SLA on report response |
| **Unauthorized data access** | Moderators viewing chat/journal without cause | Access permission tiers; audit logging |
| **GDPR non-compliance** | User data retained longer than necessary | Defined data retention policy; documented deletion procedure |

---

## Recommendations

1. **Implement an admin audit log** that records every account action (who took the action, what action, when, and against which account) — critical for governance accountability.
2. **Create a formal violation policy document** with clear criteria defining which behaviors result in warnings, suspension, or permanent bans.
3. **Build an in-platform appeal system** where suspended users can submit a reinstatement appeal through a structured form.
4. **Restrict journal and chat access** to Super Admin and Clinical Supervisor roles only, and require a documented reason to be logged before access is granted.
5. **Implement an automated account cleanup job** that flags accounts inactive for 12+ months, prompting either re-engagement outreach or data minimization.
