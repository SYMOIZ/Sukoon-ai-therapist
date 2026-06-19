# Client Features — Sukoon AI

**Section:** 02 — Client App  
**Document:** CLIENT_FEATURES.md  
**Audience:** Product Team, Marketing, Customer Support, Therapists, Investors

---

## Executive Summary

Sukoon AI provides clients with a comprehensive suite of mental wellness features spanning AI-powered conversation, personal journaling, human therapist booking, crisis support, and habit-building tools. This document describes every feature available to clients, its purpose, and its business value.

---

## Purpose

To provide a complete reference of all features available to Sukoon AI clients, enabling product decisions, marketing messaging, support responses, and investor briefings.

---

## Stakeholders

- Product and design teams (feature prioritization)
- Marketing team (feature communication)
- Customer support (answering feature questions)
- Investors (evaluating product completeness)

---

## Feature 1: AI Therapy Chat

### What It Is
The core feature of the platform. A private, real-time conversation with Sukoon's AI therapist, available 24/7.

### What It Does
- Engages users in professional, emotionally supportive conversation
- Asks structured check-in questions at the start of each session
- Responds in the user's preferred language and tone
- Builds a running understanding of the user's emotional patterns (when memory is enabled)
- Detects crisis signals in every message and responds appropriately
- Never diagnoses, prescribes medication, or makes clinical claims

### Modes Available
| Mode | Description |
|---|---|
| **Standard Chat** | Normal session with memory enabled, full personalization |
| **Tarash Zone** | Completely private mode — no data saved, no analysis run |
| **Community Mode** | Anonymous group-style interaction (no personal data shared) |
| **Therapist Mini-Chat** | Limited preview conversation (10–20 messages) before booking |

### Session Check-In
Each session begins with one rotating check-in question from three categories:
- **Emotional State** ("How have your emotions felt most of today?")
- **Energy and Connection** ("Did you feel more connected or more distant today?")
- **Mood Influence** ("What influenced your mood the most today?")

### Voice Features
- **Voice Input** — Users can speak their message instead of typing
- **Audio Playback** — AI responses can be read aloud

### Usage Limits
The number of AI chat sessions available depends on the user's subscription plan. Free-tier users have a capped number of sessions per month. Paid subscribers receive higher or unlimited access.

---

## Feature 2: Personal Journal

### What It Is
A private digital diary for emotional reflection and mood tracking.

### What It Does
- Allows users to write dated journal entries with a title, body text, and mood label
- Stores all entries securely with the user's account
- Displays entries in reverse chronological order
- Enables mood trend tracking over time

### Mood Options
Happy, Calm, Neutral, Sad, Anxious, Frustrated

### Journal Entry Limits
Free-tier users have a monthly cap on new journal entries. Paid subscribers receive higher or unlimited journal access.

### Mood Trend Monitoring
The platform quietly monitors the mood tags from journal entries. If a user records predominantly negative moods (Sad, Anxious, Stressed, Frustrated) across five or more recent entries, a supportive notification is automatically triggered, suggesting a therapy session or breathing exercise.

---

## Feature 3: Therapist Directory

### What It Is
A searchable, browsable listing of all active licensed therapists on the platform.

### What It Does
Displays each therapist's:
- Name, photo, and specialty
- Biography and clinical approach
- Years of clinical experience
- Star rating (out of 5) and number of verified reviews
- Languages spoken
- Crisis certification badge (if applicable)
- Available booking slots
- Session pricing (per session type and duration)
- Boost status (highlighted or featured in search)

### Filtering and Matching
Users can filter therapists by specialty, language, or availability. The platform also provides premium matching for subscribed users, suggesting the best-fit therapist based on the user's profile, language, and presenting concerns.

---

## Feature 4: Session Booking

### What It Is
The process through which a client schedules and pays for a session with a licensed therapist.

### Session Types
| Type | Description |
|---|---|
| **Audio** | Voice call session |
| **Video** | Video call session |
| **Chat/Text** | Text-based therapeutic session |

### Session Durations
Therapists offer sessions in standard durations (typically 45, 60, or 90 minutes). Duration and pricing are set by each therapist.

### Booking Process
1. Select therapist and available time slot
2. Choose session type and duration
3. Review the fee
4. Upload payment screenshot and transaction ID
5. Await admin payment verification
6. Receive session confirmation notification

### Booking Status Tracking
Users can see the live status of all their bookings in the Dashboard and Notifications section.

---

## Feature 5: Direct Messaging with Therapist

### What It Is
A private messaging channel between a client and their connected therapist.

### When It's Available
Direct messaging is available once a therapist-client connection has been established (after a confirmed session booking).

### What It Allows
- Sending follow-up questions between sessions
- Receiving therapist notes or homework assignments
- Checking appointment details
- Therapist responding with guidance between sessions

---

## Feature 6: Notifications

### What It Is
An in-platform notification system that keeps users informed about bookings, moods, safety, and platform updates.

### Notification Types
| Type | Trigger |
|---|---|
| **Meeting / Booking** | Session confirmation, payment approval, cancellation |
| **System** | Account actions, plan renewals, platform updates |
| **Alert** | Clinical alerts, mood interventions |
| **Broadcast** | Admin-sent messages to all users or specific audiences |
| **Info / Warning / Critical** | Graduated severity communications |
| **Marketing / Sales** | Promotional offers and plan upgrades |

