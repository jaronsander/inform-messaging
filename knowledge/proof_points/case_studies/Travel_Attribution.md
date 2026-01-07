# Case Study: The "Marketing Lie" (Women Travel Abroad)

**Subject:** Women Travel Abroad (Travel & Tourism)  
**Theme:** Attribution & ROI  
**The Hook:** "We stopped asking 'How many clicks?' and started asking 'How much profit?'"

---

## 1. The Context (The "Before")
**The Client:** A travel company selling vacation packages via third-party partners and ads.
**The Environment:** Heavy ad spend, partner commissions, zero conversion tracking.

**The Friction:**
*   **The "Black Hole":** Marketing reported high traffic numbers, but nobody knew which specific partner delivered the paying customers.
*   **Wasted Budget:** The client was paying commissions to partners who sent traffic that bounced instantly.
*   **Tech Deficit:** No Google Analytics conversion events or standardized UTMs.

---

## 2. The "Plumbing" (The Fix)
**Strategy:** Implement a "Full-Funnel" tracking layer.
**The Stack:** Google Tag Manager (GTM), Google Analytics 4 (GA4), BigQuery, Looker Studio.

**The Execution:**
1.  **Standardization:** Created a rigid UTM naming convention and built a tool to force partners to use it.
2.  **Conversion Tracking:** Configured GTM to fire events not just on "Page View," but on "Booking Confirmed" and "Deposit Paid."
3.  **The Visualization:** Piped the data into BigQuery and visualized it in Looker Studio.
4.  **The Dashboard:** A simple view showing Spend vs. Revenue per partner.

---

## 3. The "Flow" (Results & ROI)
*   **Partnership ROI:** Improved by **27%**. The client fired the low-quality partners and reallocated budget to the high-converters.
*   **Clarity:** The Founder could finally answer, "If I spend $1 on this partner, do I get $2 back?"
*   **Scalability:** The tracking infrastructure allowed them to onboard new partners with confidence, knowing they could measure performance from Day 1.
