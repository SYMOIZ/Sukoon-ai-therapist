# Subscription Plans — Sukoon AI

**Section:** 06 — Business Model  
**Document:** SUBSCRIPTION_PLANS.md  
**Audience:** Founders, Product Team, Marketing Team, Investors, Admin Team

---

## Executive Summary

Sukoon AI uses a freemium subscription model with four tiers: Free, Basic, Standard, and Premium (also called Enterprise for institutional buyers). Each tier unlocks progressively more access to AI chat, journal entries, and premium platform features. The subscription model is the primary mechanism for converting new users into paying customers and for driving long-term revenue through monthly renewals.

---

## Purpose

To define all subscription plans, their feature inclusions, limits, pricing rationale, and the lifecycle that governs a subscription from purchase to expiry.

---

## Stakeholders

- Founders (plan design decisions)
- Product team (feature gating implementation)
- Marketing team (positioning and promotion)
- Admin team (manual subscription activation)
- Investors (revenue model details)

---

## 1. Subscription Tier Overview

| Tier | Monthly Fee | Best For |
|---|---|---|
| **Free** | PKR 0 | New users; exploring the platform |
| **Basic** | Low monthly fee | Regular AI chat users with modest usage |
| **Standard** | Mid monthly fee | Active users needing more AI interactions and full features |
| **Premium / Enterprise** | Higher monthly fee | Power users; institutional or organizational use |

*Note: Specific pricing amounts are set by the operations/business team and managed in the admin subscription plan configuration.*

---

## 2. Free Tier

### What It Includes
- Access to AI chat with a **daily message limit**
- Access to journal with a **daily entry limit**
- Access to Therapist Directory (browse only)
- Access to mood check-ins
- Basic profile and settings

### What It Does Not Include
- Unlimited AI chat
- Full journal access
- Priority support
- Premium features (extended memory, advanced analytics)

### Purpose of the Free Tier
The free tier serves as a **trial and acquisition mechanism**:
- Users can experience the core value of the platform without payment
- Usage limits are carefully calibrated to demonstrate value without satisfying all needs
- Upgrade prompts appear when users hit their daily limits

### Conversion Goal
The primary goal of the free tier is to convert users to **Basic** after 2–4 weeks of engagement, once they have experienced the platform's value and hit their usage caps.

---

## 3. Basic Plan

### What It Includes
- Significantly increased AI chat message limit (daily or monthly)
- Increased journal entry limit
- Access to all standard features
- Standard support access

### Target User
A user who chats with the AI regularly (multiple times per week) and values the journaling experience as a habit, but does not need unlimited access.

---

## 4. Standard Plan

### What It Includes
- High AI chat message limit (approaching unlimited for most users)
- High journal entry limit (approaching unlimited for most users)
- Access to all features including gamification rewards and loyalty points
- Priority support response
- Full access to subscription-gated features

### Target User
An active mental health platform user who engages daily, journals regularly, has or is seeking a therapist connection, and considers the platform a meaningful part of their wellbeing routine.

---

## 5. Premium / Enterprise Plan

### What It Includes
- Unlimited AI chat messages
- Unlimited journal entries
- All platform features at maximum access
- VIP support
- Option for organizational / institutional purchase (multiple users under one account for clinics, companies, schools)

### Target User
Individual power users who want zero limitations; or organizations (employers, schools, clinics) that want to provide Sukoon AI access to their members or employees as a wellness benefit.

---

## 6. Feature Access Matrix

| Feature | Free | Basic | Standard | Premium |
|---|---|---|---|---|
| AI Chat messages/day | Limited | More | High | Unlimited |
| Journal entries/day | Limited | More | High | Unlimited |
| Therapist Directory (view) | Yes | Yes | Yes | Yes |
| Book therapy sessions | Yes | Yes | Yes | Yes |
| Mood check-ins | Yes | Yes | Yes | Yes |
| Gamification & Badges | Limited | Yes | Yes | Yes |
| Loyalty Points | No | Yes | Yes | Yes |
| Priority Support | No | No | Yes | Yes |
| AI Memory depth | Basic | Standard | Enhanced | Maximum |
| Dedicated account manager | No | No | No | Yes (Enterprise) |

