# Client Journey — Sukoon AI

**Section:** 02 — Client App  
**Document:** CLIENT_JOURNEY.md  
**Audience:** Product Team, Marketing, Customer Support, Investors

---

## Executive Summary

The Sukoon AI client journey takes a person from their first visit to the platform through registration, emotional exploration with AI, therapist discovery and booking, long-term wellness habits, and crisis management. The journey is designed to be frictionless for new users while deepening engagement as the relationship grows. This document maps every stage of the client lifecycle.

---

## Purpose

To provide a clear, stage-by-stage map of how a client experiences the Sukoon AI platform — from first awareness through ongoing engagement and off-boarding — enabling product, marketing, and support teams to design around real user needs.

---

## Stakeholders

- Product and Design teams (user experience decisions)
- Marketing team (acquisition and retention messaging)
- Customer Support (understanding where users need help)
- Clinical team (identifying where care continuity matters most)
- Investors (evaluating product stickiness and retention)

---

## Stage 1: Discovery and First Visit

### Entry Point
A new user arrives at the Sukoon AI platform — likely through word of mouth, social media, or a search for mental health support in their language.

### What They See
The **Welcome Page** is the first screen. It presents:
- A brief, warm description of Sukoon AI
- Two options: **Sign Up** (full account) or **Try Anonymously**
- A **"Continue with Google"** button for one-tap registration
- A link to the Terms of Service
- A link to the **About** and **Crisis Support** pages (accessible without logging in)

### Anonymous Access
Users who are not ready to commit can use the platform anonymously. Anonymous users access the AI chat immediately without providing any personal details. This lowers the barrier for users who are cautious about privacy. Anonymous sessions do not save history, cannot book therapists, and cannot access subscription features.

### Key Insight
The anonymous option is strategically important. It allows users experiencing stigma about seeking help to try the platform without any identity commitment — increasing the likelihood they will eventually register.

---

## Stage 2: Registration

### Standard Registration
A user chooses to create a full account. They provide:

1. **Email address** and **password** (or sign in with Google)
2. **Display name** (how they appear in the platform)
3. **Age** (used for age-appropriate AI responses)
4. **Region** (country or city)
5. **Gender** (Male, Female, Other, or "Prefer not to say")
6. **Profession** (Client, Working Professional, Both, or Other)
7. **Preferred Language** — chosen from: English, Urdu, Roman Urdu, Sindhi, Pashto, Siraiki, Arabic, Spanish
8. **Tone Preference** — how they want the AI to communicate: Cute, Mature, Friendly, Soft, Calm, or Direct

### Post-Registration
After registration:
- The user is logged in and redirected to their **Dashboard**
- A welcome notification is sent
- A default free subscription is active
- The AI chat and journal are immediately accessible

### Referral System
The platform supports referral codes. If a user registers using another user's referral code, both parties may receive rewards (reward points).

---

## Stage 3: First Experience — Dashboard

### Dashboard Overview
The **Dashboard** is the user's home screen after login. It displays:
- A mood check-in prompt ("How are you feeling today?")
- Quick access to AI chat
- Journal entry shortcuts
- Active therapist connections
- Upcoming session reminders
- Wellness streak and badge progress

### Mood Check-In
At the start of each session, the platform prompts the user with one emotional check-in question drawn from rotating question pools. Questions ask about:
- How their emotions felt during the day
- Their energy and social presence
- What influenced their mood most strongly

This mood data is stored and used to personalize AI responses and may trigger wellness notifications if negative patterns are detected.

---

## Stage 4: AI Chat Experience

### Starting a Chat
The user navigates to the **Chat** section. They can:
- Start a new conversation session
- Continue from where they left off (if conversation history is saved)
- Select the type of session (standard or "Tarash Zone" private mode)

### During the Chat
The AI therapist ("Sukoon AI") engages the user in a professional, emotionally intelligent conversation. The AI:
- Asks one focused question at a time
- Never diagnoses or prescribes
- Avoids slang, emojis, or casual language
- Maintains a calm, non-judgmental professional tone
- Responds in the user's chosen language
- Adapts tone based on the user's preference (Friendly, Calm, Mature, etc.)

