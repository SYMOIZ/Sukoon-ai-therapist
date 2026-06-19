# Phase 1 Roadmap — Sukoon AI

**Section:** 09 — Future Roadmap  
**Document:** PHASE_1.md  
**Audience:** Founders, Product Team, Investors, Operations Team

---

## Executive Summary

Phase 1 represents the platform's immediate operational priorities — the improvements that must be made to the current platform to establish it as a reliable, scalable, and commercially viable service. Phase 1 focuses on eliminating the most significant operational bottlenecks, strengthening security and safety, and building the foundational infrastructure needed to support growth. Most Phase 1 items are not new features but essential improvements to what already exists.

---

## Purpose

To define the immediate next steps for the Sukoon AI platform — what needs to be built, fixed, or strengthened in the near term to move from early-stage product to a production-ready, commercially sustainable service.

---

## Stakeholders

- Founders (priority decisions and resource allocation)
- Product team (implementation)
- Operations team (operational readiness)
- Investors (visibility into how their investment will be deployed)

---

## Timeline Target

Phase 1: **0–6 months from launch**

---

## 1. Payment Gateway Integration (Highest Priority)

### Current State
All payments (session bookings and subscriptions) are processed manually — clients upload screenshots and transaction IDs; admins verify each one individually.

### Why It's Critical
- Manual verification creates significant admin workload at scale
- Payment delays frustrate clients and therapists
- No automated recurring billing for subscriptions
- Manual process is a bottleneck that will break under growth

### What to Build
- Integrate a Pakistani payment gateway (**JazzCash**, **EasyPaisa**, or **Stripe** for card payments)
- Automate session payment collection and confirmation
- Automate subscription payment collection and activation
- Provide users with instant payment confirmation rather than waiting for admin review

### Business Impact
- Eliminates the most significant operational bottleneck
- Increases session booking conversion (fewer drop-offs during checkout)
- Enables subscription auto-renewal (increases recurring revenue)
- Reduces admin workload by 50%+ (estimate)

---

## 2. Two-Factor Authentication (2FA) for Admin Accounts

### Current State
Admin accounts use email/password only. No 2FA is in place.

### Why It's Critical
Admin accounts have access to all user data, financial records, and platform controls. A compromised admin account is a catastrophic security failure.

### What to Build
- Mandatory 2FA for all accounts with admin access
- TOTP-based (Authenticator app) or SMS OTP implementation
- Force 2FA enrollment on next login for existing admin accounts
- New admin accounts require 2FA before accessing the panel

---

## 3. Admin Audit Logging

### Current State
No systematic log exists of which admin performed which action and when.

### Why It's Critical
Without audit logs, there is no accountability for admin actions. Cannot investigate data access claims, payment errors, or misuse.

### What to Build
- Log every sensitive admin action (account status change, payment verification, payout processing, data access) with: Admin ID, action, target (user/session/payment ID), timestamp
- Audit log viewer in the Admin Dashboard (filterable by admin, action type, date)
- Audit log retention: 3 years minimum

---

## 4. Automated Session and Subscription Reminders

### Current State
No automated reminders are sent to users before their sessions or before their subscription expires.

### Why It's Critical
- No-shows are costly (lost session revenue; therapist time wasted)
- Subscription lapses are a revenue leak (users forget to renew)

### What to Build
- Session reminder notifications: 24 hours before + 1 hour before
- Subscription expiry reminders: 7 days before + 1 day before + day of expiry
- Both in-app notification and email

---

## 5. Email Notification System

### Current State
All notifications are in-app only. Users who are not opening the app miss important notifications.

### Why It's Critical
- Session confirmations, payment updates, and payout completions are time-sensitive
- Users may not open the app daily
- Subscription renewal reminders need to reach disengaged users

### What to Build
- Transactional email integration (SendGrid or AWS SES recommended)
- Email templates for: booking confirmation, payment approved/rejected, payout processed, subscription expiring, account suspended/reinstated
- User preference for email notifications (opt-out only for non-critical)

---

## 6. Crisis-Certified Therapist Roster

### Current State
Crisis certification is tracked as a flag on the therapist profile, but there is no formal on-call roster or coverage requirement.

### Why It's Critical
Crisis detection alerts must reach a qualified human rapidly. Without guaranteed coverage, alerts may go unresponded for hours.

