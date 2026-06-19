# Revenue Model — Sukoon AI

**Section:** 06 — Business Model  
**Document:** REVENUE_MODEL.md  
**Audience:** Founders, Investors, Finance Team, Executive Team

---

## Executive Summary

Sukoon AI generates revenue through two primary channels: a commission on every therapy session payment processed through the platform (15% of the session fee), and recurring subscription fees from clients who pay for premium access to AI features and platform capabilities. A secondary revenue stream exists through therapist-facing paid features (Boost and Pro subscriptions). The model is designed to grow proportionally with user and therapist activity — the more sessions delivered and the more subscribers retained, the higher the revenue.

---

## Purpose

To document the complete revenue model of the Sukoon AI platform, including all revenue streams, the logic behind each stream, and how they interact to create a sustainable business.

---

## Stakeholders

- Founders (business model decisions)
- Investors (revenue visibility and growth potential)
- Finance team (revenue tracking and reporting)
- Executive team (strategic planning)

---

## 1. Revenue Stream 1 — Session Commission

### How It Works
Every therapy session on the platform has a **session fee** set by the therapist. When a client pays for a session and the payment is verified by the admin team:
- **85%** of the session fee goes to the therapist (credited to their wallet)
- **15%** is retained by the platform as commission (gross revenue)

### Example
| Session Fee | Therapist Gets | Platform Gets |
|---|---|---|
| PKR 1,000 | PKR 850 (85%) | PKR 150 (15%) |
| PKR 2,000 | PKR 1,700 (85%) | PKR 300 (15%) |
| PKR 3,000 | PKR 2,550 (85%) | PKR 450 (15%) |

### Revenue Driver
Session commission revenue scales with:
- Number of active therapists (session supply)
- Number of active clients with approved bookings (session demand)
- Average session fee set by therapists
- Session completion rate

### Current Payment Model
Session payments are currently collected manually — clients upload a payment screenshot and transaction ID, and an admin verifies each payment. This creates operational overhead but requires no payment gateway integration costs at launch.

**This manual model is a significant operational bottleneck and is recommended for automation as a near-term priority.**

---

## 2. Revenue Stream 2 — Client Subscription Fees

### How It Works
Clients access the platform under a **freemium model** with four subscription tiers:

| Tier | Price (indicative) | Target User |
|---|---|---|
| **Free** | PKR 0 | Trial users; casual explorers |
| **Basic** | Monthly fee | Regular AI chat users |
| **Standard** | Monthly fee | Users with moderate therapy + AI needs |
| **Premium / Enterprise** | Monthly fee | Power users; institutional use |

Higher tiers unlock:
- More AI chat messages per day/month
- More journal entries per day/month
- Access to premium features (extended memory, priority support)

### Revenue Driver
Subscription revenue scales with:
- Total registered user count
- Free-to-paid conversion rate
- Monthly subscription renewal rate (retention)
- Effectiveness of subscription tier design in creating upgrade demand

### Current Payment Model
Subscriptions are currently paid manually (screenshot + transaction ID) and activated by the admin team. This limits subscription scalability and is recommended for payment gateway integration.

---

## 3. Revenue Stream 3 — Therapist-Facing Features (Secondary)

### Boost Subscription
Therapists can pay for a **Boost** subscription to increase their visibility in the Therapist Directory:
- Basic Boost: Standard listing (default)
- Professional Boost: Featured/highlighted placement, appearing higher in search results

### Pro Subscription
Therapists can pay for a **Pro** subscription to unlock additional platform features available to premium therapists.

Both Boost and Pro subscriptions are managed by the admin team and represent a secondary revenue stream — fees paid by supply-side participants (therapists) rather than demand-side (clients).

---

## 4. Revenue Model Summary

| Revenue Stream | Type | Current Collection Method | Scale Lever |
|---|---|---|---|
| **Session Commission (15%)** | Transaction fee | Manual payment verification | Sessions × avg fee |
| **Client Subscriptions** | Recurring revenue | Manual payment verification | Users × retention |
| **Therapist Boost** | Feature fee | Admin-managed | Active therapist count |
| **Therapist Pro** | Feature fee | Admin-managed | Active therapist count |

