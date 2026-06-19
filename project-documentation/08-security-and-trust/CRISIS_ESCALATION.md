# Crisis Escalation — Sukoon AI

**Section:** 08 — Security and Trust  
**Document:** CRISIS_ESCALATION.md  
**Audience:** Clinical Advisors, Admin Team, Crisis-Certified Therapists, Founders

---

## Executive Summary

Crisis escalation at Sukoon AI is a multi-stage process that begins when the AI detects crisis language in a user's message and ends when a crisis-certified therapist has made contact with the at-risk user and their wellbeing has been assessed. The process spans automated detection, human admin review, clinical assignment, and professional follow-up. This document defines every step of the crisis escalation process, the roles responsible at each stage, and the standards that must be met.

---

## Purpose

To establish a clear, actionable crisis escalation process that ensures every at-risk user on the Sukoon AI platform receives appropriate human intervention in a timely manner.

---

## Stakeholders

- Clinical advisors (setting clinical standards for escalation)
- Admin team (monitoring and assignment)
- Crisis-certified therapists (response)
- Operations manager (oversight and response time monitoring)
- Founders and investors (governance and liability)

---

## 1. What Constitutes a Crisis

For the purposes of this escalation process, a **crisis** is any situation where there is:
- Expressed or implied intent to harm oneself (suicidal ideation, self-harm)
- Active self-harm in progress
- Expressed intent to harm others
- Severe acute psychological distress that indicates a user is at immediate risk

Situations that require professional attention but are not crises include:
- Persistent low mood or depressive episodes without intent to harm
- General expressions of feeling hopeless or overwhelmed (without specific risk factors)
- Grief, anxiety, or life stressors

The distinction matters for triage — genuine crises require P0 immediate response; distress situations require prompt but less urgent follow-up.

---

## 2. Crisis Escalation Stages

### Stage 1 — Automated Detection

**What Happens:**
The AI crisis detection system scans every user message for crisis keywords. When a match is found:
- A Risk Alert is created in the Admin Dashboard
- The user's risk level is elevated to "High"
- The AI chat response is modified to include:
  - Warm, grounding acknowledgment of the user's distress
  - Explicit mention of in-platform support (admin contact, therapist connection)
  - External crisis resources (hotline numbers, emergency services)
- The AI does not alarm or panic — it focuses on connection and support

**Time to Response:** Automated — immediate.

**Responsible:** Automated system.

---

### Stage 2 — Admin Alert Review

**What Happens:**
The admin team receives the Risk Alert notification. An admin (ideally a clinically trained admin or clinical supervisor) reviews the alert:
- Reads the triggering message and context
- Assesses severity: Is this a genuine immediate crisis, a distress expression, or a false positive?
- Makes an initial triage decision

**Time to Response:** Target **within 1 hour** of alert creation for P0 crises; within 4 hours for distress situations.

**Responsible:** Admin on duty; escalate to Clinical Supervisor for P0.

---

### Stage 3 — Crisis Therapist Assignment

**What Happens:**
For confirmed crisis situations, the admin assigns a **crisis-certified therapist**:
1. Admin opens the Risk Alert and clicks "Assign Therapist"
2. Admin selects from the roster of crisis-certified therapists currently available
3. Assignment is created with:
   - Therapist assignment status: **Pending**
   - Response deadline (time by which therapist must respond)
4. Assigned therapist receives an urgent notification with:
   - User's name
   - Summary of the crisis alert context
   - Instructions to make contact immediately

**Time to Complete:** Assignment must be made within **1 hour** of alert for P0 crises.

**Responsible:** Admin / Clinical Supervisor.

---

### Stage 4 — Therapist Response

**What Happens:**
The crisis-certified therapist:
1. Reviews the alert and context
2. Accepts the assignment (status changes to **Accepted**)
3. Initiates contact with the user through the in-platform **Direct Message** system immediately
4. The initial contact message is warm, non-alarming, and focused on connection: "I'm here. I saw you're going through something really difficult right now. I'm here to talk if you'd like to."

**Time to Complete:** Therapist must accept and initiate first contact within **2 hours** of assignment.

**Responsible:** Assigned crisis-certified therapist.

---

### Stage 5 — Therapist Unable to Respond (Escalation Path)

**What Happens:**
If the assigned therapist:
- **Rejects** the assignment (status: Rejected)
- **Does not respond** within the response deadline

Then:
1. Admin is notified automatically
2. Admin assigns the next available crisis-certified therapist
3. If no crisis-certified therapists are available, the Operations Manager escalates to:
   - External crisis hotline referral for the user
   - Direct admin outreach to the user

**Time to Escalate:** Immediately upon rejection or deadline breach.

**Responsible:** Admin on duty.

---

### Stage 6 — Ongoing Clinical Follow-Up

**What Happens:**
After initial contact, the crisis-certified therapist:
1. Conducts an ongoing follow-up conversation to assess the user's safety
2. May recommend the user seek emergency services if the situation warrants
3. May arrange a formal therapy session (booked through the platform) for immediate structured support
4. Documents the intervention through:
   - Safety incident log entry
   - Session notes (if a formal session occurs)
5. The admin tracks the alert status until it is resolved

