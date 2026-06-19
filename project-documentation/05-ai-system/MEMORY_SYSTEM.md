# AI Memory System — Sukoon AI

**Section:** 05 — AI System  
**Document:** MEMORY_SYSTEM.md  
**Audience:** Founders, Investors, Clinical Advisors, Operations Team, Privacy Reviewers

---

## Executive Summary

The Sukoon AI memory system enables the AI assistant to remember meaningful information from previous conversations, creating a sense of continuity across sessions. Rather than starting from zero every time a user opens a new chat, the AI retrieves relevant memories and uses them to provide context-aware, personalized support. This document explains what the memory system stores, how it works, and how it is governed.

---

## Purpose

To describe how the AI memory system functions, what data it retains, how it respects user privacy, and what boundaries govern its operation — for clinical advisors, privacy officers, and business stakeholders.

---

## Stakeholders

- Founders and investors (understanding the personalization feature)
- Clinical advisors (ensuring memory does not create inappropriate dependency or clinical confusion)
- Privacy and compliance team (understanding what is stored and for how long)
- Product team (governing memory behavior and updates)
- Users (informed about what the AI remembers)

---

## 1. The Problem Memory Solves

Without memory, every AI chat session starts fresh. The user must re-explain:
- Their current life situation
- What they have been struggling with
- What they have tried before
- Their goals and progress

This creates friction and reduces the therapeutic value of AI conversations. Memory solves this by preserving the most relevant personal context across sessions.

---

## 2. What the Memory System Stores

The AI memory system stores **high-signal, user-relevant information** — not verbatim transcripts. Specifically, it captures:

| Type of Memory | Example |
|---|---|
| **Presenting concerns** | "User has been dealing with work-related burnout for 3 weeks" |
| **Coping strategies discussed** | "We discussed the 4-7-8 breathing exercise for anxiety" |
| **Progress notes** | "User reported improved sleep after starting journaling" |
| **Significant life events** | "User mentioned a family conflict that has been causing stress" |
| **User goals** | "User wants to work on reducing social anxiety" |
| **Preferences** | "User prefers practical exercises over theoretical discussion" |

### What Is NOT Stored
- Full verbatim transcripts of conversations (these are stored in the standard chat history, but not in the dedicated memory system)
- Medical diagnoses
- Medication information
- Information disclosed in Tarash Zone (Privacy Mode) — nothing from Tarash Zone sessions is stored

---

## 3. How the Memory System Works (RAG)

The memory system uses a technique called **Retrieval-Augmented Generation (RAG)**:

### Step 1 — Memory Creation
At the end of, or during, a conversation session, the system identifies high-signal content from the chat:
- Significant emotional events mentioned
- Coping strategies discussed or assigned
- Progress updates volunteered by the user
These are saved as discrete memory entries linked to the user's profile.

### Step 2 — Memory Retrieval
When a user starts a new conversation, the system:
1. Receives the user's first message
2. Searches the user's stored memory entries for items relevant to the current message
3. Returns the top matching memories

### Step 3 — Contextual Injection
The retrieved memories are added to the AI's context before it generates a response. The AI receives:
- The system prompt (persona and behavior instructions)
- The retrieved memory summary
- The current conversation history
- The user's latest message

This allows the AI to respond as if it recalls prior sessions naturally.

### Step 4 — New Memory Creation
If the current conversation contains new significant information, a new memory entry is created or an existing one is updated.

---

## 4. Memory Data Storage

Memory entries are stored in the platform's database linked to the user's account:

| Field | Value |
|---|---|
| **User ID** | Links memory to the correct account |
| **Memory Content** | The condensed memory note |
| **Embedding Vector** | A mathematical representation enabling semantic search |
| **Created At** | When the memory was created |
| **Source Session ID** | Which conversation session generated this memory |

Embeddings (vector representations) enable the system to find memories that are **semantically relevant** to the user's current message — not just keyword matches. For example, if a user writes about "feeling like a failure at work," the system can retrieve a memory about "imposter syndrome discussed last month" even if the words are different.

---

