# Therapist Approvals — Sukoon AI

**Section:** 04 — Admin Panel  
**Document:** THERAPIST_APPROVALS.md  
**Audience:** Admin Team, Clinical Supervisors, Operations, Compliance

---

## Executive Summary

The Therapist Approval process is the critical gateway that ensures only qualified, verified mental health professionals can practice on the Sukoon AI platform. Admins review each therapist application manually, evaluate submitted credentials, and make an approval or rejection decision. This document covers the complete approval workflow, review criteria, and post-approval steps.

---

## Purpose

To define the process by which the admin team evaluates and approves (or rejects) therapist applications, ensuring that every active therapist on the platform meets the required professional and ethical standards.

---

## Stakeholders

- Admin team (primary reviewers)
- Clinical supervisor (final authority on clinical standards)
- Applicant therapists (awaiting decision)
- Clients (who depend on therapist quality assurance)

---

## 1. Therapist Application Statuses

| Status | Meaning |
|---|---|
| **Pending** | Application submitted; not yet reviewed |
| **Approved** | Application accepted; therapist account activated |
| **Rejected** | Application declined; therapist notified with reason |

---

## 2. What the Admin Reviews

When a therapist application arrives, admins have access to everything the therapist submitted during registration:

### Personal Information
- Full name, email address, phone number
- City and country of practice

### Professional Credentials
| Submitted Item | Review Purpose |
|---|---|
| **Professional title** | Confirms claimed specialty (e.g., Clinical Psychologist, Counselor) |
| **Years of experience** | Baseline competency check |
| **Degree / qualification** | Educational verification |
| **License number** | Regulatory compliance |
| **University / institution name** | Credential cross-reference |
| **CV (curriculum vitae)** | Complete professional history |

### Practice Details
- Specializations (e.g., Anxiety, Depression, Trauma, CBT)
- Languages spoken (key for client matching)
- Session types offered (audio, video, chat)
- Session pricing (45-min, 60-min, 90-min rates)

### Crisis Certification
- Whether the therapist claims crisis certification
- Crisis certification is a separate flag that enables the therapist to receive **crisis-triggered assignments** from the AI alert system

---

## 3. Admin Review Process

### Step 1 — Application Arrives
- Admin receives a notification that a new therapist application has been submitted
- The application appears in the **Therapist Applications** section of the Admin Dashboard under "Pending" filter

### Step 2 — Initial Credential Scan
- Admin reviews the submitted CV and qualification documents
- Checks that a license number is provided (format validation if applicable)
- Verifies that specializations match the stated professional title

### Step 3 — External Verification (Optional but Recommended)
- For licensed professionals, the admin may verify the license number with the relevant regulatory body (e.g., Pakistan Council for Mental Health, local psychological association)
- This step is currently a manual process and is subject to the admin team's capacity

### Step 4 — Approval or Rejection Decision

#### Approve
- Admin clicks **"Approve"** on the application
- The therapist's account role is updated to `"therapist"`
- The therapist's profile is activated and becomes **visible in the Therapist Directory**
- The therapist receives an approval notification email/in-app message
- The therapist can now log in, complete their profile, and start adding calendar availability

#### Reject
- Admin clicks **"Reject"** and provides a **reason** (mandatory)
- The therapist receives a rejection notification with the stated reason
- The rejection reason is saved on the application record
- The applicant may re-apply after addressing the rejection reason

---

## 4. Rejection Criteria

Common grounds for rejection include:

| Rejection Reason | Explanation |
|---|---|
| **Incomplete credentials** | CV or degree not provided |
| **Invalid license number** | License number cannot be verified or appears incorrect |
| **Qualification mismatch** | Title claimed does not match submitted degree |
| **Insufficient experience** | Applicant does not meet minimum experience threshold |
| **Specialization gap** | Practice areas claimed are outside the scope of training |
| **Unprofessional application** | Application indicates ethical concerns or unprofessional conduct |
| **Duplicate application** | A previous account for this individual already exists |

---

