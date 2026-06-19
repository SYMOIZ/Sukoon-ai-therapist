# Client Support — Sukoon AI

**Section:** 02 — Client App  
**Document:** CLIENT_SUPPORT.md  
**Audience:** Customer Support Team, Operations, Product Team

---

## Executive Summary

Sukoon AI provides clients with a structured support system for resolving platform-related issues, payment queries, booking disputes, and general inquiries. Support is handled through an in-platform ticketing system managed by the admin and support team. This document describes the full support experience from the client's perspective.

---

## Purpose

To document the complete client support process — how users raise issues, what types of issues are handled, how the support team responds, and how issues are resolved.

---

## Stakeholders

- Customer support team (primary operators of the support system)
- Admin team (oversight and escalation)
- Clients (the users raising tickets)
- Operations management (SLA monitoring)

---

## 1. Support Access

### How Clients Reach Support
Clients access support through the **Support** section in the main navigation. This page is available to any logged-in user.

### What the Support Page Offers
- A support ticket submission form
- Status updates on previously submitted tickets
- FAQs (recommended future addition)
- Direct contact information for urgent matters

---

## 2. Support Ticket Submission

### Ticket Categories

| Category | When to Use |
|---|---|
| **Payment Issue** | Payment made but subscription/session not activated, duplicate charge, or payment rejected incorrectly |
| **Booking Issue** | Session not confirmed, therapist didn't show, scheduling conflict |
| **Therapist Issue** | Concerns about therapist conduct, professionalism, or communication |
| **Technical Issue** | App errors, features not loading, voice/audio problems, login issues |
| **Account Verification** | Account flagged, suspended, or locked |
| **Refund Request** | Requesting a refund for a cancelled or undelivered session |
| **General Inquiry** | Any question that doesn't fit the above categories |

### Priority Levels

| Priority | Description |
|---|---|
| **Low** | Non-urgent inquiries and general questions |
| **Medium** | Issues affecting platform use but not blocking it |
| **High** | Urgent issues preventing platform access or involving payment |

### Ticket Fields
When submitting a ticket, users provide:
- **Issue type** (from the categories above)
- **Priority level** (Low, Medium, High)
- **Subject** (brief title of the issue)
- **Description** (full detail of the problem)
- **Attachment** — optional screenshot or image to support the report (stored as image_url)

---

## 3. Ticket Lifecycle

### Status Flow

```
Submitted → Open
           │
           ▼
      Admin Reviews
           │
      ┌────┴────┐
      │         │
   Investigating  Simple Resolution
      │                │
      ▼                ▼
  In Progress       Resolved
      │
      ▼
Admin Requests More Information
      │
      ▼
"Waiting for User"
      │
      ▼
User Responds
      │
      ▼
   Resolved → Closed
```

### Status Definitions

| Status | Meaning |
|---|---|
| **Open** | Ticket submitted, not yet reviewed |
| **In Progress** | Under active investigation by support team |
| **Waiting for User** | Support needs more information from the client |
| **Resolved** | Issue has been addressed |
| **Closed** | Issue confirmed resolved; ticket archived |

---

## 4. Ticket Messaging

### In-Ticket Communication
Each support ticket has a **message thread** where:
- Clients can provide additional details or respond to admin questions
- Support staff can reply with updates, requests, or resolutions
- The full conversation history is preserved

### Message Participants
Each message is tagged with:
- **Sender type** (user or admin)
- **Sender name**
- **Timestamp**

This creates a clear audit trail for every support interaction.

---

## 5. Admin Response

### What Support Agents See
Support agents see all open tickets in the **Admin Support Panel** with:
- Ticket category, priority, and current status
- Client's name and email
- Full description and any attached screenshots
- Message thread history

### Response Actions
Support agents can:
- Reply to the client through the ticket thread
- Change the ticket status
- Resolve the ticket with an explanation (`admin_response` field)
- Escalate urgent issues to senior admin or clinical team

---

## 6. Refund Requests

### Process
When a client submits a **Refund Request**:
1. The support agent reviews the original booking or subscription payment
2. The agent confirms whether the refund criteria are met
3. If approved: the refund is processed manually (current model) and the wallet balance or original payment method is credited
4. The ticket is updated with the refund decision and resolved

### Refund Criteria Examples
- Session cancelled by therapist without rescheduling
- Payment approved but session never occurred
- Duplicate payment error
- Payment made for wrong plan (within a correction window)

---

## 7. Special Case: Therapist Complaints

When a client submits a **Therapist Issue** ticket:
1. The support agent flags it for the clinical oversight team
2. The clinical team reviews any relevant session notes, safety incidents, or communications
3. If the complaint involves conduct violations, it may trigger a therapist suspension review
4. The client is kept informed of the investigation status without disclosing confidential therapist information

---

## 8. Special Case: Account Issues

When a client's account is suspended or flagged:
1. The client sees a suspension notice on login with the reason
2. They can submit a support ticket under **Account Verification** to appeal
3. The admin team reviews the account flag and the appeal
4. If the suspension is lifted, the client is notified and access is restored

---

## 9. Response Time Standards (Recommended SLAs)

| Priority | Target Response Time | Target Resolution Time |
|---|---|---|
| **High** | 4 hours | 24 hours |
| **Medium** | 24 hours | 72 hours |
| **Low** | 48 hours | 5 business days |

Note: These SLAs are recommendations. Formal SLA commitments should be established by the operations team.

---

## Process Flow

```
Client Identifies Issue
         │
         ▼
  Navigate to Support Section
         │
         ▼
Fill Out Support Ticket Form
(Category, Priority, Description, Attachment)
         │
         ▼
  Ticket Created → Status: "Open"
         │
         ▼
  Admin Team Reviews
         │
  ┌──────┴──────────────────┐
  │                         │
Simple Issue          Complex/Needs Info
  │                         │
  ▼                         ▼
Admin Responds        "Waiting for User"
  │                  (Admin requests more info)
  ▼                         │
Resolved                    ▼
                     User Responds
                            │
                            ▼
                   Admin Resolves / Escalates
                            │
                            ▼
                     Ticket Closed
```

---

## Business Impact

| Metric | Impact |
|---|---|
| **Support ticket resolution rate** | High resolution rate builds trust and reduces churn |
| **First-response time** | Fast initial response demonstrates platform professionalism |
| **Refund rate** | High refund rates signal booking or payment process problems |
| **Therapist complaint frequency** | Tracks therapist quality and highlights training needs |
| **Support team efficiency** | Ticket system enables measurement of support team performance |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Support overload** | High ticket volume without enough support staff | Set ticket categories to route automatically; hire based on volume |
| **Slow response** | Users escalate to social media if unresponsive | Enforce response SLAs; alert admin if ticket is unresponded for 24h |
| **Refund abuse** | Users requesting refunds for completed sessions | Clear refund policy; admin reviews session completion evidence |
| **Missing escalation** | High-priority ticket treated as low priority | Priority levels with color coding in admin panel |

---

## Recommendations

1. **Publish a public FAQ** that reduces ticket volume by addressing the most common questions before users need to raise tickets.
2. **Add a live chat option** for high-priority issues during business hours.
3. **Implement automated ticket routing** that assigns tickets to the right team based on category (finance team gets Payment Issues, clinical team gets Therapist Issues, etc.).
4. **Create a ticket escalation chain** with clearly defined criteria for when a ticket moves from support agent → senior support → operations manager → clinical lead.
5. **Add CSAT surveys** (Customer Satisfaction) that automatically send after a ticket is resolved, tracking support quality over time.