## 5. Memory Relevance and Accuracy

### Memory Decay (Recommended)
Not all memories should be treated equally over time:
- Recent memories (last 30 days) are generally more relevant
- Older memories (6+ months) may reflect a state that has changed significantly

The system should apply a recency weight when retrieving memories, giving preference to more recent entries while still surfacing older ones if highly relevant.

### Memory Accuracy Risk
The AI may occasionally reference a memory in a way that feels intrusive or inaccurate if:
- The user's situation has changed significantly since the memory was created
- The memory was imprecisely captured

Users should be able to flag incorrect AI recollections through the support system.

---

## 6. User Control Over Memory

Users have the following rights regarding their AI memory:

| Right | How It Is Exercised |
|---|---|
| **Know what is stored** | Memory summary viewable in account settings (recommended feature) |
| **Clear all memories** | Option to "Reset AI Memory" in settings |
| **Use Tarash Zone** | Privacy mode where nothing is saved during a session |
| **Request memory deletion** | Via support ticket |

---

## 7. Tarash Zone and Memory

The **Tarash Zone** is a named privacy mode during AI chat that completely disables memory:
- Nothing typed in a Tarash Zone session is saved to the database
- No memory entries are created from Tarash Zone sessions
- The AI still responds within the session, but no cross-session retention occurs
- Tarash Zone sessions do not appear in the user's standard chat history

This is a deliberate design choice to allow users to speak freely about the most sensitive topics — knowing that the conversation is ephemeral.

---

## Process Flow (Memory Lifecycle)

```
User Opens Chat Session
        │
        ▼
Tarash Zone Active?
  ├── YES → No storage; no memory creation
  └── NO  → Memory retrieval begins
             │
             ▼
        User's First Message
             │
             ▼
        Semantic Search of User Memory Store
             │
             ▼
        Top Relevant Memories Retrieved
             │
             ▼
        AI Context Built (system prompt + memories + history + message)
             │
             ▼
        Gemini Generates Response
             │
             ▼
        Response Delivered
             │
             ▼
        High-Signal Content Detected?
          ├── YES → New Memory Created / Existing Updated
          └── NO  → Session ends; no new memory
```

---

## Business Impact

| Memory Feature | Business Value |
|---|---|
| **Cross-session continuity** | Differentiates from generic AI chatbots; increases perceived AI intelligence |
| **Personalized responses** | Higher user satisfaction; stronger emotional connection to the product |
| **Progress tracking through memory** | Motivates users by showing growth; increases session depth |
| **Tarash Zone** | Builds user trust through demonstrated privacy commitment |
| **RAG efficiency** | AI only sees relevant memories, reducing cost and improving response relevance |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Inaccurate memory** | AI references outdated or incorrect information | Allow users to view and clear memories |
| **Privacy breach** | Memory data exposed through security vulnerability | Encryption at rest; access controls; audit logs |
| **Intrusive AI behavior** | AI references sensitive memories at inappropriate moments | Memory injection controlled by relevance threshold |
| **Memory over-accumulation** | Thousands of entries slow retrieval | Periodic memory consolidation and pruning |
| **Tarash Zone failure** | A technical error causes Tarash Zone sessions to be stored | Tarash Zone mode must disable all write operations at session level; tested thoroughly |

---

## Recommendations

1. **Build a "My AI Memory" view** in user settings where users can see all their stored memory entries and delete individual ones or clear all — building transparency and trust.
2. **Implement memory consolidation** — rather than accumulating thousands of individual entries, periodically summarize related memories into a single condensed profile entry (e.g., monthly).
3. **Add a memory relevance threshold** — only inject a memory into the AI context if its similarity score exceeds a defined threshold, preventing irrelevant or outdated memories from confusing the AI.
4. **Conduct quarterly memory audits** — review a sample of stored memories to ensure the system is capturing meaningful content and not storing trivial or sensitive information inappropriately.
5. **Publish a plain-English "What Your AI Remembers" policy** in the app's privacy section — explaining in simple language what the memory system stores, what it does not store, and how users can control it.