### Tarash Zone (Private Mode)
A special privacy mode called the **Tarash Zone** allows users to express themselves without any data being saved or analyzed. When entered:
- The AI confirms: *"This is the Tarash Zone. Nothing written here will be saved or used for analysis. You may express yourself freely."*
- No AI memory updates occur
- No analytics are run
- The conversation is completely ephemeral

### Voice Features
The platform includes voice input (speech-to-text) and audio playback (text-to-speech) for AI responses — making the experience accessible for users who prefer to speak rather than type.

### Crisis Detection During Chat
Every message sent by the user is scanned for crisis language patterns. If a crisis signal is detected, the conversation is automatically interrupted and the **Emergency Overlay** or **Crisis Modal** is displayed. (See Stage 7 for full crisis journey.)

---

## Stage 5: Journal Experience

### Accessing the Journal
Users navigate to the **Journal** section. Here they can:
- Create a new journal entry with a **title**, **content**, and **mood tag**
- View past entries in chronological order
- Browse entries by mood
- Delete entries

### Journal Entry
A journal entry includes:
- **Title** (short label for the entry)
- **Content** (full text — no length limit)
- **Mood** — chosen from: Happy, Calm, Neutral, Sad, Anxious, Frustrated

### Mood Trend Analysis
The platform passively monitors journal mood trends. If a user consistently records negative moods (Sad, Anxious, Stressed, Frustrated) across multiple entries, the system automatically sends a **Mood Check-in Notification** suggesting a therapist session or mindfulness exercise. This analysis runs silently in the background.

---

## Stage 6: Discovering and Booking a Therapist

### Therapist Directory
Users can browse the **Therapist Directory** to find licensed professionals. Each therapist profile shows:
- Full name and photo
- Specialty (e.g., Anxiety, PTSD, CBT, Mindfulness)
- Bio and clinical specializations
- Years of experience
- Rating (out of 5) and number of reviews
- Languages spoken
- Crisis certification status
- Available time slots
- Session pricing

### Booking a Session
The booking process follows these steps:

**Step 1 — Select Therapist**
The user finds a therapist that matches their needs and clicks "Book Session."

**Step 2 — Choose Session Details**
- Session type: Audio, Video, or Chat
- Date and time from the therapist's available calendar slots
- Session duration (typically 45, 60, or 90 minutes)

**Step 3 — Review Fee**
The session fee is displayed clearly before confirming.

**Step 4 — Payment**
The platform does not process cards directly. The user is instructed to make a bank transfer or mobile payment and upload a **payment screenshot** along with a **transaction ID** as proof.

**Step 5 — Submission**
The booking is created with the status **"Pending Payment"** and submitted to the admin team for verification.

**Step 6 — Admin Review**
The admin team reviews the payment proof and either:
- Approves the payment (status moves to "Payment Approved" → "Therapist Assigned" → "Session Confirmed")
- Rejects the payment (status moves to "Payment Rejected" with a reason)

**Step 7 — Session**
Once confirmed, both the client and therapist are notified. The user receives a notification and can view their upcoming session in the **Dashboard** and **Notifications** section.

### Session Status Lifecycle
```
Draft → Pending Payment → Payment Under Review → Payment Approved
     → Therapist Assigned → Session Confirmed → Session Completed
                                              → Cancelled
     → Payment Rejected
```

---

## Stage 7: Crisis Support Journey

### Crisis Trigger
At any point during an AI chat, if the user writes something containing crisis language (such as "I want to die," "hurt myself," or "no reason to live"), the platform immediately activates the crisis protocol.

### Crisis Response
An **Emergency Overlay** appears with:
- Calm, supportive language
- Immediate crisis resources (emergency services number, crisis hotline, crisis text line)
- An option to continue in the safe environment

### Crisis Support Page
Accessible at any time — even without logging in — the **Crisis Support Page** provides:
- 24/7 crisis resources
- Guidance on what to do in an emergency
- Links to specialized crisis therapists on the platform

### Crisis Escalation
The risk alert is logged in the admin panel. An admin or clinical supervisor can assign a crisis-certified therapist to reach out to the user. (Full crisis workflow is documented in Section 08.)

