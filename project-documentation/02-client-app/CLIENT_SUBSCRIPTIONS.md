# Client Subscriptions — Sukoon AI

**Section:** 02 — Client App  
**Document:** CLIENT_SUBSCRIPTIONS.md  
**Audience:** Finance Team, Product Team, Marketing, Investors, Customer Support

---

## Executive Summary

Sukoon AI uses a subscription-based access model that gates certain platform capabilities behind paid tiers. Subscriptions govern how many AI chat sessions and journal entries a user can access per period, and whether they receive premium features like priority therapist matching. This document describes the subscription structure, the user experience of subscribing, and the business model behind it.

---

## Purpose

To document the complete subscription lifecycle for clients — how plans are structured, how users subscribe, what they receive, and how the subscription drives platform revenue.

---

## Stakeholders

- Finance team (revenue tracking)
- Product team (feature gating decisions)
- Marketing team (subscription conversion messaging)
- Customer support (handling subscription queries)
- Investors (revenue model understanding)

---

## 1. Subscription Philosophy

Sukoon AI follows a **freemium model with conversion incentives**:

- A **free tier** gives every user meaningful access to the platform so they can build trust and habit
- **Paid tiers** remove limits and unlock premium capabilities for users who depend on the platform deeply
- There is no time-limited free trial — the free tier is permanent, creating low-pressure entry

This model is designed for markets where users are skeptical of digital health tools and need to experience value before paying.

---

## 2. What Subscriptions Control

Each subscription plan governs four capability dimensions:

| Dimension | Description |
|---|---|
| **Max AI Chats** | Maximum number of AI therapy chat sessions per subscription period |
| **Max Journal Entries** | Maximum number of journal entries per subscription period |
| **Priority Matching** | Whether the user gets AI-assisted therapist matching based on their profile |
| **Premium Features** | Access to advanced capabilities (Deep Mode AI, enhanced memory, voice features) |

---

## 3. Plan Structure

The platform's plan structure is managed dynamically by admins through the database. The schema supports the following plan parameters:

| Parameter | Meaning |
|---|---|
| **Plan Name** | Display name (e.g., "Free", "Essential", "Premium", "Lifetime") |
| **Price** | Cost in local currency (PKR) |
| **Duration** | Months the plan is active |
| **Is Lifetime** | Whether the plan is a one-time permanent purchase |
| **Max AI Chats** | Session cap per period |
| **Max Journal Entries** | Journal cap per period |
| **Priority Matching** | On or off |
| **Premium Features** | On or off |
| **Is Active** | Whether the plan is currently offered |

### Typical Plan Tiers

While exact pricing is set by the admin team, the typical structure operates as follows:

**Free Tier**
- Access: 10 AI chat sessions per month
- 30 journal entries per month
- No priority therapist matching
- No premium features
- Price: PKR 0

**Essential Plan**
- Access: Increased AI chat limit (e.g., 50 sessions per month)
- Higher journal entry limit
- No priority matching
- Price: PKR [set by admin]
- Duration: Monthly

**Premium Plan**
- Unlimited or high-cap AI chat sessions
- Unlimited journal entries
- Priority therapist matching enabled
- Premium features enabled (Deep Mode AI, full voice, enhanced memory)
- Price: PKR [set by admin]
- Duration: Monthly

**Lifetime Plan**
- All premium features permanently
- One-time purchase
- No renewal required
- Price: PKR [set by admin]

---

## 4. How Users Subscribe

### Step 1 — Plans Page
The user navigates to the **Plans** section from the navigation menu or from a "Limit Reached" prompt.

### Step 2 — Plan Selection
The Plans page displays all active subscription tiers with their features and prices clearly listed.

### Step 3 — Payment
The platform uses a **manual payment verification** model. The user:
1. Selects a plan
2. Receives payment instructions (bank account or mobile payment details)
3. Makes the payment externally
4. Uploads a payment screenshot as proof
5. Submits for admin review

### Step 4 — Admin Verification
The finance/admin team reviews the payment screenshot. Once verified:
- The subscription is activated in the user's account
- A confirmation notification is sent to the user
- The subscription expiry date is set

### Step 5 — Active Subscription
The user now has access to the features included in their plan. The subscription status appears in their profile.

