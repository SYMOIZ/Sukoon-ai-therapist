# Customer Support Operations — Sukoon AI

**Section:** 07 — Operations  
**Document:** CUSTOMER_SUPPORT.md  
**Audience:** Support Team, Operations Manager, Admin Team, Customer Experience Lead

---

## Executive Summary

Customer support at Sukoon AI is the frontline of user trust and retention. It encompasses every formal interaction between the platform and its users outside of the core product features — from ticket handling to refund processing, from therapist complaint resolution to account recovery. This document defines how the support function is organized, how it operates day-to-day, what standards it upholds, and how it should evolve as the platform scales.

---

## Purpose

To establish the operational framework for customer support at Sukoon AI — covering team structure, daily operations, communication standards, escalation processes, and performance standards.

---

## Stakeholders

- Support team (front-line operators)
- Operations manager (oversight and performance)
- Admin team (account action authority)
- Clinical team (safety escalations)
- Finance team (refund processing)

---

## 1. Support Team Structure

### Current State
At the current platform scale, support is handled by the admin team who also manage therapist approvals, payments, and platform operations. There is no dedicated support specialist.

### Recommended Structure (As Platform Scales)
| Role | Responsibility |
|---|---|
| **Support Specialist (L1)** | First response on all tickets; handles standard queries |
| **Support Lead (L2)** | Complex tickets, escalations, refund approvals |
| **Operations Manager** | Performance oversight, policy decisions, reporting |
| **Clinical Liaison** | Safety escalations; consults on mental health-sensitive tickets |
| **Finance Contact** | Refund processing and billing dispute resolution |

---

## 2. Support Channels

### Primary Channel — In-Platform Ticket System
The main support channel is the **Sukoon AI Support Ticket System** accessible from within the app. All formal support requests should go through this channel.

### Advantages of In-Platform Tickets
- Full context about the user's account (visible to admin during review)
- Message threading preserves conversation history
- Status tracking visible to the user
- Integrates with account action capabilities (admin can act directly from the ticket view)

### Secondary Channels (Recommended)
As the platform scales:
- **Email support** — for users who cannot access the platform
- **WhatsApp business** — for initial inquiry response in Pakistan context
- **Phone support** — for critical or elderly users (planned future consideration)

---

## 3. Support Hours and Coverage

### Current Recommended Coverage
| Time | Coverage |
|---|---|
| **Business hours (9am–6pm, Mon–Sat)** | Full admin team available |
| **Evening hours (6pm–10pm)** | At least one on-call admin for critical alerts |
| **Night hours (10pm–9am)** | Crisis alert notifications only; no live support |
| **Sundays / Public Holidays** | Critical alerts only; ticket queue reviewed next business day |

### Future Target
- 16-hour coverage, 7 days/week for ticket support
- 24/7 coverage for crisis alerts

---

## 4. Daily Support Operations

### Morning Routine (Start of Business Day)
1. Review all **Open** tickets received overnight
2. Prioritize by: Critical → High → Medium → Low
3. Assign tickets to team members based on category expertise
4. Respond to any Critical or High priority tickets immediately

### Midday Check
- Review In Progress tickets for updates
- Send replies waiting for admin action
- Check escalated tickets for updates from the specialist teams

### End-of-Day Routine
1. Confirm all Critical and High priority tickets have had a response
2. Update ticket statuses (move to Awaiting Response or Resolved as appropriate)
3. Review tomorrow's open ticket queue
4. Send daily summary to the operations manager

---

## 5. Communication Standards

### Tone and Language
All support communications must be:
- **Warm and human** — not robotic or formulaic
- **Empathetic** — recognizing that users may be in distress
- **Clear and direct** — avoiding jargon
- **Solution-focused** — always moving toward resolution
- **Professional** — no informal slang or emoji in formal communications

### Response Templates
Pre-written templates should be created for common ticket types to ensure consistency and speed. Templates must be personalized with the user's name and specific details before sending — they are starting points, not copy-paste responses.

