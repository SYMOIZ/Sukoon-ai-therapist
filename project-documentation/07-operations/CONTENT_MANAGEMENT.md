# Content Management — Sukoon AI

**Section:** 07 — Operations  
**Document:** CONTENT_MANAGEMENT.md  
**Audience:** Operations Team, Admin Team, Clinical Advisors, Product Team

---

## Executive Summary

Content management on Sukoon AI covers the administration and governance of all content that reaches users — including the AI persona and system prompt, broadcast messages, subscription plan descriptions, mood check-in pools, and any educational or wellness content surfaced by the platform. High-quality, clinically appropriate content is foundational to the platform's credibility and therapeutic value. This document defines what content is managed, by whom, and through what processes.

---

## Purpose

To establish clear ownership and processes for all content types on the Sukoon AI platform — ensuring content is accurate, appropriate, culturally sensitive, and clinically sound.

---

## Stakeholders

- Operations team (content publishing and maintenance)
- Clinical advisors (clinical accuracy review)
- Admin team (broadcast content)
- Product team (feature-integrated content)
- Founders (brand voice and standards)

---

## 1. Types of Content on the Platform

| Content Type | Where It Appears | Who Manages It |
|---|---|---|
| **AI System Prompt** | AI chat backend | Founders + Clinical Advisor |
| **Crisis Keyword List** | Crisis detection system | Clinical Advisor + Admin Lead |
| **Broadcast Messages** | All user inboxes | Admin Team |
| **Subscription Plan Descriptions** | Plans page | Operations Team |
| **Mood Check-In Questions** | Daily check-in feature | Clinical Advisor + Product Team |
| **Notification Templates** | System notifications | Product + Operations Team |
| **Support Ticket Response Templates** | Support communications | Support Lead |
| **Platform Information Pages** | About, Status, Credits pages | Operations Team |
| **Therapist Directory Listings** | Directory | Therapists (self-managed) + Admin approval |
| **System Alerts** | Admin broadcasts | Admin Team |

---

## 2. AI System Prompt Management

### What It Is
The AI system prompt is the set of instructions that defines the Sukoon AI assistant's personality, scope, limitations, and ethical boundaries. It is the most important piece of content on the platform — every AI interaction is shaped by it.

### What It Governs
- AI persona (name, tone, personality)
- Topic scope (what the AI will and will not discuss)
- Crisis response instructions
- Cultural sensitivity guidelines
- Language and communication style
- Ethical boundaries (no diagnoses, no medication advice, etc.)

### Who Controls It
- **Clinical Advisor**: Sets and approves clinical parameters
- **Founders**: Approve persona and brand voice
- **Technical Lead**: Implements changes in the configuration

### Review Cadence
The system prompt should be reviewed:
- Quarterly (standard review)
- After any significant AI safety incident
- When platform context changes materially (new features, new markets)

### Change Process
1. Proposed change is documented with reason
2. Clinical advisor reviews for clinical safety
3. Founders approve for brand alignment
4. Technical lead implements the change
5. Testing session conducted with the updated prompt before live deployment
6. Change is logged with date and version

---

## 3. Crisis Keyword List Management

### What It Is
The list of words and phrases that trigger the crisis detection system when found in a user's AI chat message.

### Who Controls It
- **Clinical Advisor**: Primary authority on what constitutes crisis language
- **Admin Lead**: Operational oversight and update requests

### Review Cadence
- Quarterly review with the clinical advisor
- Immediate review if a crisis is reported that the system missed (false negative)

### Change Process
1. Clinical advisor identifies new keywords or phrases to add/remove
2. Admin lead documents the proposed change
3. Technical lead updates the keyword list in the configuration
4. Change is tested by sending a test message with the new keyword
5. Change is logged

---

## 4. Broadcast Message Management

### What It Is
The admin team can send platform-wide messages to all users, or to targeted groups (all clients, all therapists). Broadcasts appear as notifications in user inboxes.

### Broadcast Types
| Type | Use Case |
|---|---|
| **Informational** | Platform updates, new features, policy changes |
| **Warning** | Scheduled maintenance, temporary feature unavailability |
| **Critical** | Urgent safety or policy announcements |
| **Marketing** | Promotional offers, subscription discounts |
| **Sales** | New plan announcements, feature upsells |

### Audience Targeting
- **All Users** — All clients and therapists
- **Clients Only** — Targeted at the client user base
- **Therapists Only** — Targeted at the therapist community

### Who Can Send Broadcasts
Admin team members with "Broadcast" permission. Super Admins by default.

### Approval Process (Recommended)
- Marketing or sales broadcasts require review from the Operations Manager before sending
- Critical and warning broadcasts can be sent immediately by Super Admin
- Scheduled broadcasts are drafted and queued; reviewed before send time

