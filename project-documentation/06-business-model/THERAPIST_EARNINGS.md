# Therapist Earnings — Sukoon AI

**Section:** 06 — Business Model  
**Document:** THERAPIST_EARNINGS.md  
**Audience:** Therapists, Finance Team, Admin Team, Investors

---

## Executive Summary

Therapists earn money on Sukoon AI by setting their own session fees and receiving 85% of every verified session payment. Earnings accumulate in a digital wallet within the platform and can be withdrawn through payout requests. The transparent, timely, and fair compensation model is essential for attracting and retaining high-quality therapists — the supply-side foundation of the entire platform.

---

## Purpose

To fully document how therapist earnings are calculated, accumulated, tracked, and paid out — ensuring complete transparency for therapists, finance teams, and investors.

---

## Stakeholders

- Therapists (understanding their income and payouts)
- Finance team (processing payouts and reconciliation)
- Admin team (verifying sessions and managing payout requests)
- Investors (understanding the economics of the supply side)

---

## 1. How Therapists Earn

Therapists earn a percentage of each therapy session fee paid by their clients.

### The Commission Split
| Party | Percentage | Example (PKR 2,000 fee) |
|---|---|---|
| **Therapist** | **85%** | **PKR 1,700** |
| Platform Commission | 15% | PKR 300 |

The 85% earnings rate is positioned as therapist-friendly — enabling therapists to build meaningful income while the platform operates sustainably.

---

## 2. Session Pricing (Therapist-Controlled)

Each therapist independently sets their own session pricing. The pricing is structured around three standard session durations:

| Session Duration | Typical Use |
|---|---|
| **45 minutes** | Check-in, brief follow-up |
| **60 minutes** | Standard full session |
| **90 minutes** | Deep/extended session |

Therapists set their own price per duration. There is no platform-imposed minimum or maximum fee (though guidance may be provided by the admin team). Prices are publicly displayed on the therapist's profile in the directory.

---

## 3. Paid Chat Pricing (Additional Income)

Beyond session bookings, therapists can earn from **Paid Chat Access**:

Clients can purchase time-limited direct messaging access with a specific therapist:
- **1-Day Chat Access** — Client pays a fee for 24-hour direct messaging access
- **7-Day Chat Access** — Client pays for 7-day access
- **1-Month Chat Access** — Client pays for 30-day access

Therapists set their own price for each tier. Paid chat earnings follow the same 85/15 commission split as session earnings.

---

## 4. The Therapist Wallet System

### What It Is
Each therapist has a **digital wallet** within the platform that accumulates their earnings.

### How It Works
When a session payment is verified by the admin:
1. A **Wallet Transaction** record is created
2. The therapist's wallet balance increases by 85% of the session fee
3. The transaction is visible immediately in the therapist's Earnings section

### Transaction Record Fields
| Field | Description |
|---|---|
| **Date** | Date of the earning |
| **Session Reference** | Which booking generated this earning |
| **Client** | Which client's session |
| **Full Session Fee** | Total amount paid by client |
| **Platform Commission (15%)** | The amount retained by the platform |
| **Therapist Earning (85%)** | The amount credited to therapist wallet |
| **Transaction Type** | Session Earning, Payout, Adjustment |

---

## 5. Payout Process

### When Therapists Can Request Payout
Therapists can submit a payout request at any time their wallet has a positive balance. The admin team processes payouts on a defined schedule (recommended: bi-weekly or monthly).

### How to Request a Payout
1. Therapist navigates to **Earnings** section of their dashboard
2. Therapist clicks **"Request Payout"**
3. Therapist enters the desired payout amount (up to their current balance)
4. Therapist confirms their bank account or mobile wallet details
5. Request is submitted to the admin team

### Payout Request Review
The admin team reviews the payout request:
- Confirms the requested amount is available in the wallet
- Verifies the bank account or mobile wallet details
- Makes the transfer (manual bank transfer or mobile payment)
- Marks the payout as "Processed" in the system
- The therapist's wallet balance is reduced by the payout amount
- Therapist receives a payout notification

### Payout Timeline
Target payout processing time: **5–7 business days** from request submission to funds transfer.