## 5. Crisis Certification Verification

If the therapist has indicated they are **crisis-certified**, the admin must verify this separately:
- Request the crisis certification document
- Confirm validity with the issuing authority if possible
- Mark `crisis_certified = true` on the therapist profile only after verification

Incorrectly granting crisis certification to an unqualified therapist is a **high-severity safety risk** — unqualified therapists assigned to crisis clients can cause harm.

---

## 6. Boost Status and Pro Subscription

Upon approval, therapists are by default on "Basic Boost" status. The admin can also review requests from therapists to upgrade to:

### Boost Status
| Level | Visibility Benefit |
|---|---|
| **Basic** | Standard listing in directory |
| **Professional** | Featured/boosted placement in directory search results |

Pro Boost requests are reviewed separately from the initial application, typically requested by therapists after they have built some activity on the platform.

### Pro Subscription
Therapists can subscribe to a "Pro" tier that may unlock additional features. Admin manages and verifies pro subscription status.

---

## 7. Re-Application Process

Rejected therapists can:
1. Review the rejection reason provided
2. Address the deficiency (obtain required credentials, correct information)
3. Submit a new application

There is no automatic cooldown period before re-application, but admins should track whether a therapist has been rejected multiple times for the same reason — an indicator of an ongoing issue.

---

## 8. Therapist Directory Activation

After approval:
- The therapist's profile appears in the **Therapist Directory** visible to all clients
- Profile completeness affects how useful the listing is to clients — admins should encourage newly approved therapists to:
  - Upload a professional photo
  - Write a biography
  - Set their available calendar slots
  - Configure their session pricing

Newly approved therapists who do not complete their profile within 7 days should receive a follow-up nudge from the admin team.

---

## Process Flow

```
Therapist Submits Application
        │
        ▼
Application Appears in Admin Dashboard (Pending)
        │
        ▼
Admin Reviews Credentials
  ├── CV
  ├── Degree
  ├── License Number
  └── Specializations
        │
  ┌─────┴────────────────────────┐
  │                               │
Approved                       Rejected
  │                               │
  ▼                               ▼
Account Activated           Rejection Reason Sent
Profile Visible in          to Applicant
Directory
  │
  ▼
Therapist Completes Profile
  │
  ▼
Calendar Slots Added
  │
  ▼
First Bookings Appear
```

---

## Business Impact

| Decision Quality | Business Impact |
|---|---|
| **High-quality approvals** | Builds client trust; drives repeat bookings; strengthens platform reputation |
| **Approving unqualified therapists** | Severe reputational and legal risk if harm occurs |
| **Slow approval process** | Frustrates quality applicants; they may join competitor platforms |
| **Rejecting good applicants** | Reduces therapist supply; limits client access to care |
| **Crisis certification accuracy** | Directly impacts platform safety in life-risk situations |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Fraudulent credentials** | Applicant submits fake degree or license | External verification with regulatory bodies |
| **Unverified crisis certification** | Crisis therapist is not actually certified | Mandatory document submission and verification step |
| **Slow review queue** | Applications pile up; therapists wait weeks | 48-hour SLA target for initial review |
| **Bias in approval decisions** | Inconsistent standards across admins | Standardized approval checklist; clinical supervisor final sign-off |
| **Rejected applicant re-applying repeatedly** | System used to probe criteria | Track re-application history; add cooldown after 3 rejections |

---

## Recommendations

1. **Create a standardized therapist approval checklist** — a documented list of every item to verify before approving, ensuring consistency regardless of which admin is reviewing.
2. **Establish a 48-hour SLA target** for initial review of new applications, with escalation to a supervisor if the SLA is exceeded.
3. **Integrate with official regulatory body APIs** (where available) to automate license number verification, reducing manual cross-checking workload.
4. **Require profile completion as a condition of first listing** — prevent incomplete profiles from appearing in the directory to maintain quality standards.
5. **Implement a quarterly credential re-verification program** — require active therapists to confirm their license is still valid annually or upon renewal.