---

## 5. Unit Economics

### Per-Session Economics

| Variable | Value |
|---|---|
| Average session fee (example) | PKR 1,500 |
| Platform commission (15%) | PKR 225 |
| Admin verification cost per session | ~PKR 50 (estimated labor) |
| Net revenue per session (approx) | PKR 175 |

### Per-Subscriber Economics (Monthly)

| Variable | Basic Example |
|---|---|
| Monthly subscription fee | PKR 500 |
| AI API cost per subscriber | ~PKR 30–60 (varies with usage) |
| Support cost per subscriber | ~PKR 20 (estimated) |
| Net revenue per subscriber (approx) | PKR 420–450 |

---

## 6. Revenue Growth Levers

| Lever | Description |
|---|---|
| **More therapists** | Each new active therapist adds booking capacity and session supply |
| **More clients** | Each new client is a potential subscriber and session buyer |
| **Higher session volume** | More sessions per active client × therapist |
| **Improved conversion rate** | Higher % of free users upgrading to paid plans |
| **Reduced payment friction** | Payment gateway reduces drop-off during checkout |
| **Subscription renewal rate** | Keeping subscribers longer increases lifetime value |
| **Higher average session fee** | Attracting senior/specialist therapists raises per-session commission |

---

## 7. Revenue Protection Mechanisms

| Risk | Protection |
|---|---|
| **Session payment fraud** | Manual admin verification of every payment screenshot |
| **Subscription without payment** | Admin activation required; no automatic access without verification |
| **Therapist payout before earning** | Payouts only processed for verified, completed sessions |
| **Chargebacks** | Manual payment model means no credit card chargebacks; bank transfers are typically irreversible |

---

## Process Flow (Revenue Cycle)

```
CLIENT PAYS SESSION FEE
        │
        ▼
Screenshot + Transaction ID Submitted
        │
        ▼
Admin Verifies Payment
        │
        ▼
Session Confirmed
Therapist Wallet Credited (85%)
Platform Commission Recorded (15%)
        │
        ▼
Therapist Requests Payout (bi-weekly/monthly)
        │
        ▼
Admin Processes Payout
Net Revenue Realized

CLIENT SUBSCRIBES
        │
        ▼
Client Submits Payment Proof
        │
        ▼
Admin Verifies → Subscription Activated
Subscription Revenue Recorded
```

---

## Business Impact

| Revenue Component | Business Significance |
|---|---|
| **Session commission** | Scales with therapy demand; directly tied to platform clinical value |
| **Subscriptions** | Provides predictable recurring revenue base |
| **Therapist fees** | Supplementary income; incentivizes supply-side growth |
| **Combined model** | Two-sided marketplace economics with strong network effects |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Low session volume** | Commission revenue too small to sustain operations | Marketing investment; therapist recruitment; AI chat to drive engagement |
| **High churn** | Subscribers cancel after first month | Engagement features (gamification, progress tracking); excellent AI quality |
| **Manual payment bottleneck** | Slow payment verification slows revenue cycle | Priority: payment gateway integration |
| **Session commission squeeze** | Therapists leave if commission feels too high | Monitor therapist sentiment; benchmark against competitors |
| **Free tier over-use** | Users stay on free forever | Well-designed free tier limits that create upgrade demand without frustrating users |

---

## Recommendations

1. **Prioritize payment gateway integration** — this is the single action most likely to increase revenue velocity by reducing friction in both session payment and subscription checkout.
2. **Set explicit pricing for all subscription tiers** and publish them clearly in the platform — unclear pricing reduces conversion.
3. **Build a subscription retention program** — remind users of their plan benefits before renewal, and offer a loyalty discount for annual subscriptions.
4. **Track revenue per active user (ARPU)** monthly — this single metric captures both session commission and subscription contributions and is the clearest signal of monetization health.
5. **Model the "therapist quality → session value" flywheel** — investing in higher-quality therapist recruitment increases average session fees, increasing commission per session without changing the commission rate.
