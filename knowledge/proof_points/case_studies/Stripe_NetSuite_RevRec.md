# Case Study: Quote-to-Cash Automation (Stripe ↔ NetSuite)

**Subject:** B2B SaaS Company (Anonymous)
**Theme:** Revenue Recognition & Financial Operations
**The Hook:** "How we eliminated revenue reporting discrepancies and automated contract-based rev rec with bidirectional Stripe-NetSuite sync."

---

## 1. The Context (The "Before")
**The Client:** Growth-stage B2B SaaS company with subscription billing and professional services revenue streams.

**The Environment:** Stripe handled billing, NetSuite managed financials. Manual reconciliation between systems every month.

**The Friction:**
*   **Revenue Reporting Discrepancies:** Monthly close revealed inconsistencies between Stripe charges and NetSuite revenue recognition.
*   **Manual Reconciliation:** Finance team spent days each month matching Stripe invoices to NetSuite records, correcting errors, and adjusting revenue schedules.
*   **Delayed Recognition:** Subscription revenue recognition lagged behind actual billing due to manual entry delays.
*   **Forecasting Blindness:** Could not accurately forecast revenue due to inconsistent data between billing and financial systems.
*   **Audit Risk:** Inconsistent records created compliance and audit trail concerns.

---

## 2. The "Plumbing" (The Fix)
**Strategy:** Build bidirectional sync between Stripe and NetSuite with event-driven revenue recognition logic.

**The Stack:** Celigo (iPaaS integration platform), dbt (data modeling), Stripe API, NetSuite API.

**The Execution:**
1.  **Directional Sync Architecture:** Built Stripe ↔ Celigo ↔ NetSuite flow:
    *   Stripe charges/subscriptions automatically create NetSuite invoices and revenue schedules
    *   NetSuite contract updates flow back to Stripe for billing adjustments
2.  **Event-Driven Rev Rec:** Created logic to automatically recognize revenue based on:
    *   Subscription start/end dates
    *   Contract terms (monthly vs. annual)
    *   Professional services delivery milestones
3.  **Data Modeling in dbt:** Modeled subscription and invoice objects to ensure consistent schemas between systems.
4.  **Revenue Forecasting Dashboard:** Built dashboards pulling from unified data model for accurate revenue forecasting and recognition visibility.

---

## 3. The "Flow" (Results & ROI)
*   **Eliminated Discrepancies:** Revenue reporting inconsistencies between Stripe and NetSuite reduced to near-zero.
*   **Finance Time Savings:** Eliminated multi-day manual reconciliation process each month. Finance team redirected time to strategic analysis.
*   **Real-Time Recognition:** Subscription revenue now recognized automatically within hours of billing instead of weeks.
*   **Forecasting Accuracy:** Revenue forecasting accuracy improved significantly with unified, real-time data.
*   **Audit Readiness:** Created clean audit trail with automated records linking billing events to revenue recognition.
*   **Scalability:** System scaled seamlessly as subscription volume grew without adding Finance headcount.
