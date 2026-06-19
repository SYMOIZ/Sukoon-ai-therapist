# Therapist Onboarding — Sukoon AI

**Section:** 03 — Therapist Portal  
**Document:** THERAPIST_ONBOARDING.md  
**Audience:** Therapist Relations Team, Operations, Admins, Prospective Therapists

---

## Executive Summary

Licensed therapists join Sukoon AI through a structured application and verification process designed to ensure platform quality and clinical safety. From initial application to first active client, a therapist goes through five stages: application submission, document verification, admin review, profile activation, and client-facing onboarding. This document describes every step.

---

## Purpose

To provide a clear, complete reference for how therapists are recruited, verified, and activated on the Sukoon AI platform — ensuring consistent quality standards and a smooth experience for incoming clinical professionals.

---

## Stakeholders

- Therapist relations team (recruiting and onboarding)
- Admin team (application review and approval)
- Compliance team (license verification)
- Prospective therapists (understanding the process)

---

## 1. The Therapist Value Proposition

Before discussing the onboarding process, it is important to understand why licensed therapists join Sukoon AI:

- **Digital reach** — Access clients across the country and diaspora without a physical office
- **Flexible scheduling** — Set their own calendar and availability
- **Transparent earnings** — Earn 85% of every session fee (platform takes 15%)
- **Clinical tools** — Built-in note-taking, client management, and scheduling
- **Crisis support** — Platform handles crisis escalation so therapists can focus on clinical work
- **Boosted visibility** — Optional paid promotion to appear higher in the therapist directory

---

## 2. Application Submission

### How a Therapist Applies
A prospective therapist registers on the Sukoon AI platform and selects the **"Join as Therapist"** option (or equivalent in the Welcome Page flow). They complete a structured application form with the following fields:

| Field | Description |
|---|---|
| **Full Name** | Legal name as per professional license |
| **Email Address** | Professional contact email |
| **Phone Number** | Contact number |
| **Years of Experience** | Total years in clinical practice |
| **Specialization** | Primary area of expertise (e.g., Anxiety, CBT, Youth Counseling, Sleep CBT) |
| **License Number** | Official professional license identifier |
| **CV File** | Resume or curriculum vitae (uploaded document) |
| **Degree File** | Academic degree certificate (uploaded document) |

### Application Status After Submission
After submission, the application enters **"Pending"** status. The therapist's user account is also placed in **"Pending"** status, meaning they cannot operate as an active therapist until approved.

---

## 3. Document Verification

### What Is Verified
The admin team reviews the submitted documents for:

1. **License Number** — Cross-referenced with relevant licensing bodies (PMDC for Pakistan, relevant councils for other regions)
2. **Academic Degree** — Confirms appropriate clinical qualifications (psychology, psychiatry, counseling)
3. **CV / Resume** — Confirms experience claims match the application
4. **Professional Background** — Flags any inconsistencies or missing information

### Verification Responsibility
The admin team is responsible for document review. For complex licensing verification, the clinical oversight team or an external compliance partner may be involved.

---

## 4. Admin Review and Decision

### Review Panel
All therapist applications appear in the **Therapist Applications** section of the Admin Dashboard. Admins can view each application with full detail including uploaded documents.

### Review Actions
The admin team takes one of three actions:

| Action | Outcome |
|---|---|
| **Approve** | Therapist account moves to "Active" status; profile becomes visible to clients |
| **Reject** | Application is declined; therapist is notified with a reason |
| **Request More Information** | Admin contacts therapist via email or support ticket for clarification |

### Approval Criteria
An application is approved when:
- License number is valid and active
- Degree is appropriate for the specialization claimed
- Experience is consistent with the application
- No red flags in professional background

### Rejection Criteria
An application may be rejected if:
- License cannot be verified
- Degree does not meet platform requirements
- Significant inconsistencies are found
- The specialization is outside the platform's current scope

---

## 5. Profile Activation

### What Happens After Approval
When an application is approved:

1. The therapist's account status changes from **"Pending"** to **"Active"**
2. A **therapist profile** is created in the platform's therapist directory
3. The therapist receives a notification and email confirming their approval

### Profile Setup
After activation, the therapist completes their profile setup:
- Upload a professional profile photo
- Write or edit their biography
- List clinical specializations
- Set session types offered (audio, video, chat)
- Set pricing for 45-, 60-, and 90-minute sessions
- Configure bank/payment details for earnings payouts
- Set notification preferences (email alerts, SMS alerts)

