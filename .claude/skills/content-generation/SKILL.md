---
name: content-generation
description: Generates LinkedIn/Reddit content from raw ideas and processes user feedback to update the knowledge base.
allowed-tools: Read, Write, Bash, Glob, Replace
---

# Content Generation Skill

## Purpose
1.  **Generate:** Transform raw notes in `content_pipeline/01_ideas/` into structured drafts in `content_pipeline/02_drafts/` using the `knowledge/` base.
2.  **Learn:** Analyze edits made by the user in `content_pipeline/03_ready/` to update the `knowledge/` base (Feedback Loop).

## Interactive Workflow

### Mode 1: Generate Content

**Trigger:** User asks to "Generate content" or "Process ideas".

1.  **Scan:** List files in `content_pipeline/01_ideas/`.
2.  **Select:** Ask user which idea to process.
3.  **Context Loading:**
    *   Read the selected idea file.
    *   Read `knowledge/brand/playbooks/Content_Marketing.md` (Voice/Tone).
    *   Read `knowledge/icp/00_ICP_Definition.md` (Target Audience).
    *   Read `knowledge/brand/style_guide_updates.md` (Negative constraints - *if exists*).
    *   Read `knowledge/brand/00_CORE_Identity_Positioning.md` (Optional: if strategy is needed).
4.  **Drafting:**
    *   Create 3 variations based on the "Tri-Type" Strategy (Story, Thought Leader, Sales).
    *   Apply constraints from `style_guide_updates.md`.
5.  **Save:** Write the result to `content_pipeline/02_drafts/[Idea_Name]_DRAFT.md`.
6.  **Cleanup:** Ask to move the original idea to `content_pipeline/04_archive/` or keep it.

**Example Prompt to Agent:**
"Generate content for `agency_data_mess.md`. Use the 'Tri-Type' strategy. Ensure you check `style_guide_updates.md` for banned phrases."

---

### Mode 2: Feedback Loop (The Optimizer)

**Trigger:** User says "I edited the draft" or "Run feedback loop on [file]".

1.  **Locate:**
    *   Find the **Final** version in `content_pipeline/03_ready/`.
    *   Find the **Original** draft in `content_pipeline/02_drafts/` (or archive).
2.  **Diff:** Compare the two files. Identify changes in:
    *   **Tone/Voice:** (Did they make it punchier? Less formal?)
    *   **Facts:** (Did they correct pricing or terms?)
    *   **Structure:** (Did they change the hooks?)
3.  **Route Updates:**
    *   **If Tone/Structure changed:** Suggest appending a rule to `knowledge/brand/style_guide_updates.md` OR updating `Content_Marketing.md`.
    *   **If Facts changed:** Suggest updating `00_CORE_Identity_Positioning.md` or `01_CORE_Services_Pricing.md`.
4.  **Execute:** Update the relevant knowledge file upon user confirmation.

**Example Analysis:**
"I noticed you changed 'We facilitate data integration' to 'We fix broken pipes'.
-> **Action:** I will add 'Use plumbing metaphors over corporate speak' to `style_guide_updates.md`."

---

## Critical Files

*   `content_pipeline/INSTRUCTIONS_CONTENT_LOOP.md`: The user manual for this workflow.
*   `knowledge/brand/playbooks/Content_Marketing.md`: The source of truth for *how* to write.
*   `knowledge/brand/style_guide_updates.md`: The "Negative Constraints" buffer (create if missing).

## Tips for Success

*   **Always read the Negative Constraints:** This is how the system stops making the same mistake twice.
*   **Check for ROI:** If an idea mentions numbers, always cross-reference `knowledge/proof_points/00_ROI_Master_Sheet.md`.
*   **Refactor, Don't Append:** When updating the knowledge base from feedback, rewrite the section; don't just add a P.S. at the bottom.
