# Safety Process — Sukoon AI

**Section:** 08 — Security and Trust  
**Document:** SAFETY_PROCESS.md  
**Audience:** Clinical Advisors, Admin Team, Operations Team, Founders, Investors

---

## Executive Summary

Safety on Sukoon AI operates across three dimensions: the safety of users (protecting mental health and preventing harm), the safety of therapists (protecting professional integrity and personal wellbeing), and the safety of the platform (protecting data and operations). This document maps all safety processes — from crisis detection and therapist incident reporting to content moderation and user account safety — providing a comprehensive view of how the platform maintains a safe environment.

---

## Purpose

To document every safety process on the Sukoon AI platform, defining what the platform does to protect its users and therapists, who is responsible for each safety function, and what happens when safety incidents occur.

---

## Stakeholders

- Clinical advisors (clinical safety standards)
- Admin team (safety response)
- Therapists (safety incident reporting)
- Founders and investors (governance and liability)
- Operations team (safety monitoring)

---

## 1. User Safety Framework

### 1.1 — AI Crisis Detection
Every message in an AI chat session (outside of Tarash Zone) is scanned for crisis-indicating language. When detected:
- A Risk Alert is created for the admin team
- The AI response is modified to include crisis resource language
- The user is connected to a crisis-certified therapist (see CRISIS_ESCALATION.md for full detail)

### 1.2 — Tarash Zone Privacy Protection
While not a direct safety intervention, Tarash Zone protects users by allowing them to speak freely about sensitive topics without fear of surveillance — removing a barrier that might prevent someone from disclosing a crisis to the AI in the first place.

### 1.3 — Crisis Resource Visibility
Crisis resources (emergency contacts, platform support links) must be visible in the platform at all times, independent of navigation. A dedicated "Help" or "Crisis" button that does not require account authentication is a recommended minimum standard.

### 1.4 — Account Safety
Users' accounts are protected by:
- Authentication through email/password or Google OAuth
- Session tokens with expiry (automatically logged out after inactivity)
- Admin ability to suspend or ban accounts for behavior that threatens other users
- No public visibility of user identity to other users (not a social platform)

---

## 2. Therapist Safety Framework

### 2.1 — Safety Incident Logging
Therapists are empowered and required to log safety incidents they encounter during sessions:
- Suicidal ideation or self-harm risk expressed by a client
- Harassment or abusive behavior from a client
- Privacy violations or boundary crossings
- Any situation where the therapist feels unsafe

Incidents are reviewed by the admin clinical team. The therapist is not alone in managing the situation.

### 2.2 — Therapist Wellbeing
Therapists on a mental health platform face vicarious trauma and emotional burnout risks. While the platform does not directly provide therapist wellbeing services, the operations team should:
- Monitor for signs of therapist burnout (high incident log rate, declining session completeness)
- Provide guidance to therapists on self-care resources
- Consider implementing a peer support or supervision network for platform therapists

### 2.3 — Professional Boundary Enforcement
Therapist-client communications are all on-platform (through the DM system). This:
- Prevents exchange of personal contact details
- Maintains professional boundaries
- Creates a record of all communications for audit if needed

---

## 3. Platform Content Safety

### 3.1 — AI Content Restrictions
The AI system prompt includes explicit restrictions on the types of content the AI will generate:
- No harmful advice
- No self-harm instructions
- No encouragement of dangerous behaviors
- No clinical diagnoses
- No medication recommendations

In addition, Google Gemini has built-in safety filters that reject requests for harmful content, providing a secondary content safety layer.

### 3.2 — Therapist Profile Moderation
Therapist profiles are reviewed at the point of approval and monitored for:
- Misleading claims about qualifications
- Inappropriate content
- Personal contact information (to prevent off-platform communication)

Admin team can edit or remove profiles that violate content standards.

### 3.3 — Support Ticket Moderation
Support tickets from users may contain distressing content. The support team is trained to:
- Recognize safety escalation signals in ticket content
- Escalate immediately if a ticket indicates the user is in crisis
- Not engage beyond their scope in clinical situations

---

## 4. Financial Safety

### 4.1 — Payment Fraud Prevention
Manual payment verification creates a human review layer that automated systems lack. Every payment screenshot is reviewed by a human admin before a session is confirmed, reducing the risk of fraudulent bookings.

