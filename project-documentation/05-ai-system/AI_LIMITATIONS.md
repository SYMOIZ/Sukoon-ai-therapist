# AI Limitations — Sukoon AI

**Section:** 05 — AI System  
**Document:** AI_LIMITATIONS.md  
**Audience:** Founders, Investors, Clinical Advisors, Therapists, Operations Team

---

## Executive Summary

The Sukoon AI assistant is a powerful and valuable tool for emotional support, but it has defined limitations that everyone involved with the platform must understand. These limitations are not failures — they are intentional boundaries and inherent characteristics of AI technology in the current state of development. This document describes what the AI cannot do, what it should not be expected to do, and what safeguards exist to prevent it from operating outside its appropriate scope.

---

## Purpose

To clearly document the clinical, technical, and ethical limitations of the Sukoon AI assistant, ensuring all stakeholders — especially clinical advisors, therapists, and business leaders — have accurate expectations of the system.

---

## Stakeholders

- Clinical advisors (setting appropriate clinical standards)
- Therapists (understanding what the AI does and does not do before referring clients to use it)
- Founders and investors (accurate representation of the product)
- Operations team (knowing when to intervene)
- Users (who must understand they are interacting with an AI, not a therapist)

---

## 1. Clinical Limitations

### 1.1 — Cannot Diagnose
The AI cannot and must not diagnose any mental health condition. It cannot tell a user they have depression, anxiety disorder, PTSD, bipolar disorder, or any other clinical condition. Only a licensed clinical professional can make a diagnosis after appropriate assessment.

**If a user asks the AI whether they have a specific condition:** The AI is instructed to acknowledge the user's experience, explain that it cannot make diagnoses, and encourage the user to seek an assessment from a licensed professional.

### 1.2 — Cannot Prescribe or Advise on Medication
The AI has no knowledge of a user's medical history and is not licensed to advise on medications. It must not:
- Suggest starting, stopping, or changing a psychiatric medication
- Comment on dosing
- Advise on interactions between medications

**If a user asks about medication:** The AI is instructed to direct the user to their prescribing doctor or psychiatrist.

### 1.3 — Cannot Provide Clinical Therapy
The AI is not a therapist. It cannot conduct Cognitive Behavioral Therapy, EMDR, trauma processing, or any other evidence-based therapeutic intervention as a clinical treatment. It can use language informed by therapeutic frameworks (e.g., CBT-influenced thought challenging) but this is supportive, not clinical.

### 1.4 — Cannot Assess Clinical Risk
The AI detects crisis keywords, but it cannot conduct a proper clinical risk assessment. A formal suicide risk assessment requires a trained clinician using validated tools (e.g., Columbia Suicide Severity Rating Scale). When crisis signals are detected, the responsibility shifts to the admin team and the crisis-certified therapist.

---

## 2. Knowledge Limitations

### 2.1 — Knowledge Cutoff
Like all large language models, the Gemini AI's base knowledge has a training cutoff date. It may not be aware of:
- Recent developments in mental health research
- Newly approved treatments
- Current events that might be affecting the user's situation

### 2.2 — No Real-World Verification
The AI cannot verify any facts the user tells it. If a user says they have been to therapy before, or that a doctor said something specific, the AI accepts this at face value. It cannot cross-reference or confirm.

### 2.3 — Not a Crisis Hotline
The AI does not have the training, protocols, or legal authority of a professional crisis line. It can direct users to crisis resources, but it should never be positioned as an equivalent to a crisis hotline.

---

## 3. Interaction Limitations

### 3.1 — May Generate Inaccurate or Unhelpful Responses
No AI model is perfect. The Sukoon AI may occasionally:
- Misunderstand the user's emotional state
- Provide advice that is well-intentioned but not helpful for the specific individual
- Misinterpret a culturally specific expression

Users who feel the AI's response was inappropriate should be encouraged to use the feedback mechanism or contact support.

### 3.2 — Cannot Remember Without the Memory System
Outside of what is stored in the memory system, the AI has no recollection of prior sessions. If memory retrieval fails (e.g., no relevant memories found), the AI starts from limited context. Users may sometimes need to re-explain their situation.

### 3.3 — Cannot Take Actions in the World
The AI is conversational only. It cannot:
- Send messages on behalf of the user
- Book therapy sessions for the user (it can tell the user how to book, not do it for them)
- Contact emergency services
- Notify the user's family or emergency contacts

### 3.4 — No Voice or Video Capability
The AI currently operates through text chat only. It cannot conduct voice conversations or video sessions.

---

## 4. Ethical Limitations and Boundaries