### Notification Center
All notifications are accessible in the **Notifications** page, where users can:
- View all notifications in reverse chronological order
- Mark individual notifications as read
- See unread counts

---

## Feature 7: Subscription and Plans

### What It Is
A tiered access system where different subscription levels unlock different platform capabilities.

### What Plans Govern
- Maximum AI chat sessions per period
- Maximum journal entries per period
- Access to priority therapist matching
- Access to premium features

### Plans Page
The **Plans Page** displays all available subscription tiers with prices, features, and durations. Users can upgrade directly from this page.

(Full subscription documentation: see CLIENT_SUBSCRIPTIONS.md)

---

## Feature 8: Profile Management

### What It Is
A personal profile page where users can view and update their identity and preferences.

### What Users Can Update
- Profile picture
- Cover image (banner)
- Biography
- Personal details (age, region, gender, profession)
- Referral code (shareable)

---

## Feature 9: Settings and Personalization

### What It Is
A settings panel where users customize how the AI interacts with them.

### Personalization Options
| Setting | Options |
|---|---|
| **Language** | English, Urdu, Roman Urdu, Sindhi, Pashto, Siraiki, Arabic, Spanish |
| **Tone** | Cute, Mature, Friendly, Soft, Calm, Direct |
| **AI Therapist Style** | Gentle, CBT (Cognitive Behavioral Therapy), Mindfulness |
| **Personality Mode** | Introvert, Extrovert |
| **Voice** | Enabled / Disabled |
| **Audio Auto-Play** | Enabled / Disabled |
| **Memory** | Enabled (AI learns about you) / Disabled (fresh each session) |
| **Dark Mode** | On / Off |

### Why Personalization Matters
These settings allow Sukoon AI to serve users across wildly different cultural and personality contexts. A 22-year-old in Lahore who wants a "Cute" and "Friendly" Urdu conversation has a fundamentally different experience from a 40-year-old professional in London who wants "Mature" and "Direct" English responses — and the platform accommodates both.

---

## Feature 10: Crisis Support

### What It Is
An emergency support system built directly into the platform, accessible at all times.

### Components
- **Emergency Overlay** — Activates automatically during AI chat when crisis language is detected
- **Crisis Modal** — Displays crisis resources in a calm, accessible format
- **Crisis Page** — A standalone page accessible without login at `/crisis-support`
- **Risk Alert Logging** — Crisis events are logged for clinical team follow-up

### Always Accessible
The Crisis Support page can be accessed by anyone — even without an account — ensuring that the most vulnerable users are never locked out of safety resources.

---

## Feature 11: Gamification and Badges

### What It Is
A wellness habit-building system using streaks and achievement badges.

### How It Works
- The platform tracks consecutive days the user engages with the platform
- Badges are awarded at milestone streak intervals
- Badges display on the user's profile and dashboard

### Purpose
Gamification is not about making mental health "fun" in a trivial sense — it is about building sustainable habits. Daily engagement with emotional reflection tools produces better mental wellness outcomes over time.

---

## Feature 12: About and Credits Pages

### About Page
Accessible to the public (without login). Provides information about the Sukoon AI platform, its mission, and the team behind it.

### Credits Page
Accessible at `/credits`. Acknowledges contributors, collaborators, and any open source or academic foundations the platform builds upon.

### Status Page
Accessible at `/status`. Provides real-time information about platform health, database connectivity, and system status — useful for operations teams.

---

## Process Flow

```
User Login
    │
    ▼
Dashboard (Mood Check-in)
    │
    ├── AI Chat ──────────────────────────── Crisis Detection
    │       └── Tarash Zone (private)              │
    │                                              ▼
    ├── Journal (entries + mood)           Crisis Response
    │
    ├── Therapist Directory
    │       └── Booking → Payment → Admin Approval → Session
    │
    ├── Notifications (all alerts)
    │
    ├── Profile & Settings
    │
    └── Plans (subscription upgrade)
```

---

## Business Impact

| Feature | Revenue Link | Retention Link |
|---|---|---|
| AI Chat | Drives subscription upgrades at session limit | Core daily engagement driver |
| Journal | Deepens emotional investment in platform | Increases session frequency |
| Therapist Booking | Direct commission revenue | Long-term care relationship |
| Notifications | Drives return visits | Re-engagement for churned users |
| Gamification | Increases daily active use | Habit formation |
| Crisis Support | Risk mitigation, brand trust | Demonstrates platform integrity |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| Feature overload | Too many options overwhelming new users | Phased feature reveal during onboarding |
| Voice quality issues | Poor audio on low-bandwidth connections | Graceful fallback to text |
| Journal privacy | Users worried about who can see entries | Clear privacy policy; entries not accessible to admins by default |
| Booking abandonment | Manual payment process causes drop-off | Future payment gateway integration |

---

## Recommendations

1. **Add AI chat history export** — Allow users to download their conversation history as a PDF for personal records or sharing with their therapist.
2. **Enable journal sharing** — Give users the option to share specific journal entries with their assigned therapist.
3. **Create a wellness streak leaderboard** — Community feature (anonymous) that motivates consistent platform engagement.
4. **Improve voice mode** — Expand to full duplex voice conversation with natural turn-taking for a more human-like AI therapy experience.
5. **Add mood analytics dashboard** — Show users a visual chart of their mood trends over 30, 60, and 90 days.