### Content Standards for Broadcasts
- Clear subject line stating the topic
- Body text in plain language; no jargon
- Actionable — what does the user need to do (if anything)?
- Appropriate tone for the broadcast type (critical = direct; marketing = engaging)
- No misleading claims about features or services

---

## 5. Mood Check-In Content

### What It Is
The daily mood check-in feature presents users with questions about their emotional state, energy, and focus. The question pool is curated to be:
- Clinically appropriate
- Culturally relevant
- Non-triggering
- Varied (not repetitive)

### Who Controls It
Clinical advisor and product team jointly.

### Review Cadence
- Annual review; update as needed based on user feedback.

---

## 6. Platform Information Pages

### What They Are
Static or near-static pages within the platform:
- **About Page** — What Sukoon AI is; mission; team
- **Status Page** — Platform operational status (uptime, incidents)
- **Credits Page** — Acknowledgments; open-source credits

### Who Controls Them
Operations team maintains these pages. Any factual updates (new team members, status changes) are made by operations staff with admin access.

---

## 7. Therapist Profile Content

### What It Is
Each therapist's public-facing profile content: photo, biography, specializations, and pricing.

### Who Controls It
Therapists write and manage their own profiles. Admins can:
- Review profiles for inappropriate or misleading content
- Request profile updates from therapists
- Edit a profile in exceptional circumstances (e.g., therapist is temporarily unreachable but a factual error needs correction)

### Content Standards
Therapist profiles must:
- Use professional, accurate language
- Not claim certifications or specializations not verified through the application
- Not include personal contact information (to keep all communication on-platform)
- Not contain promotional language that could be considered misleading

---

## 8. Notification Templates

System-generated notifications are pre-written templates triggered by platform events (booking confirmed, payment approved, payout processed, etc.).

### Who Controls Them
Product team drafts; operations team maintains and updates.

### Content Standards
- Direct and specific (tell the user exactly what happened)
- Warm but not informal
- Include relevant action link if any action is needed

---

## Content Review Schedule

| Content Type | Review Frequency | Owner |
|---|---|---|
| AI System Prompt | Quarterly | Clinical Advisor + Founders |
| Crisis Keyword List | Quarterly | Clinical Advisor |
| Subscription Plan Descriptions | Annually or on plan change | Operations |
| Mood Check-In Pool | Annually | Clinical Advisor + Product |
| Notification Templates | Annually or on feature change | Product + Operations |
| Broadcast Templates | As needed | Support Lead |
| About/Credits/Status Pages | As needed | Operations |

---

## Process Flow (Content Update)

```
Proposed Content Change Identified
        │
        ▼
Determine Content Type and Owner
        │
        ▼
Draft Change
        │
        ▼
Review (Clinical Advisor if clinical; Operations if platform)
        │
        ▼
Approval (documented)
        │
        ▼
Implementation
        │
        ▼
Testing / Verification
        │
        ▼
Change Log Updated
```

---

## Business Impact

| Content Quality | Business Impact |
|---|---|
| **AI system prompt accuracy** | Foundation of all AI quality; clinical credibility |
| **Crisis keyword completeness** | Safety system effectiveness; liability management |
| **Clear broadcast communication** | User awareness; reduced support tickets |
| **Therapist profile quality** | Directory trust; booking conversion |
| **Culturally appropriate content** | User comfort; reduced churn among target demographic |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **AI prompt drift** | Undocumented changes break clinical safety | Version-controlled prompt with mandatory review |
| **Broadcast tone errors** | Marketing message sent in crisis tone; or vice versa | Pre-send review for all broadcasts |
| **Outdated crisis keywords** | New crisis language patterns not captured | Quarterly clinical review |
| **Therapist profile misinformation** | Unverified claims in profiles | Admin review of profiles; credential cross-check at approval |
| **Inconsistent brand voice** | Different team members create inconsistent content | Brand voice guidelines document; centralized template library |

---

## Recommendations

1. **Create a Brand Voice Guide** — a 1–2 page document defining the platform's tone, personality, and communication standards. Anyone creating content should refer to it.
2. **Implement a content change log** — a shared document (or system feature) recording every change to the AI prompt, crisis keywords, and broadcast templates, with date, change description, and approver.
3. **Establish a clinical content review partnership** — formalize the relationship with a clinical advisor so content reviews happen on schedule, not ad-hoc.
4. **Build a content preview function** — allow admins to preview how a broadcast will appear to users before sending, reducing accidental formatting or content errors.
5. **Create a content audit process** — an annual review of all platform-facing content (profile templates, notification templates, AI prompt, check-in questions) to ensure nothing is outdated, inaccurate, or no longer appropriate.