### 4.1 — Cannot Form Relationships
The AI must not foster parasocial relationships or emotional dependency. If a user begins to treat the AI as a friend, romantic partner, or primary support person, the AI should gently redirect the user toward human connection and professional support.

### 4.2 — Cannot Guarantee Confidentiality
While the platform takes privacy seriously (see DATA_HANDLING.md), the AI cannot guarantee that conversations are fully confidential in all legal circumstances. Specific legal obligations (e.g., mandatory reporting in some jurisdictions) may apply.

### 4.3 — Should Not Replace Human Therapy
The AI is explicitly designed to complement professional therapy, not replace it. The platform must consistently communicate this distinction to users and avoid marketing language that implies the AI is equivalent to a licensed therapist.

---

## 5. Technical Limitations

### 5.1 — Dependent on API Availability
The AI requires a successful connection to the Google Gemini API. If the API is unavailable (planned outage or unexpected failure), AI chat will be unavailable. Users should receive clear error messages when this occurs.

### 5.2 — Response Latency
Generating AI responses takes time (typically 1–5 seconds). Under high load, this may increase. Users expect conversational speed; significant delays degrade the experience.

### 5.3 — Context Window Limits
The AI can only consider a limited amount of text in a single request (the "context window"). Very long conversations may require the platform to summarize or truncate earlier messages. The memory system partially addresses this, but there are inherent technical limits.

### 5.4 — Language and Cultural Limitations
The AI performs best in English. While the platform serves a South Asian audience (primarily Pakistan), the AI may perform less well with:
- Urdu-heavy messages
- Regional dialects and idioms
- Culturally specific expressions of distress

---

## 6. Communicating Limitations to Users

The platform should communicate AI limitations at key touchpoints:

| Touchpoint | Message |
|---|---|
| **Onboarding (first AI chat)** | "Hi, I'm Sukoon, your AI companion. I'm here to listen and support you, but I'm not a therapist or a substitute for professional mental health care." |
| **Subscription plans page** | "Sukoon AI provides emotional support, not clinical therapy. For professional care, connect with one of our licensed therapists." |
| **Crisis response in AI chat** | "What you're sharing sounds serious. Please reach out to a professional — I can help you connect with a therapist or find emergency support." |
| **Settings / About section** | Full disclosure of AI nature, capabilities, and limitations in plain language |

---

## Process Flow (When AI Limitations Are Reached)

```
User Asks Clinical Question (e.g., "Do I have depression?")
        │
        ▼
AI Detects Out-of-Scope Request
        │
        ▼
AI Responds with:
 1. Acknowledgment ("That sounds difficult...")
 2. Clear limitation statement ("I'm not able to diagnose...")
 3. Constructive redirect ("Here's how you can connect with a therapist...")
        │
        ▼
User Directed to:
  ├── Therapist Directory
  ├── Support (for further help)
  └── Crisis Resources (if distress signals present)
```

---

## Business Impact

| Limitation | Business Implication |
|---|---|
| **Cannot diagnose** | Reduces liability; requires platform to market honestly |
| **Not a crisis service** | Requires investment in crisis-certified therapist roster |
| **Text-only** | Limits session richness; voice/video roadmap adds value |
| **API dependency** | Service outages damage trust; redundancy is important |
| **Language limitations** | Limits market reach in Urdu-first users |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **User over-reliance on AI** | User substitutes AI for professional care in clinical situations | Consistent communication of AI scope; recommend therapy prominently |
| **AI provides harmful advice** | Out-of-scope response harms a vulnerable user | System prompt restrictions; clinical advisory review |
| **User frustrated by limitations** | User feels AI is unhelpful when it redirects | Warm, empathetic limitation responses that still provide value |
| **Platform misrepresentation** | Marketing implies clinical capability the AI doesn't have | Review all marketing copy with clinical advisor before publishing |

---

## Recommendations

1. **Create an AI Limitations disclosure page** in the app — a plain-English, easily accessible page that explains what the AI is, what it can and cannot do, and when to seek professional help.
2. **Conduct a clinical review of the AI's limitation responses** — have a licensed therapist test the AI with out-of-scope questions and evaluate whether the responses are appropriate and helpful.
3. **Build multilingual support into the roadmap** — adding Urdu language support would significantly expand the platform's effective reach in its primary market.
4. **Establish an AI feedback loop** — allow users to rate individual AI responses (thumbs up/down), with low-rated responses reviewed by the clinical team to identify and correct problematic patterns.
5. **Require honest marketing review** — all promotional materials should be reviewed to ensure no statement implies the AI provides clinical therapy, guarantees outcomes, or is equivalent to a licensed professional.