### 4.2 — Payout Fraud Prevention
Payout requests are reviewed against the therapist's verified wallet balance before processing. Bank account details must match pre-registered information. Unusual payout requests (large amount from low-volume therapist) may require additional verification.

---

## 5. Data Safety

Data safety is covered in detail in DATA_HANDLING.md. Key points:
- Sensitive clinical data is encrypted and access-controlled
- Third-party data sharing is limited and documented
- Audit logs record all sensitive data access
- Backups ensure data is not lost in the event of system failure

---

## 6. Safety Governance Structure

| Safety Area | Responsible |
|---|---|
| **Clinical safety (user crisis)** | Clinical supervisor + Admin Lead |
| **Therapist incident management** | Clinical Admin |
| **AI content safety** | Clinical Advisor + Technical Lead |
| **Account security** | Technical Lead + Admin Lead |
| **Financial safety** | Finance Team + Admin Lead |
| **Data safety** | Technical Lead |
| **Content moderation** | Admin Team |

---

## 7. Safety Training Requirements

All admin and support team members must receive training on:
- Basic mental health first aid
- Crisis recognition in written communication
- Escalation procedures for safety-related tickets
- Data privacy protocols
- Professional boundaries in user communication

Training should be completed before any team member handles user support tickets or risk alerts, and refreshed annually.

---

## 8. Safety Metrics and Reporting

| Metric | Frequency |
|---|---|
| Risk alerts created | Monthly |
| Risk alerts resolved | Monthly |
| Average time to crisis therapist assignment | Monthly |
| Safety incidents logged by therapists | Monthly |
| Safety incidents resolved | Monthly |
| Support tickets flagged as safety-sensitive | Monthly |

Monthly safety metrics are included in the **Monthly Safety Report** shared with the executive team.

---

## Process Flow (Integrated Safety Response)

```
THREAT DETECTED (via AI scan, therapist report, support ticket)
        │
        ▼
Severity Assessment
  ├── Immediate crisis → P0 — Act within 1 hour
  ├── Active incident → P1 — Act within 4 hours
  └── Ongoing concern → P2 — Act within 24 hours
        │
        ▼
Appropriate Response:
  ├── P0: Assign crisis therapist; contact user; escalate if needed
  ├── P1: Clinical review; admin action; safety incident documented
  └── P2: Follow-up monitoring; support ticket response
        │
        ▼
Outcome Documented
        │
        ▼
Included in Monthly Safety Report
```

---

## Business Impact

| Safety Investment | Business Impact |
|---|---|
| **Crisis detection** | Prevents user harm; demonstrates clinical responsibility |
| **Therapist incident logging** | Protects therapists; professional liability management |
| **Content safety filters** | Prevents reputational incidents |
| **Financial fraud prevention** | Protects revenue and therapist trust |
| **Safety governance** | Investor confidence; regulatory compliance |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Crisis missed** | Safety system fails to detect a user in crisis | Multi-layer detection; human reporting supplement AI |
| **Safety incident underreported** | Therapist doesn't log incidents | Training; no-blame incident culture |
| **Burnout in safety responders** | Admin team handling intense situations | Rotation; mental health support for team |
| **AI content bypass** | User finds prompt injection to make AI behave unsafely | Regular AI red-team testing |
| **Escalation failure** | Safety incident escalation process not followed | Clear written procedure; regular drills |

---

## Recommendations

1. **Formalize a Safety Response Playbook** — a step-by-step document for each type of safety incident (crisis alert, therapist incident, data breach, financial fraud), so any team member can follow the correct procedure.
2. **Conduct quarterly safety drills** — simulate a crisis alert, a therapist incident, and a data breach scenario to test that the team can execute the response procedures correctly.
3. **Establish a clinical ethics advisory board** — even informally, having 2–3 licensed mental health professionals available for consultation on difficult cases provides essential clinical governance.
4. **Create a no-blame incident culture** — therapists and staff should feel safe reporting incidents and errors without fear of punishment. This is how safety systems learn and improve.
5. **Publish a Safety Charter** — a public-facing statement of the platform's safety commitments, available to users, therapists, and investors, demonstrating the seriousness with which the platform takes its safety responsibilities.
