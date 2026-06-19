# AI Response Flow — Sukoon AI

**Section:** 05 — AI System  
**Document:** AI_RESPONSE_FLOW.md  
**Audience:** Operations Team, Founders, Technical Advisors, Clinical Advisors

---

## Executive Summary

The AI response flow describes exactly what happens between the moment a user sends a message and the moment they receive the AI's reply. Multiple systems work in sequence and in parallel: message receipt, safety scanning, memory retrieval, AI generation, and response delivery. Understanding this flow is essential for operations teams managing the platform, clinical advisors evaluating its safety, and business leaders assessing its reliability.

---

## Purpose

To document, in plain terms, the complete sequence of operations that occurs when a user sends a message in the AI chat — from input to output — including every safety, memory, and quality step involved.

---

## Stakeholders

- Operations team (managing the platform)
- Technical advisors (reviewing architecture)
- Clinical advisors (validating safety steps)
- Founders (understanding product reliability)

---

## 1. The Complete Message-to-Response Cycle

### Stage 1 — Message Received by the Platform

When a user types a message and sends it:
- The message is received by the **Node.js server** (the platform's gateway)
- The server processes the request and routes it to the AI chat handler

### Stage 2 — Session Mode Check

Before any processing occurs, the server checks:
**Is this session in Tarash Zone (Privacy Mode)?**

- **YES — Tarash Zone Active:**
  - The message is NOT saved to the database
  - No crisis scan is run
  - No memory retrieval is performed
  - The AI receives the message with a modified context (privacy mode) and generates a response
  - The response is NOT saved
  - The user receives the response; session leaves no trace

- **NO — Standard Session:**
  - The message is saved to the chat history in the database
  - Processing continues to Stage 3

### Stage 3 — Crisis Detection (Parallel Safety Scan)

Running **in parallel** with the AI generation request:
- The message text is normalized
- The text is checked against the crisis keyword list
- **If a match is found:**
  - A Risk Alert is created in the Admin Dashboard
  - The AI response for this message is flagged to include crisis resource language
  - The user's risk level is updated
- **If no match is found:**
  - Normal response flow continues

This scan runs independently of the AI — even if the AI fails or is slow, the safety scan has already captured the crisis signal.

### Stage 4 — Memory Retrieval (Context Building)

Before calling the AI, the system retrieves relevant memories:
- A semantic search is run against the user's stored memory entries
- The top N most relevant memories are retrieved
- These memories are formatted as a context summary

Memory retrieval adds conversational continuity — the AI "knows" important things about the user without the user having to repeat them.

### Stage 5 — AI Request Construction

The full request to the AI is assembled:

```
REQUEST TO GEMINI AI:
├── System Prompt (Sukoon's persona, behavior rules, ethical restrictions)
├── Memory Context (top relevant memories retrieved in Stage 4)
├── Conversation History (recent messages from this session)
└── User's New Message (the message just sent)
```

This structured context is sent to the **Google Gemini API**.

### Stage 6 — AI Generation

Google Gemini processes the full request and generates a response:
- The AI considers the persona instructions, the user's history, and the current message
- The AI produces a response that is empathetic, contextually appropriate, and within scope

**If the crisis flag is active (from Stage 3):**
- The AI response is reviewed and augmented with crisis resource language before delivery

### Stage 7 — Response Delivery

The AI's response is:
1. Returned from the Gemini API to the platform server
2. Saved to the chat history in the database (for standard sessions)
3. Delivered to the user's screen

### Stage 8 — Memory Update

After the response is delivered:
- The system evaluates whether the conversation contained new high-signal information
- **If significant new information was shared** (e.g., user disclosed a new life event, made a progress update):
  - A new memory entry is created or an existing entry is updated
  - The memory is stored with a vector embedding for future retrieval
- **If no significant new information:**
  - No memory action; session continues

---

## 2. What Happens When the AI Takes Too Long

The platform uses retry logic for AI API calls:
- If the API does not respond within a defined timeout, the system retries
- After a maximum number of retries, a graceful error message is shown to the user
- The error does not expose any internal system information
- The user is encouraged to try again shortly

---

## 3. Message Rate and Subscription Limits

Before the message is processed, the system checks the user's subscription tier and message quota:
- If the user has remaining messages → proceed
- If the user has reached their message limit:
  - The message is not sent to the AI
  - The user sees an upgrade prompt explaining their limit and subscription options

This check occurs **before** the AI call to avoid wasting API usage on blocked users.

---

## 4. Response Modes

### Standard Response
The AI generates a natural, empathetic conversational response based on the user's message and context.

### Mood Check-In Response
If the user is completing a scheduled mood check-in (rather than free chat), the AI uses a slightly different prompt structure focused on asking about the user's current emotional state, energy level, and any specific concerns today.

### Crisis-Augmented Response
When crisis detection triggers, the AI response is modified to:
- Acknowledge the seriousness of what was shared
- Provide warm, grounding language
- Include explicit mention of crisis resources
- Not lecture or alarm, but clearly communicate that help is available

---

## Complete Flow Diagram

```
USER SENDS MESSAGE
       │
       ▼
┌─────────────────────────────────────────────┐
│         SESSION MODE CHECK                  │
│  Tarash Zone?                               │
│  YES → Skip storage/scan/memory             │
│  NO  → Continue                             │
└─────────────────────────────────────────────┘
       │
  ┌────┴────────────────────────────────┐
  │ PARALLEL OPERATIONS                 │
  │                                     │
  │  ┌─────────────────┐  ┌──────────┐ │
  │  │ Crisis Keyword  │  │ Memory   │ │
  │  │ Scan            │  │ Retrieval│ │
  │  │ (runs in        │  │          │ │
  │  │  parallel)      │  │          │ │
  │  └────────┬────────┘  └────┬─────┘ │
  │           │                │       │
  └───────────┼────────────────┼───────┘
              │                │
              ▼                ▼
        Crisis Alert?    Top Memories
        YES → Flag      Retrieved
              │                │
              └────────┬───────┘
                       │
                       ▼
             AI REQUEST ASSEMBLED
             (System Prompt +
              Memory Context +
              Conversation History +
              User Message)
                       │
                       ▼
              GEMINI AI API CALL
                       │
                   Success?
               NO → Retry (up to limit)
               YES → Response Returned
                       │
                       ▼
         Crisis Flag Active?
         YES → Augment with crisis resources
         NO  → Response as-is
                       │
                       ▼
              RESPONSE DELIVERED TO USER
              Response Saved to Chat History
                       │
                       ▼
              MEMORY UPDATE CHECK
              (New significant info? → Save memory)
```

---

## Business Impact

| Flow Stage | Business Importance |
|---|---|
| **Crisis scan** | Enables proactive safety management; demonstrates responsible AI |
| **Memory retrieval** | Differentiates product; drives user retention |
| **Subscription check** | Enforces monetization; drives upsell |
| **Fast response delivery** | User experience quality; platform perceived intelligence |
| **Graceful error handling** | Protects brand when AI service has issues |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **API latency** | Slow AI responses frustrate users | Response timeout with retry; streaming response display |
| **Memory retrieval failure** | Relevant memories not retrieved | Fallback to context-only mode if memory system unavailable |
| **Crisis scan failure** | Safety check not triggered | Alert admin team; log and investigate; manual review capability |
| **Tarash Zone bug** | Privacy mode fails to suppress storage | Thorough testing; separate code path verification |
| **Cost overrun** | High AI API usage exceeds budget | Subscription gating; monthly usage monitoring; API cost alerts |

---

## Recommendations

1. **Implement response streaming** — display the AI response word-by-word as it is generated (rather than waiting for the full response), significantly improving perceived response speed.
2. **Add latency monitoring** — track AI response time per request and alert the operations team if average latency exceeds 5 seconds (indicates API issues or overload).
3. **Build an AI usage dashboard** — show total AI API calls per day/month, average response time, and total cost to date, allowing the operations team to monitor budget consumption.
4. **Test Tarash Zone isolation thoroughly** — verify through independent testing that absolutely no data from Tarash Zone sessions is stored anywhere in the system.
5. **Create a fallback message for AI unavailability** — a warm, human-feeling message that appears when the AI cannot respond, directing users to alternative support resources rather than showing a cold error.
