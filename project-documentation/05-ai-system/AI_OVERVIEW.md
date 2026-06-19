# AI System Overview — Sukoon AI

**Section:** 05 — AI System  
**Document:** AI_OVERVIEW.md  
**Audience:** Founders, Investors, Therapists, Clinical Advisors, Operations Team

---

## Executive Summary

The Sukoon AI platform uses Google's Gemini large language model as its AI engine, configured specifically for the mental health and emotional wellness context. The AI functions as an always-available emotional support companion — not a clinical replacement for human therapists, but an accessible first point of contact for users who need to talk, reflect, or process their emotions. This document provides a high-level overview of the AI system: what it does, how it is designed, and what boundaries are in place.

---

## Purpose

To explain, in plain terms, what the Sukoon AI assistant is, how it operates, what it is designed to do, and what safeguards govern its behavior — for non-technical audiences including founders, investors, and clinical advisors.

---

## Stakeholders

- Founders and investors (understanding the AI product)
- Therapists (understanding how AI interacts with their clients)
- Clinical advisors (evaluating safety and clinical standards)
- Operations team (governing AI behavior)
- Admin team (monitoring AI-triggered alerts)

---

## 1. What the AI Is

The Sukoon AI assistant is a **conversational AI companion** that:
- Engages users in text-based conversations about their mental health and emotional wellbeing
- Responds with empathy, evidence-based support frameworks (CBT-influenced language, motivational interviewing), and practical guidance
- Remembers context from previous conversations (through a memory system)
- Monitors conversations for signs of crisis (suicidal ideation, self-harm, severe distress)
- Operates within a defined persona and set of ethical boundaries

The AI is available **24 hours a day, 7 days a week**, providing emotional support at moments when a human therapist is not available.

---

## 2. What the AI Is Not

| It Is NOT | Why This Matters |
|---|---|
| A licensed therapist | It cannot diagnose, prescribe, or provide clinical treatment |
| A crisis service | It detects crisis signals but cannot intervene as an emergency service |
| A general-purpose AI chatbot | It is restricted to mental health and wellness topics |
| A replacement for human therapy | It is explicitly designed to complement, not replace, professional care |
| A recording or surveillance tool | Sessions in "Tarash Zone" are never saved or analyzed |

---

## 3. The AI Engine

The AI is powered by **Google Gemini** — Google's family of large language models. Gemini is accessed through Google's official AI API and operates as a **server-side service** (the AI call is made from Sukoon's servers, not directly from the user's device, protecting the API key and enabling additional controls).

### Why Gemini
- State-of-the-art language understanding and generation
- Strong performance in empathetic and supportive conversational contexts
- Scalable to handle concurrent user sessions
- Integrated with Google's safety filters

---

## 4. The AI Persona: Sukoon

The AI assistant has a defined persona named **"Sukoon"** (the Urdu word for peace and tranquility). This persona is configured through a **system prompt** — a set of instructions given to the AI before every conversation that shapes its behavior.

### Sukoon's Core Personality
- Warm, empathetic, non-judgmental
- Patient and present
- Evidence-informed (draws on CBT, mindfulness, motivational interviewing concepts)
- Culturally sensitive (designed for South Asian context)
- Clear about being an AI, not a human therapist

### What Sukoon Focuses On
- Listening to the user's current emotional state
- Helping users articulate and understand their feelings
- Offering practical coping strategies
- Encouraging professional therapy for clinical concerns
- Mood tracking and daily check-in conversations
- Guided journaling prompts

---

## 5. AI Safety System

The AI system includes multiple layers of safety:

### Layer 1 — System Prompt Restrictions
The AI is instructed never to:
- Pretend to be human
- Provide medical or clinical diagnoses
- Offer advice on medications
- Engage with topics outside mental health and wellness
- Dismiss or minimize expressions of crisis

### Layer 2 — Crisis Keyword Detection
Every message sent by a user is **scanned for crisis keywords** before the AI responds. If a crisis keyword is detected, the platform:
1. Flags the user as high risk
2. Creates a Risk Alert in the Admin Dashboard
3. May alter the AI response to include crisis resources and immediate support language

This scan happens in addition to the AI's own response — it is a parallel safety layer, not dependent on the AI's judgment.

