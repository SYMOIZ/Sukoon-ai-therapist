# Crisis Detection — Sukoon AI

**Section:** 05 — AI System  
**Document:** CRISIS_DETECTION.md  
**Audience:** Clinical Advisors, Founders, Investors, Admin Team, Operations Team

---

## Executive Summary

The Sukoon AI platform includes a dedicated crisis detection system that monitors every user message for signs of serious emotional distress — including suicidal ideation, self-harm, and acute mental health crises. When a crisis signal is detected, the platform automatically creates an alert for the admin team, adjusts the AI response to include crisis support messaging, and triggers an escalation workflow to connect the user with a crisis-certified therapist. This document describes how crisis detection works, what happens when it triggers, and what safeguards are in place.

---

## Purpose

To document the platform's approach to detecting and responding to user crisis situations — a core clinical safety responsibility — for clinical advisors, founders, and the operations team.

---

## Stakeholders

- Clinical advisors (setting crisis standards and keyword lists)
- Admin team (acting on risk alerts)
- Crisis-certified therapists (receiving emergency assignments)
- Founders and investors (understanding liability management and clinical governance)
- Users (who receive crisis support through this system)

---

## 1. What Crisis Detection Is

Crisis detection is a **real-time safety scan** that runs on every message a user sends during an AI chat session. It operates as a parallel check — the AI generates its response at the same time the crisis scan runs. The scan is not dependent on the AI's judgment; it is a separate, always-on safety layer.

### When It Runs
- Every message in an AI chat session is scanned
- The scan runs **before** or **simultaneously with** the AI response generation
- It does not run on messages in **Tarash Zone** sessions (where no content is saved or analyzed)

---

## 2. How Crisis Detection Works

### Keyword Matching
The crisis detection system uses a **curated list of crisis keywords and phrases** — words and expressions associated with suicidal ideation, self-harm intent, and acute distress.

Examples of crisis-triggering language (categories, not exhaustive):
- Direct statements of suicidal intent
- Expressions of hopelessness combined with plans
- Self-harm language
- Statements about ending one's life
- Expressions of extreme psychological pain with withdrawal from life

The keyword list is defined in the platform configuration and can be updated by the admin team as the clinical team refines the criteria.

### Matching Process
1. The user's message text is normalized (lowercased, punctuation-stripped)
2. The normalized text is checked against each keyword and phrase in the crisis list
3. If any match is found, the crisis detection system triggers

### Sensitivity vs. Specificity
Crisis keyword detection is intentionally set toward **higher sensitivity** (fewer missed crises) rather than higher specificity (fewer false alarms):
- The cost of missing a genuine crisis is far higher than the cost of a false alarm
- False alarms result in an admin creating an alert that is later confirmed to be non-crisis — manageable
- Missed crises could result in serious harm to the user

---

## 3. What Happens When Crisis Is Detected

### Step 1 — Risk Alert Created
- A **Risk Alert** is created in the Admin Dashboard
- The alert is marked with:
  - User ID and name
  - Timestamp
  - The triggering message (excerpt showing the flagged content)
  - Current assignment status: "None"

### Step 2 — Admin Dashboard Notification
- Admins see the new alert in the **Risk Alerts** section of the Admin Dashboard
- If the admin team has notification alerts configured, they receive an immediate in-app or email notification

### Step 3 — AI Response Adjusted
- The AI response for this message is modified to include:
  - Acknowledgment of the distress expressed
  - Empathetic, non-dismissive language
  - Explicit mention of crisis resources (hotline numbers, in-app support contact)
  - Encouragement to reach out to a human therapist or the admin team

The AI does not lecture or panic — the response is warm and grounding, prioritizing connection over information delivery.

### Step 4 — Crisis Therapist Assignment
- An admin reviews the alert and assigns a **crisis-certified therapist** to the user
- The assignment status moves: None → Pending → Accepted (or Rejected → Reassigned)
- The assigned therapist receives a notification with context about the situation
- The therapist initiates contact through the direct message system

### Step 5 — Resolution Tracking
- The admin tracks the alert status until it is resolved
- Resolution means: the crisis-certified therapist has made contact, and the user's risk status has been reassessed
- Unresolved alerts remain visible in the admin dashboard until explicitly closed

