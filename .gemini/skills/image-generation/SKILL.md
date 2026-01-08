---
name: image-generation
description: Generates visual assets for content posts using Nano-Banana, adhering to the brand's "Digital Plumbing" aesthetic.
allowed-tools: Read, Write, Generate Image, Generate Icon, Generate Diagram, Move
---

# Image Generation Skill

## Purpose
Create on-brand visual assets for finalized content in `content_pipeline/03_ready/`.

## Dependencies
*   **Style Guide:** `knowledge/brand/visual_style_guide.md`
*   **Asset Storage:** `content_pipeline/assets/`

## Interactive Workflow

### Trigger
User says: "Create visuals for [File Name]" or "Generate images for this post".

### Step 1: Analysis
1.  **Read the Target File:** (e.g., `content_pipeline/03_ready/my_post.md`)
2.  **Read the Style Guide:** `knowledge/brand/visual_style_guide.md`
3.  **Concept Extraction:**
    *   Identify the core metaphor (e.g., "Data leaks," "Integration," "Pricing").
    *   Map it to the "Digital Plumbing" aesthetic (Copper pipes, blueprints, flow).

### Step 2: Prompt Engineering
Construct a prompt for `nano-banana` that combines the concept with the style guide constraints.

*   **Template:** `[Concept] depicted as [Plumbing Metaphor], [Style Keywords from Guide], [Color Palette].`
*   **Example:** `Data silos depicted as disconnected rusty storage tanks, isometric vector art, minimalist style, deep navy background with copper accents.`

### Step 3: Generation
Use the appropriate tool based on the need:
*   **Hero Image:** `generate_image(prompt="...", style=["minimalist", "modern"], format="separate")`
*   **Diagram:** `generate_diagram(prompt="Flowchart of...", style="professional", type="flowchart")`
*   **Icon:** `generate_icon(prompt="...", style="modern", type="ui-element")`

### Step 4: Storage & Linking
1.  **Save:** The tool automatically saves the file. Ensure it is moved/saved to `content_pipeline/assets/`.
2.  **Rename:** Rename the file to match the post (e.g., `my_post_hero.png`).
3.  **Link:** detailed instructions on where the file is located for the user.

## Tips
*   **Consistency:** Always check previous assets in `assets/` (if visible) or strictly follow the Style Guide to ensure the feed looks cohesive.
*   **Simplicity:** For LinkedIn/Twitter, bolder, simpler images work better than complex scenes.
