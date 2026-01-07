# Case Study: The "Black Box" of Revenue (PreSales Collective)

**Subject:** PreSales Collective (Membership & Community)  
**Theme:** Financial vs. CRM Disconnect  
**The Hook:** "Sales thought we won the deal. Finance hadn't been paid. We fixed the handshake."

---

## 1. The Context (The "Before")
**The Client:** A subscription-based community and partnership platform.
**The Environment:** Stripe (Memberships/Partnerships) + HubSpot (CRM) + Manual Invoicing.

**The Friction:**
*   **The "Gap":** Sales reps marked deals as "Closed Won" in HubSpot, but had no idea if the credit card actually went through in Stripe.
*   **Churn Blindness:** No automated way to track when a membership was expiring. Renewals were handled manually or missed entirely.
*   **Partnership Chaos:** High-ticket partnership invoices were sent manually, with no visibility in the CRM on payment status.

---

## 2. The "Plumbing" (The Fix)
**Strategy:** Make Stripe the "Trigger" and HubSpot the "Source of Truth."
**The Stack:** HubSpot, Stripe, Custom Webhook Integration.

**The Execution:**
1.  **The "Membership" Pipeline:** Created a dedicated pipeline in HubSpot strictly for membership automated flows.
2.  **Stripe-to-HubSpot Sync:**
    *   *Logic:* When `charge.succeeded` fires in Stripe -> Search HubSpot for email -> Create/Update Deal -> Move to "Paid" Stage.
3.  **Metadata Sync:** Pulled the Stripe Customer ID, Subscription ID, and Renewal Date into custom HubSpot fields.
4.  **Automated Renewal Defense:** Built workflows triggered by the Stripe Renewal Date field.
    *   *30 Days Out:* "Value Add" email sent automatically.
    *   *7 Days Out:* Renewal reminder.
    *   *Payment Failed:* Task created for CSM to reach out immediately.

---

## 3. The "Flow" (Results & ROI)
*   **Churn Reduction:** Dropped churn by **20%** simply by being proactive with automated renewal comms.
*   **Source of Truth:** Sales and Finance finally looked at the same numbers.
*   **Onboarding Velocity:** New members received onboarding emails **seconds** after payment, not hours later when a human checked Stripe.
