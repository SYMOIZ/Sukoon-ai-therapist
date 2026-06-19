# Daily Operations — Sukoon AI

**Section:** 07 — Operations  
**Document:** DAILY_OPERATIONS.md  
**Audience:** Admin Team, Operations Manager, Support Team, Finance Team

---

## Executive Summary

Daily operations on Sukoon AI is the ongoing routine through which the platform is kept running, users are served, therapists are supported, payments are processed, and safety is maintained. Unlike features or policies that are set once, daily operations must be performed consistently every working day. This document defines the daily operating rhythm of the Sukoon AI team — what must be done, by whom, and in what priority order.

---

## Purpose

To define the standard operating rhythm for the Sukoon AI team — ensuring that all critical daily tasks are performed on time, responsibilities are clear, and nothing falls through the cracks as the platform scales.

---

## Stakeholders

- Admin team (primary operators)
- Operations manager (oversight)
- Finance team (payment and payout tasks)
- Support team (ticket management)
- Clinical team (safety monitoring)

---

## 1. Priority Framework

All daily tasks are classified by the impact of delay:

| Priority | Description | Response Target |
|---|---|---|
| **P0 — Critical** | Safety-related; user in immediate distress | Within 1 hour |
| **P1 — High** | Revenue-affecting; booking/payment delays | Within 4 hours |
| **P2 — Medium** | Service quality; support tickets; approvals | Within 24 hours |
| **P3 — Standard** | Administrative; reporting; maintenance | Within 48 hours |

---

## 2. Daily Task Checklist

### Start-of-Day Tasks (9:00 AM — 10:00 AM)

| Task | Priority | Owner |
|---|---|---|
| Review all new Risk Alerts from the previous night | P0 | Admin on duty |
| Review all new Critical support tickets | P0 | Support Lead |
| Check for new therapist applications | P2 | Admin Lead |
| Review new session payment submissions | P1 | Finance Team / Admin |
| Review new subscription payment submissions | P1 | Finance Team / Admin |
| Review new payout requests from therapists | P1 | Finance Team |
| Check overnight new support tickets | P2 | Support Team |
| Check new therapist complaint tickets | P1 | Support Lead |

### Core Hours Tasks (10:00 AM — 4:00 PM)

| Task | Priority | Owner |
|---|---|---|
| Process pending payment verifications | P1 | Admin |
| Review and respond to support tickets (in priority order) | P2 | Support Team |
| Process outstanding payout requests | P1 | Finance Team |
| Review therapist applications (any pending from previous days) | P2 | Admin Lead |
| Monitor Risk Alert dashboard for new alerts | P0 | Admin on duty |
| Assign crisis therapist to any unassigned Risk Alerts | P0 | Clinical Admin |
| Review safety incidents logged by therapists | P1 | Clinical Admin |
| Reply to any user or therapist DMs requiring admin response | P2 | Admin Team |

### End-of-Day Tasks (4:00 PM — 6:00 PM)

| Task | Priority | Owner |
|---|---|---|
| Confirm all P0 risk alerts have been actioned | P0 | Admin Lead |
| Confirm all P1 payment verifications are processed or in queue | P1 | Finance Team |
| Update outstanding support ticket statuses | P2 | Support Team |
| Send daily operations summary to Operations Manager | P3 | Admin Lead |
| Confirm on-call admin is available for evening risk alert monitoring | P0 | Operations Manager |
| Check whether any scheduled broadcasts need to go out | P2 | Admin Lead |

---

## 3. Weekly Tasks

Performed at the start or end of each week:

| Task | Timing | Owner |
|---|---|---|
| **Process batch payout run** (if bi-weekly cycle) | Mondays / 1st and 15th | Finance Team |
| **Review therapist application backlog** | Monday mornings | Admin Lead |
| **Pull weekly support metrics** (ticket volume, response time) | Fridays | Support Lead |
| **Review Risk Alert resolution status** | Fridays | Clinical Admin |
| **Review inactive therapist list** (no calendar slots set) | Mondays | Admin Team |
| **Plan any scheduled broadcasts** for the coming week | Monday mornings | Operations Manager |

---

## 4. Monthly Tasks

Performed in the first week of each month:

| Task | Owner |
|---|---|
| **Generate Monthly Financial Report** | Finance Team |
| **Generate Monthly Safety Report** | Clinical Admin |
| **Generate Monthly Support Report** | Support Lead |
| **Review therapist quality metrics** (ratings, session volume, incidents) | Admin Lead |
| **Review subscription renewal health** (expired vs. renewed) | Finance Team |
| **Review AI usage costs** (Gemini API consumption) | Technical Team / Operations |
| **Content review** (any system prompt or keyword list updates needed?) | Clinical Advisor + Admin Lead |
| **Share reports with Executive Team** | Operations Manager |