### Payout Statuses
| Status | Meaning |
|---|---|
| **Pending** | Submitted; awaiting admin processing |
| **Under Review** | Admin is reviewing |
| **Processed** | Funds transferred; wallet balance reduced |
| **Rejected** | Could not be processed (incorrect details, etc.) |

---

## 6. Payout History

Therapists can view a complete history of all payout requests, including:
- Date of request
- Amount requested
- Amount received
- Status
- Payment reference (if provided)

This gives therapists a complete and transparent record of all financial activity through the platform.

---

## 7. Annual Earnings Example

To illustrate the potential therapist income:

| Scenario | Sessions/Month | Avg Session Fee | Monthly Earnings (85%) | Annual Earnings |
|---|---|---|---|---|
| Part-time (10 sessions) | 10 | PKR 1,500 | PKR 12,750 | PKR 153,000 |
| Active (20 sessions) | 20 | PKR 2,000 | PKR 34,000 | PKR 408,000 |
| High-volume (40 sessions) | 40 | PKR 2,500 | PKR 85,000 | PKR 1,020,000 |

These numbers are illustrative and depend entirely on the therapist's session fees, booking rate, and availability.

---

## 8. Boost and Pro Impact on Earnings

Therapists who invest in a **Professional Boost** subscription gain higher visibility in the directory, which can lead to:
- More profile views
- More booking inquiries
- Higher session volume
- Higher total earnings

The indirect earnings impact of Boost is a key selling proposition for the Boost feature.

---

## 9. Taxes and Financial Responsibility

The platform provides earnings records through the Wallet system. However:
- Therapists are individually responsible for declaring their platform income to relevant tax authorities
- The platform does not withhold taxes on behalf of therapists
- Therapists should consult a financial advisor regarding their tax obligations
- The platform may be required to provide income reports to regulatory bodies as required by law

---

## Process Flow (Full Earnings Cycle)

```
Client Books Session + Pays
        │
        ▼
Admin Verifies Payment
        │
        ▼
Therapist Wallet Credited (85%)
Transaction Record Created
        │
        ▼
Therapist Views Earnings in Dashboard
        │
        ▼
Therapist Submits Payout Request
  (amount + payment details)
        │
        ▼
Admin Reviews Request
        │
        ▼
Admin Transfers Funds
Marks Payout "Processed"
        │
        ▼
Therapist Receives Notification
Wallet Balance Reduced
        │
        ▼
Transaction Appears in Payout History
```

---

## Business Impact

| Earnings Feature | Business Impact |
|---|---|
| **85% earning rate** | Competitive therapist compensation drives supply-side recruitment |
| **Transparent wallet** | Builds therapist trust; reduces payout disputes |
| **Fast payout processing** | Therapist satisfaction and retention |
| **Session fee autonomy** | Attracts therapists at all price points |
| **Paid chat income** | Additional revenue stream for active therapists |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Payout delays** | Slow processing damages therapist trust | Enforce 7-day SLA; auto-notify therapists of payout status |
| **Incorrect payout amount** | Admin error in processing | Double-verify amount against wallet balance before transfer |
| **Wallet balance discrepancy** | Earning credited but wrong amount | Commission calculation is automated; manual overrides require senior approval |
| **Therapist payout to wrong account** | Funds sent to incorrect bank details | Require therapists to confirm bank details twice; SMS confirmation to therapist |
| **Tax compliance issues** | Platform not meeting regulatory requirements | Consult legal/financial advisor; implement income reporting for tax compliance |

---

## Recommendations

1. **Set and publish the payout processing schedule** (e.g., every 1st and 15th of the month) — therapists need to plan their finances, and a predictable schedule reduces anxiety and ad-hoc requests.
2. **Add a payout receipt** — a formatted PDF or email confirmation for every processed payout, giving therapists a financial record.
3. **Build a payout simulation tool** — allow therapists to see "If I complete 10 sessions this month at PKR 2,000 each, here is your projected earning" — motivating more booking availability.
4. **Introduce a therapist loyalty bonus** — consider a quarterly bonus for therapists who maintain high session volume, high ratings, and low cancellation rates — incentivizing quality supply.
5. **Consult a local tax advisor** on the platform's obligations regarding therapist income reporting, particularly as session volumes grow into ranges that may trigger formal reporting requirements.
