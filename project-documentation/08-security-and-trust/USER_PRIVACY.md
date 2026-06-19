# User Privacy — Sukoon AI

**Section:** 08 — Security and Trust  
**Document:** USER_PRIVACY.md  
**Audience:** Users, Legal/Compliance Team, Investors, Clinical Advisors, Founders

---

## Executive Summary

Privacy is foundational to Sukoon AI. Users share highly sensitive personal information — their emotional struggles, mental health history, crisis moments, and intimate journal entries. The platform is designed with the principle that this information belongs to the user, is collected only for the purpose of providing care and support, and is protected against unauthorized access or misuse. This document defines Sukoon AI's privacy principles, what data is collected, how it is used, and what rights users have.

---

## Purpose

To establish and communicate Sukoon AI's privacy principles and user data rights, providing users, investors, and regulatory reviewers with a clear understanding of how personal information is handled.

---

## Stakeholders

- Users (whose privacy this protects)
- Legal and compliance team (regulatory adherence)
- Founders (privacy by design)
- Investors (governance and risk management)
- Clinical advisors (professional ethics)

---

## 1. Privacy Principles

Sukoon AI is committed to the following core privacy principles:

### 1.1 — Data Minimization
The platform collects only the information necessary to provide the service. It does not collect data "in case it might be useful later."

### 1.2 — Purpose Limitation
Information collected for one purpose (e.g., account authentication) is not used for a different purpose (e.g., marketing to external parties) without explicit user consent.

### 1.3 — User Control
Users have the right to access, export, and delete their personal data.

### 1.4 — Transparency
Users are informed — in plain language — about what data is collected, why, and how it is used. There are no hidden data collection practices.

### 1.5 — Appropriate Access
Personal data is accessible only to those with a legitimate operational need. Clinical data (chat history, journal entries) is subject to stricter access controls than general account data.

---

## 2. What Data Is Collected

### At Registration
| Data Item | Purpose |
|---|---|
| Full name | Identity and personalization |
| Email address | Authentication; notifications |
| Password (hashed) | Account security |
| Phone number (optional) | Account recovery |
| Date of birth (optional) | Age-appropriate content |

### During Platform Use
| Data Item | Purpose |
|---|---|
| **AI chat messages** | Providing AI support; memory system; crisis detection |
| **Journal entries** | Personal wellbeing tool; platform feature |
| **Mood check-in responses** | Wellbeing tracking; AI context |
| **Therapy session bookings** | Service delivery; payment tracking |
| **Payment proofs (screenshots)** | Manual payment verification; fraud prevention |
| **Support ticket content** | Issue resolution |
| **Profile settings and preferences** | Personalization |

### Not Collected
- Payment card numbers (no card details are ever stored; manual bank transfer model)
- Health records or medical history (not requested or stored)
- Device location (location is not tracked)
- Device contacts or other apps (no such permissions requested)

---

## 3. Tarash Zone — Privacy Mode

The **Tarash Zone** is the platform's dedicated privacy mode for AI chat sessions. When activated:
- The conversation is completely ephemeral
- No messages are saved to the database
- No crisis detection scan is run on the content
- No AI memory is created from the session
- The conversation leaves no record after the session ends

Tarash Zone exists specifically because the platform recognizes that users may need to speak freely about extremely sensitive topics — and that recording these conversations, even for safety purposes, could itself cause harm or prevent users from seeking help.

**Users must understand that crisis resources are always available through the platform menu, even during Tarash Zone sessions.**

---

## 4. Clinical Data Special Protections

AI chat messages and journal entries are **clinical-sensitivity data** — the most sensitive category of information on the platform. Special protections apply:

| Protection | Detail |
|---|---|
| **Access restriction** | Chat and journal data is not accessible to general admin staff; restricted to clinical review roles |
| **Documented access** | Any access to a user's clinical data by an admin must be logged with a documented reason |
| **Minimum necessary** | Only the specific session or entry relevant to an issue is accessed, not the full history |
| **Audit trail** | All data access events are recorded for accountability |

