# Reporting and Analytics — Sukoon AI

**Section:** 04 — Admin Panel  
**Document:** REPORTING_AND_ANALYTICS.md  
**Audience:** Executive Team, Investors, Operations Management, Admin Team

---

## Executive Summary

Reporting and Analytics in the Sukoon AI Admin Panel provides leadership and operations teams with visibility into platform performance across four domains: user growth, therapist activity, financial performance, and clinical health. This document describes the key metrics tracked, the reports available, how they are produced, and how they should be used to make operational decisions.

---

## Purpose

To define what data the platform captures, how it is organized into meaningful reports, and how those reports are used by the management team to measure health, growth, and risk across the platform.

---

## Stakeholders

- Executive team (platform health, strategic decisions)
- Investors (growth metrics, revenue performance)
- Finance team (revenue and payout data)
- Operations team (daily performance monitoring)
- Clinical team (safety and wellbeing metrics)

---

## 1. Platform Overview Metrics

The **Admin Dashboard Overview** shows live running totals for the most critical platform indicators:

| Metric | Description |
|---|---|
| **Total Registered Users** | All-time client registrations |
| **Active Users (30-day)** | Users who have logged in within the last 30 days |
| **Total Therapists** | Approved active therapists on the platform |
| **Total Sessions Completed** | All-time delivered and verified sessions |
| **Sessions This Month** | Sessions completed in the current calendar month |
| **Platform Revenue (Gross)** | Total session commissions and subscription fees |
| **Open Support Tickets** | Currently unresolved tickets |
| **Active Risk Alerts** | Unresolved high-risk user alerts |

---

## 2. User Growth Metrics

### Tracked Data Points
- New registrations per week / month
- Registration source (email/password vs. Google OAuth)
- User activation rate (registered → verified → first AI chat)
- Monthly Active Users (MAU)
- User retention rate (users who return after 30 days)
- Churn rate (users who stop using the platform)

### Report: Monthly User Report
| Section | Content |
|---|---|
| New Registrations | Count and growth rate vs. previous month |
| Activated Accounts | Users who completed onboarding |
| Monthly Active Users | Unique users with at least one session this month |
| Retention | % of last month's users still active this month |
| Churn | % of users who have not returned in 60+ days |

---

## 3. Therapist Activity Metrics

### Tracked Data Points
- Total approved therapists
- New approvals this month
- Active therapists (at least one session in the last 30 days)
- Average sessions per therapist per month
- Therapists with no calendar availability (inactive)
- Average therapist rating
- Payout requests submitted and processed

### Report: Therapist Performance Report
| Section | Content |
|---|---|
| Approved Therapists | Total active approved therapists |
| New Approvals | Therapists approved this month |
| Session Volume | Total sessions delivered per therapist |
| Ratings Summary | Average platform rating; lowest and highest rated |
| Inactive Therapists | Therapists with no calendar slots in 14+ days |
| Payout Volume | Total payout value processed |

---

## 4. Financial Performance Metrics

### Tracked Data Points
- Gross session revenue (total payments approved)
- Platform commission earned (15% of gross)
- Subscription revenue
- Total payouts processed
- Net platform revenue (commission + subscription − payouts − expenses)
- Revenue per active user (ARPU)
- Average session fee (platform-wide)

### Report: Monthly Financial Report
| Section | Content |
|---|---|
| Session Revenue | Total session payments approved |
| Commission Income | 15% platform share from sessions |
| Subscription Income | Subscription fees collected |
| Payouts Disbursed | Total paid out to therapists |
| Marketing Expenses | Logged operational expenses |
| Net Revenue | Income minus payouts and expenses |
| Revenue Growth | % change from previous month |

---

## 5. Session and Booking Metrics

### Tracked Data Points
- Total bookings submitted (all time and monthly)
- Bookings completed vs. cancelled vs. disputed
- Payment approval rate (approvals ÷ total payment submissions)
- Payment rejection reasons (breakdown)
- Average time to payment approval
- Session type breakdown (audio / video / chat)
- Session duration breakdown (45 / 60 / 90 min)
- Repeat booking rate (clients who book more than once)

---

## 6. Clinical Safety Metrics

### Tracked Data Points
- Active risk alerts (unresolved)
- Risk alerts created this month
- Average time to crisis therapist assignment
- Safety incidents logged by therapists
- Safety incidents by type (Suicide Risk, Harassment, Privacy, etc.)
- Safety incidents resolved vs. under review