---

## Stage 8: Notifications and Engagement

### Types of Notifications
Users receive notifications for:
- **Meeting reminders** — upcoming therapy session alerts
- **System notifications** — platform updates, account actions
- **Mood check-ins** — triggered by negative mood trends
- **Broadcasts** — platform-wide messages from admins
- **Booking updates** — payment approved, session confirmed, etc.
- **Alert notifications** — urgent clinical or safety messages

### Notification Page
All notifications are viewable in the **Notifications** section, where users can mark them as read.

---

## Stage 9: Profile and Settings Management

### Profile Page
Users can view and update:
- Profile picture and cover image
- Bio
- Personal details (age, region, gender, profession)

### Settings Page
Users can update:
- **Language preference** (8 languages)
- **Tone preference** (6 options)
- **AI therapist style** (Gentle, CBT, Mindfulness)
- **Personality mode** (Introvert / Extrovert)
- **Voice features** (enable/disable)
- **Memory** (enable/disable AI learning from their sessions)
- **Dark mode**

---

## Stage 10: Gamification and Streaks

### How Badges Work
The platform awards badges for consistent platform engagement:
- **Day 1 Badge** — "You showed up for yourself today."
- Additional badges unlock at multi-day streaks

### Wellness Dashboard
The Dashboard displays:
- Total active days
- Last active date
- Unlocked badges

These features encourage daily mental wellness check-ins and build habit loops around emotional health.

---

## Stage 11: Account Lifecycle

### Active Account
A normal, healthy account with access to all subscribed features.

### Suspended Account
An account suspended by an admin, typically for policy violations. The user sees a suspension notice and reason upon login. No platform access is available during suspension.

### Anonymous Exit
Anonymous users can close the browser at any time. No account data is retained.

### Account Deletion
Not yet formally implemented as a user-facing feature. Currently handled by the admin team upon request. (Recommended as a future feature — see Section 09.)

---

## Process Flow Summary

```
Discovery → Welcome Page
         → Anonymous Use (no account) OR Registration
                              ↓
                         Dashboard
                       ↙    ↓    ↘
               AI Chat   Journal   Therapist Directory
                 ↓          ↓             ↓
          Crisis Detection  Mood      Book Session
                 ↓       Tracking        ↓
           Crisis Response           Payment Upload
                                         ↓
                                   Admin Verification
                                         ↓
                                  Session Confirmed
                                         ↓
                                  Post-Session Care
                                  (Direct Messages,
                                  Follow-up Booking)
```

---

## Business Impact

The client journey drives three core business metrics:

1. **Activation Rate** — Percentage of registered users who complete their first AI chat session. A smooth onboarding directly impacts this.
2. **Subscription Conversion** — Users who hit the free-tier limits (AI chat cap, journal limits) are prompted to upgrade. The quality of the free experience determines conversion.
3. **Session Booking Rate** — Users who find value in the AI experience are more likely to book human therapist sessions, generating commission revenue.

---

## Risks

| Risk | Impact | Mitigation |
|---|---|---|
| High drop-off at registration | Low activation | Simplify registration; anonymous access reduces friction |
| Users not upgrading from free tier | Low revenue | Clear value communication at limit boundaries |
| Crisis missed during anonymous session | Clinical liability | Crisis detection runs even in anonymous mode |
| Language mismatch | Poor experience | Language is the first setting users configure |
| Payment process friction | Low booking completion | Streamline payment verification; consider payment gateway integration |

---

## Recommendations

1. **Add in-app payment gateway** (JazzCash, EasyPaisa, Stripe) to eliminate the manual payment screenshot process and reduce booking abandonment.
2. **Implement a post-session feedback form** that automatically appears after each session is marked "Completed."
3. **Create a re-engagement flow** for users who have not logged in for 7+ days — triggered through email or push notification.
4. **Develop an onboarding tutorial** for first-time users to reduce confusion about the AI chat vs. human therapist distinction.
5. **Add account deletion functionality** as a user-facing feature to meet privacy expectations and potential regulatory requirements.