---

## 5. User Rights

Every registered user has the following rights:

| Right | How to Exercise |
|---|---|
| **Right to Access** | Request a copy of all personal data held by the platform through a support ticket |
| **Right to Correction** | Request correction of inaccurate information in their account profile |
| **Right to Deletion** | Request deletion of their account and associated personal data |
| **Right to Data Portability** | Request an export of their data in a readable format |
| **Right to Restrict Processing** | Request that the platform stop using their data for non-essential purposes |
| **Right to Object** | Object to use of their data for marketing purposes |

Requests for data access or deletion are handled through support tickets and must be responded to within **30 days**.

---

## 6. Third-Party Data Sharing

Sukoon AI does not sell user data to third parties. User data may be shared with:

| Third Party | What Is Shared | Why |
|---|---|---|
| **Google (Gemini AI API)** | Current conversation messages | AI response generation |
| **Google (Firebase Auth)** | Email, display name | Authentication via Google OAuth |
| **Payment processor (future)** | Payment transaction data | Automated payment processing |

### Important: Gemini API and Privacy
When a user's message is sent to the Gemini API, that message content is processed by Google's servers. Users should be informed that their AI chat messages are processed by Google Gemini as part of the service delivery.

---

## 7. Children's Privacy

Sukoon AI is not intended for use by children under 13 years of age. The platform does not knowingly collect personal information from children. If a user is identified as being under 13, their account will be suspended and their data removed promptly.

For users aged 13–17, parental consent should be considered as the platform involves mental health discussions that may be age-sensitive.

---

## 8. Privacy Policy Communication

The platform's privacy practices must be communicated to users:
- At registration (acceptance of Privacy Policy as a condition of use)
- In the platform's Settings/About section (accessible at any time)
- In plain, non-legal language (alongside any legal document)

---

## Process Flow (Data Access Request)

```
User Submits Data Access/Deletion Request (Support Ticket)
        │
        ▼
Admin Verifies Identity of Requester
        │
        ▼
Check for Open Disputes, Active Bookings, Safety Investigations
        │
  ┌─────┴──────────────────────────┐
  │                                 │
Clear to Proceed              Blocked Pending Resolution
  │                                 │
  ▼                                 ▼
Data Access: Compile export     Notify user of reason for delay
Data Deletion: Anonymize PII
        │
        ▼
Respond to User within 30 Days
```

---

## Business Impact

| Privacy Feature | Business Impact |
|---|---|
| **Tarash Zone** | Differentiating trust feature; increases willingness to share |
| **Clear privacy policy** | Regulatory compliance; user confidence |
| **Data minimization** | Reduces security risk; reduces liability |
| **User data rights** | Regulatory compliance; builds institutional trust |
| **No data selling** | Brand integrity; user loyalty |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Data breach** | Unauthorized access to user data | Encryption at rest and in transit; access controls; audit logs |
| **Gemini API data handling** | Google's use of conversation data | Review Google's data processing terms; communicate clearly to users |
| **Tarash Zone failure** | Technical bug causes ephemeral data to be stored | Separate code path; thorough testing; periodic audit |
| **Unauthorized admin access** | Staff member accessing clinical data without cause | Role-based access; mandatory logging |
| **Regulatory non-compliance** | Failure to meet privacy law requirements | Consult legal advisor on Pakistan and applicable regional requirements |

---

## Recommendations

1. **Draft and publish a plain-language Privacy Policy** accessible in the platform's settings — written at an 8th-grade reading level, not legal English.
2. **Engage a legal advisor** to review the platform's data practices against applicable privacy regulations in Pakistan and any target export markets.
3. **Implement data retention limits** — define how long chat messages, journal entries, and payment screenshots are retained, and build automatic deletion of data beyond those limits.
4. **Conduct an annual privacy audit** — review all data collection practices, third-party data sharing, and access logs annually to identify and address gaps.
5. **Add in-app privacy education** — a simple onboarding screen explaining what the AI remembers, what Tarash Zone does, and how to delete data — building informed, confident users.