### Report: Monthly Safety Report
| Section | Content |
|---|---|
| Risk Alerts | Created, assigned, resolved this month |
| Assignment Response Time | Average time from alert to therapist assignment |
| Safety Incidents | Count by type; resolution rate |
| High-Risk Users | Number of users currently flagged as High risk |

---

## 7. Support Operations Metrics

### Tracked Data Points
- Tickets opened per week/month
- Tickets resolved per week/month
- Average first response time (by priority level)
- Average resolution time
- Tickets by category (breakdown)
- Escalation rate
- Resolution satisfaction rate (if survey implemented)

---

## 8. How Reports Are Produced

### Current State
At the current platform development stage, reports are produced **manually** by admin staff querying the database or pulling data from the Admin Dashboard. The Admin Dashboard overview provides live aggregate counts; detailed breakdowns require direct database queries or export.

### Target State (Recommended)
- Build an **Export to CSV** function for all major data tables (users, sessions, payments, tickets)
- Build a **Monthly Report Generator** that automatically compiles the standard monthly reports in PDF format
- Integrate a lightweight analytics dashboard tool to visualize trends over time

---

## 9. Key Performance Indicators (KPIs)

The following KPIs should be reviewed monthly at the management level:

| KPI | Target (to define) | Current Source |
|---|---|---|
| **Monthly Active Users (MAU)** | Growth month-over-month | Admin Dashboard |
| **Session Completion Rate** | >85% of confirmed bookings | Finance / Sessions data |
| **Payment Approval Time** | <24 hours average | Finance Dashboard |
| **Payout Processing Time** | <7 days from request | Finance Dashboard |
| **Support First Response Time** | <24 hours average | Support Dashboard |
| **Risk Alert Response Time** | <2 hours average | Safety Dashboard |
| **Platform Net Revenue** | Growing month-over-month | Finance Report |
| **Therapist Retention Rate** | >80% active after 3 months | Therapist Report |

---

## Process Flow (Monthly Reporting Cycle)

```
First Week of Month:
  │
  ▼
Finance Team pulls previous month payment and payout data
  │
  ▼
Admin Team compiles user growth numbers from dashboard
  │
  ▼
Support Team reviews ticket resolution metrics
  │
  ▼
Clinical Team reviews safety incident summary
  │
  ▼
All data consolidated into Monthly Performance Report
  │
  ▼
Report shared with Executive Team
  │
  ▼
Management Review Meeting
  │
  ▼
Decisions taken on: staffing, feature priorities, therapist recruitment, marketing
```

---

## Business Impact

| Report / Metric | Business Impact |
|---|---|
| **MAU trend** | Validates product-market fit and marketing effectiveness |
| **Session completion rate** | Directly indicates revenue reliability |
| **Therapist activity** | Identifies supply bottlenecks before they impact bookings |
| **Safety report** | Demonstrates responsible governance to regulators and investors |
| **Net revenue** | Core business health indicator for investors |
| **Support resolution time** | Indicator of operational maturity and user experience quality |

---

## Risks

| Risk | Description | Mitigation |
|---|---|---|
| **Manual report production errors** | Human error in data compilation | Automate with CSV export and reporting templates |
| **Lagging metrics** | Monthly reports are too infrequent to catch problems early | Add weekly snapshot emails for key metrics |
| **KPI targets never set** | Metrics tracked but no goal to measure against | Define targets in the first management review |
| **Data not acted upon** | Reports produced but not reviewed | Make monthly review a standing mandatory meeting |
| **Incomplete data capture** | Some events not tracked in the database | Regular data integrity audits |

---

## Recommendations

1. **Define KPI targets** in the first management review meeting — numbers without targets cannot measure success or failure.
2. **Automate CSV export** for all major tables (users, sessions, payments, support tickets) so finance and operations teams can pull data without technical assistance.
3. **Build a weekly email digest** for the executive team showing the 5 most critical KPIs vs. previous week — catching trends before they become problems.
4. **Implement a data analytics tool** (Metabase, Redash, or similar) connected to the database, enabling the management team to self-serve queries without relying on developer time.
5. **Create an investor dashboard** — a read-only view with key growth and revenue metrics, usable during investor updates without sharing admin credentials.