### Calendar Setup
The therapist creates their availability calendar by adding **calendar slots**:
- Select specific dates and times
- Set session duration
- Mark slots as "available" or block them

---

## 6. Crisis Certification

### What It Is
A special designation awarded to therapists who are qualified and trained in crisis intervention.

### Why It Matters
Crisis-certified therapists are the first point of human contact when the platform detects a client in crisis. They are also prioritized in the therapist directory when a client searches for crisis support.

### How It Is Assigned
The crisis certification flag (`is_crisis_certified`) is set by the admin team as part of the therapist profile review. It is typically granted to therapists with documented training in:
- Suicide risk assessment
- Crisis de-escalation
- Trauma-informed care

---

## 7. Therapist Status Lifecycle

```
Application Submitted → "Pending"
                            │
               ┌────────────┼────────────┐
               │            │            │
           Approved      Rejected    More Info
               │            │        Requested
               ▼            ▼            │
            "Active"   "Rejected"        │
               │       (notified)        │
               │                    Therapist
               │                    Responds
               │                        │
               │                    Re-reviewed
               │                        │
               ▼                        ▼
        Full Access              Approved/Rejected
       to Platform
               │
               │ (conduct violation)
               ▼
         "Suspended"
```

---

## 8. Boost and Pro Subscription (Optional)

### Therapist Boost
A paid promotional feature where therapists pay a fee to appear higher in the therapist directory for a set number of days.

| Boost Type | Description |
|---|---|
| **Basic Boost** | Moderate visibility increase |
| **Professional Boost** | Maximum visibility — featured at top of directory |

Boost applications follow the same payment screenshot process as client sessions — the therapist uploads payment proof, and the admin verifies and activates the boost.

### Pro Subscription
A separate subscription for therapists that unlocks additional platform features. Identical payment process to boosts.

---

## 9. Ongoing Compliance

### Therapist Account Review
Therapist accounts are subject to ongoing review if:
- Client complaints are filed (via support tickets)
- Safety incidents are logged
- Violation strikes are accumulated

### Violation Strikes
The platform tracks `violationStrikes` on each therapist's profile. Accumulating strikes can result in:
- A formal warning notification
- Account suspension
- Application rejection for re-approval

---

## Process Flow

```
Prospective Therapist Finds Sukoon AI
               │
               ▼
Registers on Platform (selects "Therapist" role)
               │
               ▼
Fills Out Application Form
(Name, License, Specialty, CV, Degree)
               │
               ▼
  Application Status: "Pending"
               │
               ▼
  Admin Reviews Documents
               │
    ┌──────────┴──────────┐
    │                     │
 Approved             Rejected
    │                     │
    ▼                     ▼
Account Activated    Notification Sent
    │                with Rejection Reason
    ▼
Profile Setup (photo, bio, pricing, calendar)
    │
    ▼
Visible in Therapist Directory
    │
    ▼
Clients Find and Book Sessions
```

---

## Business Impact

| Metric | Description |
|---|---|
| **Therapist supply** | Number of active therapists directly limits session booking capacity |
| **Application approval rate** | Reflects quality bar; too low = talent bottleneck; too lenient = quality risk |
| **Time-to-activation** | Long review delays cause therapist drop-off; target ≤ 5 business days |
| **Therapist retention** | Active, booking therapists indicate platform health |
| **Crisis-certified therapists** | A critical safety metric — platform needs sufficient coverage for crisis escalations |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Unqualified therapist approved** | Clinical harm, legal liability | Rigorous document check; external verification partnerships |
| **Slow review process** | Qualified therapists choose competitors | Set 5-business-day approval target; dedicated reviewer role |
| **Fake license numbers** | Fraudulent applications | License cross-check with licensing authority APIs |
| **Therapist abandons profile** | Inactive profiles mislead clients | Auto-deactivate profiles with no availability in 30 days |
| **Scope mismatch** | Therapist specializes in areas platform clients don't need | Match specializations to demand data |

---

## Recommendations

1. **Partner with PMDC and equivalent licensing bodies** to create an API-based license verification system, reducing manual verification time.
2. **Create a standardized therapist onboarding video** walkthrough that guides newly approved therapists through profile setup in 10 minutes.
3. **Define a minimum profile completeness score** before a therapist profile is made visible to clients (e.g., must have photo, bio, pricing, and at least 3 available slots).
4. **Establish a therapist community forum** or WhatsApp group for peer support and platform updates, increasing therapist loyalty and retention.
5. **Create a therapist performance dashboard** that shows each therapist their own rating, session count, and earnings — giving them data to improve their practice.