### Languages
Support is primarily conducted in **English and Urdu**. All team members should be proficient in both.

---

## 6. Escalation Thresholds

| Situation | Escalation Target | Timeframe |
|---|---|---|
| User expresses suicidal ideation in a ticket | Clinical supervisor → Crisis protocol | Immediately (within 15 minutes) |
| Legal threat or formal complaint | Operations Manager + legal advisor | Within 2 hours |
| Fraudulent payment claim | Finance team + Super Admin | Within 4 hours |
| Therapist misconduct allegation | Clinical supervisor + Admin lead | Within 4 hours |
| Platform outage reports | Technical team | Immediately |
| Unresolved ticket over 72 hours | Support Lead / Manager | Same day |

---

## 7. Refund Policy (Support Team Reference)

### Eligible Refunds
- Session not delivered (therapist no-show, cancellation without rebooking)
- Payment approved for a session that was then cancelled by the platform
- Duplicate payment for the same session
- Technical error causing double charge

### Non-Eligible Refunds
- Completed sessions the client found unsatisfactory (standard outcome; addressed through complaint process, not refund)
- Subscription fees for plans already used
- Cancellations made after a session has been confirmed and not cancelled in advance

### Refund Process
1. Ticket categorized as "Refund Request"
2. Support Lead verifies eligibility against policy
3. Finance team processes refund if approved
4. User notified of outcome with timeline

---

## 8. Feedback Loop to Product Team

Support tickets are a rich source of product improvement signals. The support team should:
- Tag tickets with recurring themes (e.g., "UI confusion," "payment friction," "feature request")
- Compile a **monthly support insights report** summarizing:
  - Top 5 recurring issues
  - Feature requests mentioned more than 3 times
  - Critical failures that affected multiple users
- Share this report with the product team at the monthly review

---

## Process Flow (Support Daily Cycle)

```
Start of Day
    │
    ▼
Review Overnight Tickets → Prioritize
    │
    ▼
Assign to Team Members
    │
    ▼
First Responses Sent (within SLA)
    │
    ▼
Investigate → Act (refund / account action / information)
    │
    ▼
Follow Up (await user confirmation)
    │
    ▼
Close Resolved Tickets
    │
    ▼
End-of-Day Summary
    │
    ▼
Escalations Tracked and Outstanding Items Noted
```

---

## Business Impact

| Support Excellence | Business Impact |
|---|---|
| **Fast first response** | User satisfaction; reduced negative reviews |
| **Fair refund policy** | Trust in platform; repeat usage |
| **Empathetic tone** | Particularly important for mental health platform users |
| **Safety escalation speed** | Clinical responsibility; liability management |
| **Product feedback loop** | Reduces recurring issues over time |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Slow response times** | User frustration; public complaints | Enforce SLA; monitor response time daily |
| **Inconsistent policies** | Different agents give different answers | Policy documentation; case precedent library |
| **Agent burnout** | Mental health platform support is emotionally taxing | Regular team check-ins; rotation of emotionally challenging cases; access to counseling |
| **Safety ticket missed** | Crisis ticket not escalated | Keyword flagging in ticket system for safety escalation; mandatory training |
| **Ticket queue overwhelm** | Volume exceeds team capacity | Hiring plan tied to user growth milestones |

---

## Recommendations

1. **Create a formal Support Handbook** — a documented reference covering all policies, response templates, escalation procedures, and communication standards. New team members should be onboarded through this handbook.
2. **Implement a satisfaction survey** — 2–3 questions sent to users after ticket closure, measuring support quality and identifying gaps.
3. **Invest in mental health training for the support team** — the team interacts with users who may be in emotional distress; equipping them with basic psychological first aid skills improves response quality and protects the team members.
4. **Build a ticketing knowledge base** — an internal searchable library of previous ticket resolutions that agents can reference for consistency.
5. **Review SLA adherence weekly** — a weekly 15-minute team review of response time metrics against SLA targets keeps the team accountable without becoming bureaucratic.