### Layer 3 — Tarash Zone (Privacy Mode)
The "Tarash Zone" is a special privacy mode that users can activate during AI chat sessions. In Tarash Zone:
- Nothing the user says is saved to the database
- No content analysis is run on the messages
- The AI still responds normally, but no record is kept

This allows users to speak freely about sensitive topics without fear of surveillance.

### Layer 4 — Human Escalation
When crisis signals are detected, the AI points users toward:
- Immediate platform support (contacting the admin team)
- Connecting with their assigned therapist (if they have one)
- External emergency contacts and crisis hotlines

---

## 6. AI Memory System

The AI maintains a **Retrieval-Augmented Generation (RAG) memory system** that allows it to remember important facts from previous conversations.

### What This Means for Users
- The AI remembers that a user has been struggling with work stress for three weeks
- The AI can reference a coping strategy it suggested last session and ask how it went
- The AI can maintain continuity across sessions without users having to re-explain their history

### What Is Stored in Memory
Only high-signal information is stored — emotional patterns, significant life events mentioned, coping strategies tried, progress notes. Not verbatim transcripts.

This is documented in detail in the MEMORY_SYSTEM.md file.

---

## 7. Freemium AI Access

AI chat access is governed by the subscription tier system:

| Plan | AI Chat Limit |
|---|---|
| **Free** | Limited number of messages per day/month |
| **Basic** | Increased limit |
| **Standard** | Higher limit |
| **Premium / Enterprise** | Unlimited or very high limit |

When a user reaches their AI chat limit, they are prompted to upgrade their subscription plan. This is the primary mechanism for converting free users to paid subscribers.

---

## 8. AI Response Pipeline

When a user sends a message:
1. Message is received by the platform server
2. Crisis keyword scan runs (parallel safety check)
3. Relevant memory items are retrieved (RAG system)
4. A request is sent to the Gemini AI API with: system prompt + retrieved memory + conversation history + user's new message
5. Gemini generates a response
6. Response is returned to the user
7. Memory update runs (if the message contains significant new information)

---

## Process Flow

```
User Types Message
      │
      ▼
Crisis Keyword Scan (parallel)
  ├── Crisis Detected → Risk Alert Created → AI Response includes crisis resources
  └── No Crisis → Normal response flow
      │
      ▼
Memory Retrieval (RAG)
      │
      ▼
Gemini AI Called with full context
      │
      ▼
AI Generates Response
      │
      ▼
Response Delivered to User
      │
      ▼
Memory Update (if significant content detected)
```

---

## Business Impact

| AI Feature | Business Value |
|---|---|
| **24/7 availability** | Users can access support at any time, driving retention |
| **Empathetic persona** | Improves user satisfaction and session depth |
| **Memory continuity** | Differentiates platform from generic chatbots |
| **Crisis detection** | Reduces platform liability; demonstrates clinical responsibility |
| **Freemium gating** | AI access limits drive subscription conversion |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **AI giving harmful advice** | AI responds inappropriately to a clinical situation | System prompt restrictions; human escalation for crisis |
| **Over-reliance on AI** | Users substitute AI for professional therapy | AI explicitly encourages professional therapy; platform provides therapist directory |
| **Data privacy** | User conversations stored and potentially exposed | Tarash Zone privacy mode; encrypted storage; access controls |
| **AI persona inconsistency** | AI behaves differently across sessions | Well-defined system prompt; version-controlled configuration |
| **API outage** | Gemini API unavailable | Retry logic and graceful error messaging to user |

---

## Recommendations

1. **Establish a quarterly AI persona review** — review the system prompt with clinical advisors to ensure the AI's language and approach remain appropriate, culturally sensitive, and clinically sound.
2. **Log crisis detection events** for monthly clinical review — not the content of conversations, but the frequency and outcomes of crisis detections, to assess system effectiveness.
3. **Add explicit crisis resource section** in the AI interface — visible always, not just when triggered by keywords, so users know where to go for immediate help.
4. **Implement user consent flow** for AI memory — inform users that the AI maintains memory across sessions and give them the option to clear their AI memory at any time.
5. **Define an AI incident response plan** — a documented protocol for what happens if the AI produces a harmful, inappropriate, or dangerous response, including who is notified and how it is addressed.
