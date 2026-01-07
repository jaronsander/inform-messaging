# Contributing & Maintenance Protocol

**Purpose:** This repository is the "Single Source of Truth" for Inform Growth's messaging, strategy, and brand. This document outlines how to maintain its integrity.

## 1. The Global Workflow
We follow a strict **"Raw -> Processed"** pipeline to prevent knowledge decay.

### Step 1: Ingest (Dump)
*   **Where:** `raw_files/unprocessed/`
*   **What:** Meeting notes, brain dumps, forwarded emails, new case study stats, or unformatted strategy docs.
*   **Action:** Save the file here with a descriptive name (e.g., `2024-01-15_New_Pricing_Ideas.md`).

### Step 2: Process (Refactor)
*   **Who:** AI Agent or Human Operator.
*   **Action:** Read the raw file and "refactor" the knowledge into the structured `knowledge/` directories.
*   **Rule:** **Do not copy/paste.** Extract the truth and integrate it into the existing systems.

### Step 3: Cleanup (Delete)
*   **Action:** Once the knowledge has been successfully integrated, **delete** the file from `raw_files/unprocessed/`.
*   **Goal:** The `unprocessed` folder should be empty at the end of every session.

---

## 2. Directory Structure & Routing

| Directory | Purpose | Protocol |
| :--- | :--- | :--- |
| **`knowledge/brand/`** | Identity, Services, and Playbooks. | See `knowledge/brand/INSTRUCTIONS.md` |
| **`knowledge/icp/`** | Target Audience Definitions. | See `knowledge/icp/INSTRUCTIONS.md` |
| **`knowledge/proof_points/`** | Case Studies & ROI Stats. | See `knowledge/proof_points/README.md` |
| **`raw_files/unprocessed/`** | Temporary holding pen for new info. | Must be processed and deleted. |

---

## 3. The "Golden Rules" of Maintenance

1.  **Single Source of Truth:** Never duplicate a core truth (e.g., pricing) across multiple files unless necessary. If you do, update ALL instances simultaneously.
2.  **Refactor, Don't Append:** Never just add new text to the bottom of a file. Rewrite the relevant section to include the new information.
3.  **Delete Legacy:** If a strategy changes (e.g., "We no longer do cold calling"), delete the old instructions. Do not keep "deprecated" folders.
4.  **Check Ripple Effects:** If you update the **ICP** (Who we target), you MUST check **Prospecting Playbooks** (How we target them) to ensure alignment.