---

## 5. On-Call Responsibility

The platform must have at least one admin on call at all times for:
- Crisis risk alert monitoring (evenings and weekends)
- Critical support escalations
- Payment processing emergencies

On-call admin responsibilities:
- Monitor risk alert notifications on mobile
- Act on new risk alerts within 1 hour (assign crisis therapist or escalate)
- Available by phone for Critical issues

The on-call rota should be formalized as the team grows, with clear handover procedures between shifts.

---

## 6. New User Onboarding Support

Every day, new users register on the platform. While onboarding is largely self-service, the admin team supports it by:
- Monitoring for users who register but do not complete their first AI chat (within 3 days) → send a nudge notification
- Monitoring for users who get stuck (support ticket: "can't log in", "payment not processing") → fast response
- Ensuring the platform status is healthy so new users have a good first experience

---

## 7. Platform Health Monitoring

Daily operational awareness of platform technical health:

| Health Check | Frequency | Responsible |
|---|---|---|
| AI chat is functioning (test prompt) | Daily | Admin on duty |
| Platform login is working | Daily | Admin on duty |
| Payment submission form is working | Daily | Admin on duty |
| Support ticket system is receiving submissions | Daily | Support Team |
| Risk alert notifications are being generated | Weekly (test) | Clinical Admin |

If any check fails, escalate to the technical team immediately.

---

## 8. Communication Norms

### Internal Communication
- Daily admin team sync (15-minute stand-up) — What's in queue? Any blockers? Any P0 items?
- Operations manager available for escalations during business hours
- Shared task tracker for in-progress items (recommended: Trello, Notion, or any shared tool)

### External Communication
- Admins respond to support tickets; no unsolicited contact with users outside the ticket system
- Therapist communications go through the platform notification system or through admin DMs (for operational matters)

---

## Process Flow (Standard Operational Day)

```
9:00 AM — Start of Day Review
  ├── Risk Alerts: P0 reviewed first
  ├── Payment Queue: P1 reviewed
  └── Support Tickets: Triaged

10:00 AM — 4:00 PM — Core Hours
  ├── Payment Verifications Processed
  ├── Support Tickets Responded to (by SLA)
  ├── Payout Requests Handled
  ├── Risk Alerts Actioned (ongoing monitoring)
  └── Therapist Applications Reviewed

4:00 PM — 6:00 PM — End of Day
  ├── All P0s confirmed resolved
  ├── P1 payments queue confirmed
  ├── Daily summary sent to Manager
  └── On-call handover confirmed

Evening / On-Call
  └── Risk Alert monitoring only
      Critical escalations handled
```

---

## Business Impact

| Operational Discipline | Business Impact |
|---|---|
| **Same-day payment verification** | Session confirmed quickly; client and therapist satisfied |
| **24-hour support response** | User trust; reduced churn |
| **Real-time risk alert response** | Clinical safety; liability management |
| **Weekly payout processing** | Therapist retention; supply-side health |
| **Daily platform health checks** | Early detection of issues before users are widely affected |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Overloaded admin team** | Too many tasks; quality drops | Hire ahead of growth; prioritize ruthlessly |
| **No on-call coverage** | Evening crisis alert missed | Formal on-call rota; mandatory notification setup |
| **Task list not followed** | Ad-hoc work pushes aside structured tasks | Daily stand-up; shared task tracker |
| **Bottleneck on single person** | One admin handling everything | Cross-training; documented procedures; team redundancy |
| **No monitoring of platform health** | Technical issues go undetected until users complain | Daily health checks; automated uptime monitoring |

---

## Recommendations

1. **Formalize the daily checklist** as a shared document or task tracker item that gets checked off each day — providing operational accountability and a clear record of what was done.
2. **Implement automated uptime monitoring** (e.g., Uptime Robot, Better Uptime) that alerts the technical team immediately if any critical platform endpoint goes down.
3. **Hold a weekly 30-minute operations review** — Admin Lead, Finance Lead, and Support Lead review the week's key metrics and outstanding issues together.
4. **Create an operations playbook** — for each major task category (payment verification, payout processing, risk alert response), write a step-by-step procedure so that any team member can pick it up correctly.
5. **Document and review on-call incidents** — every on-call escalation should be logged with: what happened, how it was handled, and any follow-up needed. Monthly review of these logs identifies recurring issues.
