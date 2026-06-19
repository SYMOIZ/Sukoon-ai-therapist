# Finance Management — Sukoon AI

**Section:** 04 — Admin Panel  
**Document:** FINANCE_MANAGEMENT.md  
**Audience:** Finance Team, Admin Team, Executive Team, Investors

---

## Executive Summary

Finance management on Sukoon AI is handled entirely within the Admin Panel. The finance module covers four core areas: session payment verification (the manual approval of client payment screenshots), therapist payout processing, subscription revenue tracking, and marketing expense management. This document describes every financial process, the roles responsible, and the controls in place.

---

## Purpose

To document the complete financial operations of the Sukoon AI platform — how money flows in (client payments), how it is tracked (commission and wallet), and how it flows out (therapist payouts and business expenses).

---

## Stakeholders

- Finance team (payout processing, expense management)
- Admin team (payment verification)
- Therapists (earning and requesting payouts)
- Clients (paying for sessions and subscriptions)
- Executive team (revenue visibility)
- Investors (financial performance oversight)

---

## 1. Revenue Streams

The platform generates revenue from two primary sources:

| Revenue Source | Description |
|---|---|
| **Session Commission** | 15% of every verified session payment |
| **Subscription Fees** | Recurring fees from client subscription plans |

### Secondary Revenue Consideration
- **Therapist Boost / Pro fees** (therapists paying for featured directory placement and pro features) — these are tracked as platform income if implemented as paid features.

---

## 2. Session Payment Verification

### The Manual Payment Model
Sukoon AI currently uses a **manual payment model** where:
1. Client makes a bank transfer or mobile payment
2. Client uploads a **screenshot** of the payment and enters a **transaction ID** in the booking form
3. Admin reviews the payment evidence and either **approves** or **rejects** the payment

### Admin Verification Steps
When reviewing a session payment, the admin:
1. Opens the payment record in the Finance dashboard
2. Reviews the uploaded payment screenshot
3. Checks:
   - Screenshot clarity (clearly shows transfer)
   - Amount matches the session fee
   - Transaction ID is present and plausible
   - Payment date is recent
   - Recipient account matches platform payment details
4. Selects **Approve** or **Reject**

### On Approval
- Session booking status advances to "Payment Approved"
- Therapist is notified that the booking is confirmed
- The session earnings entry is created in the wallet system

### On Rejection
- Reason must be provided by admin
- Client is notified of rejection with the reason
- Client can resubmit with corrected payment proof

---

## 3. Commission Model

Every verified session payment generates a commission split:

| Destination | Percentage | Example (PKR 1,000 fee) |
|---|---|---|
| **Therapist Earnings** | 85% | PKR 850 |
| **Platform Commission** | 15% | PKR 150 |

The commission split is automatically calculated when the admin approves a payment. No manual calculation is required — the system records both figures in the transaction log.

### Platform Commission Tracking
Platform commission accumulates in a separate tracked total visible in the Finance Dashboard. This represents the platform's gross revenue from session bookings.

---

## 4. Therapist Wallet and Payout System

### The Wallet
Each therapist has a **digital wallet** within the platform that accumulates earnings. After a payment is approved:
- The therapist's wallet balance increases by their 85% share
- A wallet transaction record is created with:
  - Date of transaction
  - Amount earned
  - Session / booking reference
  - Transaction type (Session Earning, Payout, Adjustment)

### Payout Requests
When therapists are ready to withdraw their earnings:
1. Therapist submits a **payout request** from their dashboard
2. Payout request appears in the **Finance section** of the Admin Dashboard
3. Admin reviews the request:
   - Confirms requested amount matches available balance
   - Verifies payment details (bank account or mobile wallet)
4. Admin processes the payout:
   - Makes the bank transfer or mobile payment to the therapist
   - Marks the payout request as "Processed" in the system
5. Therapist's wallet balance is reduced by the payout amount
6. Therapist receives a payout notification

### Payout Request Statuses
| Status | Meaning |
|---|---|
| **Pending** | Submitted by therapist; not yet reviewed |
| **Under Review** | Admin is reviewing the request |
| **Processed** | Payment made; wallet balance updated |
| **Rejected** | Payout could not be processed (incorrect details, etc.) |

### Payout Cycle
The recommended payout cycle is **bi-weekly or monthly**. All pending payout requests are processed in one batch at the defined cycle date. Therapists should be informed of the payout schedule to manage expectations.