**Resolved When:** The user has been assessed by the therapist as stable, or has been referred to an appropriate level of care.

**Responsible:** Crisis therapist (primary); Admin (monitoring and documentation).

---

### Stage 7 — Alert Resolution and Documentation

**What Happens:**
Once the user is stable and the situation is resolved:
1. The crisis therapist or admin marks the Risk Alert as **"Resolved"**
2. The incident is logged in the safety incident record
3. A brief resolution note is added: What happened, what was done, outcome
4. The user remains on the "High Risk" monitoring list for a defined period (recommended: 30 days)
5. The incident is included in the monthly Safety Report

**Responsible:** Admin / Clinical Supervisor.

---

## 3. External Crisis Resources

The platform must always have visible references to external crisis resources for users who need immediate help beyond what the platform can provide:

| Resource | Contact |
|---|---|
| **Umang Pakistan (Mental Health Helpline)** | 0317-4288665 |
| **Rozan Counseling Helpline** | 051-2890505 |
| **Emergency Services (Pakistan)** | 115 (Rescue) / 1122 |
| **In-Platform Support** | Support ticket; admin direct message |

These resources must be:
- Accessible without login
- Visible during crisis AI response
- Listed in the platform's Help/About section

---

## 4. Crisis-Certified Therapist Roster

### Who Qualifies
Crisis-certified therapists are therapists who have:
- Verified crisis intervention training certification
- Admin-verified crisis certification flag (`crisis_certified = true`) on their profile
- Agreement to be available for crisis assignment on a defined schedule

### Availability Requirements
The platform must maintain a minimum number of crisis-certified therapists who are:
- Available during business hours
- On-call during evenings and weekends (on a rotation)

If the crisis-certified therapist roster is empty or unavailable, the admin team escalates directly to external crisis resources.

---

## 5. Response Time Standards

| Stage | Action | Target Time |
|---|---|---|
| Alert creation (automated) | Crisis keyword detected → Alert created | Immediate |
| Admin review | Admin reviews alert | Within 1 hour |
| Therapist assignment | Admin assigns therapist | Within 1 hour of alert |
| Therapist response | Therapist accepts + first contact | Within 2 hours of assignment |
| Therapist follow-up | Ongoing support | Within current session |
| Alert resolution | Admin marks resolved | Within 24–48 hours of initial response |

---

## Process Flow

```
AI CHAT: Crisis Keyword Detected
        │
        ▼
AUTOMATED: Risk Alert Created
AI Response Modified (crisis resources + empathy)
        │
        ▼
ADMIN NOTIFIED (within minutes)
        │
        ▼
ADMIN REVIEWS: P0 or distress?
  ├── P0 (Immediate Crisis) ──────────────────────────┐
  │                                                   │
  └── Distress (not immediate) → Monitor + DM Support │
                                                      │
                                              ASSIGN CRISIS THERAPIST
                                                      │
                                              THERAPIST NOTIFIED (urgent)
                                                      │
                                         Therapist Accepts?
                                           ├── YES → First Contact Initiated
                                           └── NO  → Reassign Next Therapist
                                                      │
                                              FOLLOW-UP CONVERSATION
                                                      │
                                              STABILITY ASSESSMENT
                                                      │
                                       Stable?
                                         ├── YES → Alert Resolved; 30-day monitoring
                                         └── NO  → Refer to Emergency Services;
                                                   Escalate to Clinical Supervisor
```

---

## Business Impact

| Crisis Process | Business Impact |
|---|---|
| **Timely crisis response** | Prevents tragic outcomes; greatest possible impact |
| **Clinical documentation** | Legal and regulatory protection for the platform |
| **Crisis-certified therapist roster** | Supply-side requirement for operating safely |
| **External resource referrals** | Demonstrates responsible limits of platform scope |
| **Monthly safety reporting** | Governance accountability; investor trust |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Delayed admin response** | Admin not monitoring alerts | 24/7 on-call; push notification for Critical alerts |
| **No available crisis therapist** | All crisis therapists unavailable | Maintain minimum roster; fallback to external resources |
| **Alert false positives** | Non-crisis flagged as crisis | Clinical review before full escalation |
| **User doesn't engage** | User ignores therapist's DM | Warm, low-pressure initial message; admin follow-up through support ticket |
| **Therapist not actually certified** | Crisis certification unverified | Mandatory certification document submission; admin verification |

---

## Recommendations

1. **Establish a minimum crisis-certified therapist coverage requirement** — define the minimum number of crisis-certified therapists who must be on-call at any time, and trigger a recruitment alert when coverage falls below this threshold.
2. **Build a crisis alert dashboard** — a dedicated view in the Admin Dashboard showing all open risk alerts, their ages, assignment status, and response progress — keeping crisis management visible and prioritized.
3. **Conduct annual crisis response drills** — simulate a P0 crisis alert and walk the team through the full escalation process to identify gaps and keep the team practiced.
4. **Partner with a crisis hotline service** — as a formal backup when platform-based crisis resources are unavailable, ensuring users always have a path to professional human support.
5. **Review every resolved crisis incident** — a post-incident review for each resolved crisis should identify what went well, what could be faster, and whether the outcome was appropriate — these reviews are how the crisis process improves over time.