---

## 5. Subscription Status Types

| Status | Meaning |
|---|---|
| **Active** | Subscription is valid and features are accessible |
| **Expired** | Subscription period has ended; user reverts to free-tier limits |
| **Pending** | Payment submitted, awaiting admin verification |
| **Cancelled** | Subscription was cancelled by admin or user request |

---

## 6. Purchase History

All subscription purchases are recorded in a **Purchase History** log that includes:
- Item type (subscription, boost, etc.)
- Amount paid
- Currency (PKR)
- Payment status (Completed, Pending, Refunded)
- Payment method
- Transaction ID
- Receipt reference

This gives both users and admins a clear audit trail for all financial transactions.

---

## 7. Subscription Renewal

Subscription renewal is currently a **manual process**:
- The system tracks the expiry date of each subscription
- When a subscription expires, the user reverts to free-tier limits
- The platform can send expiry reminder notifications
- The user must manually purchase a renewal

**Recommendation:** Auto-renewal via payment gateway integration is identified as a high-priority future feature (see Section 09).

---

## 8. Lifetime Plan

The Lifetime Plan is a one-time purchase that permanently activates premium features. It has no expiry date and does not require renewal. This plan type has strategic business value:
- Generates large upfront revenue
- Builds deeply loyal long-term users
- Reduces support burden from recurring subscription issues

---

## 9. Connection to AI Feature Limits

The `max_ai_chats` and `max_journal_entries` settings are enforced in real time. When a user approaches or reaches their limit:
- A warning is displayed in the AI chat or journal interface
- A prompt to upgrade their subscription is shown
- The user is linked directly to the Plans page

This limit-gate mechanism is the primary conversion driver from free to paid tiers.

---

## 10. Admin Control Over Plans

Subscription plans are **fully configurable by the admin team** without requiring any changes to the platform. Admins can:
- Create new plans
- Edit existing plan prices and features
- Deactivate plans that are no longer offered
- View all active user subscriptions
- Manually activate or modify a user's subscription

This flexibility allows the business team to run promotions, A/B test pricing, and respond to market conditions without technical intervention.

---

## Process Flow

```
User Hits Limit / Browses Plans Page
           │
           ▼
    Select Subscription Plan
           │
           ▼
    External Payment Made
           │
           ▼
  Screenshot Uploaded + Transaction ID
           │
           ▼
   Admin Reviews Payment Proof
           │
      ┌────┴────┐
   Approved    Rejected
      │            │
      ▼            ▼
  Plan Activated  User Notified
  Notification    with Rejection
  Sent to User    Reason
```

---

## Business Impact

| Metric | How Subscriptions Impact It |
|---|---|
| **Monthly Recurring Revenue (MRR)** | Monthly plan subscriptions form the predictable revenue base |
| **Average Revenue Per User (ARPU)** | Higher plan tiers increase ARPU |
| **Conversion Rate** | Free-to-paid conversion driven by feature limits and plan page UX |
| **Lifetime Value (LTV)** | Lifetime plans maximize LTV from power users |
| **Churn Rate** | Manual renewal creates churn risk; auto-renewal would reduce it |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Payment friction** | Manual payment process increases abandonment | Future payment gateway integration |
| **Verification delays** | Admin team bottleneck in approving payments | Set SLA of 24 hours for payment verification |
| **Churn at expiry** | Users who forget to renew are lost | Expiry reminder notifications 7 days and 1 day before expiry |
| **Plan complexity** | Too many plan options confuse users | Limit to 3–4 clearly differentiated tiers |
| **Fraud** | Fake payment screenshots uploaded | Admin manual review; require transaction IDs that can be cross-checked |

---

## Recommendations

1. **Integrate a payment gateway** (JazzCash, EasyPaisa, Stripe) to automate payment collection and eliminate manual screenshot verification.
2. **Implement automatic subscription renewal reminders** sent via notification and email 7 days and 1 day before expiry.
3. **Add a referral rewards program** where successful referrals earn free subscription days or credits toward a plan upgrade.
4. **Create a student discount program** targeting university students — a high-need, high-engagement demographic for mental health services.
5. **Build a plan comparison page** with a clear table showing what each tier includes, making upgrade decisions easier.