---

## 5. Subscription Revenue

### How Subscription Payments Work
Clients pay for subscription plans (Basic, Standard, Premium, Enterprise). Subscription payments are:
- Currently processed manually (screenshot + transaction ID, same model as session payments)
- Or, in future, via automated payment gateway

### Admin Subscription Management
From the **Subscriptions** section, admins can:
- View all active subscriptions
- See subscription plan details (plan type, start date, expiry date, amount paid)
- Manually activate a subscription after verifying payment
- Manually extend or adjust subscription dates (e.g., for courtesy extensions)
- Deactivate subscriptions upon expiry or non-renewal

### Subscription Revenue Tracking
Subscription income is tracked separately from session commission in the Finance Dashboard. Monthly subscription revenue is a key performance indicator for platform health.

---

## 6. Marketing and Expense Tracking

### Marketing Expenses
The Finance Module includes a section for tracking **marketing and operational expenses**. The admin/finance team can log:
- Marketing campaign costs
- Platform operational expenses
- Other business expenses

Each expense record includes:
- Date
- Category (Marketing, Operations, Technical, Other)
- Amount
- Description / purpose

### Purpose
Expense tracking enables the finance team to:
- Calculate net profit (gross revenue minus expenses)
- Prepare financial reports for management
- Track return on marketing investment

---

## 7. Financial Reporting

From the Finance Dashboard, the admin team can generate:

| Report Type | What It Shows |
|---|---|
| **Monthly Revenue Summary** | Total session payments, subscription payments, commissions |
| **Payout Register** | All payouts made, by therapist, for a period |
| **Expense Register** | All recorded expenses for a period |
| **Therapist Earnings Report** | Earnings breakdown per therapist |
| **Commission P&L** | Platform gross revenue minus payouts and expenses |

---

## Process Flow (Finance Operations Cycle)

```
INFLOW (Daily):
Client Makes Payment → Screenshot Uploaded
        │
        ▼
Admin Verifies Payment
        │
  Approved → Session Confirmed → Therapist Wallet Credited
  Rejected → Client Notified

OUTFLOW (Bi-weekly/Monthly):
Therapist Submits Payout Request
        │
        ▼
Admin Reviews → Processes Bank Transfer
        │
        ▼
Payout Marked as Processed
Therapist Wallet Reduced
Therapist Notified

EXPENSES (As Incurred):
Finance Team Logs Expense
        │
        ▼
Expense Appears in Monthly Report

REPORTING (Monthly):
Revenue Summary Generated
P&L Statement Created
Shared with Management
```

---

## Business Impact

| Financial Control | Business Impact |
|---|---|
| **Fast payment verification** | Session starts; revenue earned; client satisfied |
| **Timely payout processing** | Therapist retention; platform reputation |
| **Accurate commission tracking** | Clean financial records; investor confidence |
| **Expense tracking** | Visible profitability; investment decision support |
| **Subscription verification** | Subscription revenue captured; plan access granted |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Payment fraud** | Fake screenshots to receive sessions without paying | Manual review; transaction ID cross-reference; escalation to authorities if detected |
| **Payout errors** | Wrong bank details or incorrect amount processed | Double-check payout details before processing; require therapists to confirm details |
| **Revenue leakage** | Commissions not recorded properly | Automated commission calculation; regular reconciliation |
| **Cash flow bottleneck** | Manual payment process slows revenue cycle | Payment gateway integration (recommended) |
| **Expense tracking gaps** | Expenses unrecorded distort profitability | Monthly expense reconciliation process |

---

## Recommendations

1. **Integrate a payment gateway** (JazzCash, Stripe, or EasyPaisa) to automate payment collection and eliminate the screenshot verification bottleneck — the single highest-impact operational improvement available.
2. **Define and publish a payout schedule** (e.g., every 1st and 15th of the month) so therapists can plan their finances and reduce ad-hoc payout requests.
3. **Implement double-entry confirmation** for payouts — require a second admin to confirm payouts above a defined threshold, reducing the risk of errors.
4. **Build a reconciliation dashboard** that compares total client payments received versus total therapist payouts processed, flagging any discrepancies.
5. **Produce monthly financial reports** in PDF format and share with the executive team — making financial performance visible to leadership on a regular cadence builds accountability.