### What to Build
- Define minimum coverage: at least 2 crisis-certified therapists reachable at all times
- Create an on-call schedule for crisis-certified therapists
- Implement automatic escalation if alert goes unresponded beyond the 2-hour SLA

---

## 7. Urdu Language AI Support

### Current State
The AI operates in English only. The majority of the target user base in Pakistan communicates in Urdu or code-switches between English and Urdu.

### Why It's Critical
An AI that cannot engage meaningfully in Urdu excludes a large portion of the potential market.

### What to Build
- Test and optimize Gemini for Urdu-language conversations
- Add Urdu text input support in the AI chat interface
- Translate the AI system prompt for Urdu-mode interactions
- Test with native Urdu speakers for cultural and linguistic accuracy

---

## 8. Mobile App (iOS and Android)

### Current State
Sukoon AI is a web application. There is no dedicated mobile app.

### Why It's Critical
Mental health support is a mobile-first use case. Users need access on their phone, in their daily moments of distress, not just on a desktop.

### What to Build
- Native iOS and Android app (React Native recommended for code sharing with web frontend)
- Push notifications enabled on mobile
- App Store and Google Play listing

---

## 9. Data Retention and Deletion Policy Implementation

### Current State
No automated data retention or deletion processes exist. Data accumulates indefinitely.

### Why It's Critical
Privacy regulations and responsible data governance require defined retention limits. Accumulating unnecessary data increases breach risk and liability.

### What to Build
- Define retention periods per data category (as per DATA_HANDLING.md recommendations)
- Implement automated deletion jobs for expired data
- Account deletion request process (support ticket → verified deletion)

---

## Phase 1 Priority Summary

| Priority | Initiative | Timeline |
|---|---|---|
| P0 | Payment gateway integration | Month 1–2 |
| P0 | 2FA for admin accounts | Month 1 |
| P1 | Admin audit logging | Month 1–2 |
| P1 | Automated reminders (session + subscription) | Month 2 |
| P1 | Email notification system | Month 2 |
| P1 | Crisis therapist on-call roster | Month 1 |
| P2 | Urdu language AI | Month 3–4 |
| P2 | Mobile app | Month 3–6 |
| P2 | Data retention implementation | Month 3–4 |

---

## Process Flow (Phase 1 Planning)

```
Phase 1 Prioritization Meeting
        │
        ▼
Assign Engineering Capacity to P0 Items (payment gateway, 2FA)
        │
        ▼
P0 Items Live (Month 1–2)
        │
        ▼
P1 Items Enter Development (Month 2)
        │
        ▼
P1 Items Live (Month 2–3)
        │
        ▼
P2 Items Planned and Resourced
        │
        ▼
Phase 1 Review (Month 6) → Gate to Phase 2
```

---

## Business Impact

| Phase 1 Item | Business Impact |
|---|---|
| **Payment gateway** | 50%+ reduction in admin payment workload; higher conversion rate |
| **Admin 2FA** | Critical security protection |
| **Email notifications** | Reduced churn; improved user engagement |
| **Crisis therapist roster** | Clinical safety compliance |
| **Urdu AI** | Significantly expanded addressable market |
| **Mobile app** | Access growth; engagement improvement |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Payment gateway integration complexity** | Integration takes longer than expected | Budget 8 weeks; choose well-documented provider |
| **Mobile app scope creep** | Feature additions delay launch | Strict MVP scope for v1 mobile app |
| **Urdu AI quality** | Gemini Urdu performance unsatisfactory | Test thoroughly before public release |
| **Phase 1 resource constraints** | Small team cannot execute all items simultaneously | Strict prioritization; P0 items before P2 items |

---

## Recommendations

1. **Begin payment gateway integration immediately** — this is the Phase 1 item with the highest business impact and should be the first development sprint.
2. **Enable 2FA for admin accounts within the first week of production** — this is a security emergency relative to the current state and should not wait for a formal sprint.
3. **Define Phase 1 success metrics before starting** — what does success look like at the end of Month 6? (e.g., payment verification fully automated, mobile app launched, email notifications live)
4. **Hire a dedicated mobile developer** if the in-house team does not have native mobile experience — the mobile app is too important for the long-term to be delayed by skill gaps.
5. **Communicate Phase 1 progress to therapists and early users** — building in public (sharing what's coming) creates anticipation and reinforces the platform's commitment to improvement.
