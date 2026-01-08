# Content Pipeline & Feedback Loop

This document outlines the workflow for converting ideas into content and, crucially, how to use the feedback loop to improve the system over time.

## 📂 The Pipeline Structure

*   **`01_ideas/`**: Raw thoughts, links, voice notes (transcribed).
*   **`02_drafts/`**: AI-generated options (Tri-Type: Story, Thought Leader, Sales).
*   **`03_ready/`**: Polished, formatted, ready for posting.
*   **`04_archive/`**: Posted content.

---

## 🔄 The Feedback Loop (Optimization)

To reduce editing time, we use a specific protocol after you edit a post in `03_ready/`.

### 1. The "Post-Mortem" Trigger
After you move a file to `03_ready/` and make final edits, run the **Feedback Analysis** (via the Content Generation Skill).

**The Logic:**
1.  Compare `02_drafts/[file]` vs. `03_ready/[file]`.
2.  Identify *what* changed:
    *   **Tone?** (e.g., "Too salesy" -> Update `Content_Marketing.md`)
    *   **Facts?** (e.g., "Price is wrong" -> Update `01_CORE_Services_Pricing.md`)
    *   **Formatting?** (e.g., "More whitespace" -> Update `style_guide.md`)
3.  **Execute the Update:** The system will immediately update the `knowledge/` base.

### 2. The "Negative Constraints" File
Located at `knowledge/brand/style_guide_updates.md`.
*   This file acts as a "Buffer" for quick style corrections.
*   *Example:* "Stop starting sentences with 'In the world of...'"
*   The Content Generator reads this file *every time* it generates a draft.

---

## 📝 Workflow for Users

1.  **Drop an Idea:** Create a file in `01_ideas/`.
2.  **Generate:** Ask the agent to "Generate content for [idea]".
3.  **Review:** Read the file in `02_drafts/`.
4.  **Edit & Finalize:** Move to `03_ready/` and tweak it.
5.  **Add Visuals:** Ask the agent (Gemini) to "Create visuals for [file]". It will use the `visual_style_guide.md` and save images to `assets/`.
6.  **Close the Loop:** Tell the agent: "I finished editing [file]. Run the feedback loop."

---

## ⚠️ Golden Rule for Feedback
**If you change a Fact (Pricing, Service Name, ICP trait), you MUST trigger the feedback loop.**
Otherwise, the system will keep generating outdated content.