---

## 4. Crisis Risk Levels

Users are assigned a risk level that is updated by the crisis detection system:

| Risk Level | Trigger |
|---|---|
| **Low** | No crisis keywords detected; default status |
| **Medium** | Mild crisis language detected (general expressions of hopelessness without specific intent) |
| **High** | Specific crisis language detected (direct expressions of suicidal ideation or self-harm) |

Risk levels are visible in the Admin Dashboard on the user's profile and in the Risk Alerts section.

---

## 5. What the System Does NOT Do

| Limitation | Explanation |
|---|---|
| **Does not call emergency services** | The platform cannot directly contact police or ambulance; it can only escalate within the platform and direct users to external emergency contacts |
| **Does not guarantee response time** | If no crisis-certified therapist accepts the assignment quickly, the system escalates but cannot force a response |
| **Does not operate in Tarash Zone** | Privacy mode disables all scanning; users should be clearly informed that crisis resources are still always accessible through the platform menu |
| **May miss novel phrasing** | Keyword detection can miss crisis expressions in unusual phrasing, metaphors, or languages not covered by the keyword list |
| **Is not a clinical assessment** | A keyword match is not a clinical diagnosis of suicidal intent — the admin and therapist must make that assessment |

---

## 6. The Crisis Keyword List

The crisis keyword list is a configuration item maintained by the admin team in consultation with clinical advisors. It should be:
- Reviewed quarterly with the clinical team
- Updated as new expressions or patterns emerge
- Expanded to cover multiple languages used by the platform's user base (currently primarily English and Urdu)
- Treated as a sensitive document (not publicly disclosed)

---

## Process Flow

```
User Types Message (AI Chat Session)
          │
          ▼
Is Tarash Zone Active?
  ├── YES → No scanning; AI responds normally
  └── NO  → Crisis Keyword Scan Runs
             │
        Match Found?
          ├── NO  → Normal AI response
          └── YES → Risk Alert Created
                    Admin Notified
                    AI Response Modified (includes crisis resources)
                         │
                         ▼
                    Admin Reviews Alert
                         │
                         ▼
                    Crisis Therapist Assigned
                         │
                         ▼
                    Therapist Contacts User
                         │
                         ▼
                    Alert Resolved (admin marks closed)
```

---

## Business Impact

| Safety Feature | Business / Clinical Impact |
|---|---|
| **Real-time crisis detection** | Demonstrates clinical responsibility; reduces liability |
| **Immediate admin alert** | Enables timely human intervention |
| **Crisis resource messaging in AI response** | User receives help before admin responds |
| **Crisis therapist assignment** | Connects at-risk users with professional support |
| **Risk level tracking** | Enables ongoing monitoring of vulnerable users |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Missed crisis (false negative)** | Crisis language not in keyword list goes undetected | High-sensitivity keyword list; regular clinical review; encourage users to self-identify through support tickets |
| **False alarm (false positive)** | Non-crisis user flagged unnecessarily | Admin clinical review before full escalation; trained admin team |
| **Tarash Zone blind spot** | Crisis occurs during Tarash Zone session | Always-visible crisis resources in the interface, independent of Tarash Zone status |
| **No admin online** | Crisis alert created but not seen immediately | Configure 24/7 admin on-call rotation; push notifications for Critical alerts |
| **Therapist not responding** | Crisis assignment not accepted | Define maximum response SLA with escalation to next available therapist |

---

## Recommendations

1. **Establish a 24/7 admin on-call rotation** specifically for risk alert monitoring — at least one person must be reachable at all times to act on critical alerts.
2. **Define a maximum response SLA** for crisis alerts (recommendation: 2 hours from alert creation to therapist first contact), with automatic escalation if not met.
3. **Post permanent crisis resources** in the app interface (not behind any navigation) — a clearly visible "Crisis Help" button that leads to emergency contacts and platform support, accessible even during Tarash Zone.
4. **Conduct quarterly clinical review of the keyword list** with a licensed clinical psychologist to ensure the detection criteria remain appropriate and cover emerging patterns.
5. **Build a crisis detection performance report** — monthly review of how many alerts were generated, how many were genuine crises, and how quickly they were resolved — to continuously improve the system.
