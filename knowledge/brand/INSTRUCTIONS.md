# Protocol: Updating the Brand Knowledge Base

**Purpose:** This document outlines the strict protocol for ingesting new information into the Brand & Strategy section.

---

## 1. The Golden Rule: Refactor, Do Not Append
**Never** simply paste new text at the bottom of a file.
*   **Bad:** Adding a new pricing table at the bottom of `01_CORE_Services_Pricing.md` while the old one remains at the top.
*   **Good:** Locating the existing pricing section, replacing it with the new data, and ensuring the surrounding context (ROI calculations, deliverables) still makes sense.

---

## 2. Ingestion Routing Logic (Where does it go?)

When you receive a new document or insight, map it to the correct file:

| If the new info is about... | Update this file... |
| :--- | :--- |
| **Identity, Tone, Persona** | `00_CORE_Identity_Positioning.md` |
| **Target Audience (ICP), Competitors** | `00_CORE_Identity_Positioning.md` |
| **Service Offerings, Deliverables** | `01_CORE_Services_Pricing.md` |
| **Pricing, ROI, Proof Points** | `01_CORE_Services_Pricing.md` |
| **Cold Outreach, Lead Gen, Triggers** | `playbooks/Prospecting.md` |
| **Sales Scripts, Objections, Closing** | `playbooks/Sales_Calls.md` |
| **Marketing Content, LinkedIn, Voice** | `playbooks/Content_Marketing.md` |

---

## 3. The Update Workflow

1.  **Analyze:** Is this a Refinement, Expansion, or Pivot?
    *   *Pivots (changing core truth) require User Confirmation.*
2.  **Check Conflicts:** Does this contradict `00_CORE_Identity_Positioning.md`?
3.  **Execute:** Rewrite the specific section in the target file.
4.  **Ripple Check:** If you change a core truth (e.g., pricing), update the corresponding scripts in `playbooks/`.
5.  **Clean:** Remove deprecated information.

---

## 4. Maintenance
*   **Deduplication:** Ensure stories in `Sales_Calls.md` and `Content_Marketing.md` are consistent.