---

## 7. Subscription Lifecycle

### Step 1 — User Selects a Plan
User navigates to the **Plans** page and selects a subscription tier.

### Step 2 — Payment
User makes payment through the available payment method:
- Currently: Bank transfer or mobile payment with screenshot and transaction ID
- Future: Automated payment gateway (recommended)

### Step 3 — Admin Verification
Admin team receives notification of subscription payment submission. Admin reviews the payment proof and activates the subscription.

### Step 4 — Subscription Activated
- User's account is updated with the new plan tier
- Feature limits are immediately unlocked
- Subscription start date and expiry date are recorded
- User receives a confirmation notification

### Step 5 — Active Subscription Period
User enjoys full access to their plan features until the expiry date.

### Step 6 — Renewal
- Before expiry, user receives a renewal reminder notification
- User must manually re-submit payment and trigger the renewal cycle
- There is no automatic recurring billing in the current model (manual model limitation)

### Step 7 — Expiry / Downgrade
- When the subscription expires and is not renewed, the user's access reverts to **Free tier**
- Features not available on the free tier become unavailable
- The user's data (chat history, journal entries) is preserved
- The user can re-subscribe at any time

---

## 8. Admin Subscription Management

From the Admin Dashboard, admins can:
- View all active subscriptions
- Manually activate a new subscription
- Extend an existing subscription (for courtesy extensions or disputed renewals)
- Deactivate a subscription (for fraud or non-payment)
- Create, edit, or disable subscription plan tiers

---

## 9. Subscription Cancellation

Users who want to cancel their subscription:
- Submit a support ticket requesting cancellation
- Admin reviews and confirms cancellation
- User reverts to free tier upon expiry of the current paid period (cancellation does not generate a refund for the current period unless admin approves)

---

## Process Flow (Subscription Lifecycle)

```
User Browses Plans Page
        │
        ▼
Selects Desired Plan
        │
        ▼
Makes Payment (bank transfer / mobile)
        │
        ▼
Uploads Screenshot + Transaction ID
        │
        ▼
Admin Verifies Payment
        │
  Approved → Subscription Activated
  Rejected → User Notified; Payment Resubmission
        │
        ▼
User Enjoys Full Feature Access
        │
        ▼
Renewal Reminder (before expiry)
        │
        ▼
User Renews Payment or
Subscription Expires → Reverts to Free
```

---

## Business Impact

| Subscription Feature | Business Significance |
|---|---|
| **Freemium entry** | Low barrier to entry; high acquisition volume |
| **Usage limits driving upgrade** | Natural conversion mechanism as users see value |
| **Monthly renewal model** | Predictable recurring revenue stream |
| **Enterprise tier** | High-value contracts for organizational wellness programs |
| **Admin-controlled activation** | Complete oversight and fraud prevention |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Low conversion rate** | Users stay on free indefinitely | Optimize free tier limits; improve upgrade prompts |
| **Low renewal rate** | Subscribers don't return after first month | Engagement programs; renewal reminders; demonstrable value |
| **Manual activation bottleneck** | Admin must verify every subscription payment | Automate with payment gateway |
| **No auto-renewal** | Users forget to renew; revenue interrupted | Proactive renewal reminders; offer annual subscriptions at discount |
| **Abuse of free tier** | Users create multiple free accounts to avoid paying | Email verification; account linking detection |

---

## Recommendations

1. **Define specific plan prices** and test them with potential users through pricing research — pricing is the single most important lever for conversion rate.
2. **Design the free tier limits carefully** — too restrictive drives users away; too generous removes upgrade motivation. Recommend: free users get 5–10 AI messages/day, enough to experience value but not enough for daily habit formation.
3. **Introduce annual subscription discounts** (e.g., 20% off vs. monthly) to improve cash flow, reduce churn, and reward committed users.
4. **Build automated renewal reminders** — 7 days, 3 days, and 1 day before expiry — reducing revenue loss from forgotten renewals.
5. **Develop an enterprise sales process** — create a dedicated enterprise plan page, a contact form for bulk/institutional inquiries, and a pricing proposal template for schools, employers, and clinics.
