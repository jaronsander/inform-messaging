---
name: image-generation
description: Generates reusable visual assets (Roy poses, elements, backgrounds) using Gemini's nano-banana image generation and maintains the asset catalog.
allowed-tools: Read, Write, Edit, Generate Image, Generate Icon, Generate Diagram, Bash
---

# Asset Generation Skill

## Purpose
Generate reusable visual components for Canva composition using **Gemini's nano-banana image generation capability**. This skill creates individual assets (not full posts) and automatically updates the asset catalog.

**CRITICAL PRINCIPLE:** This skill does NOT contain hard-coded rules. All visual guidelines, character definitions, colors, and constraints are defined in external markdown files. Your job is to READ those files and FOLLOW what they say.

## Required Files (READ EVERY TIME)

Before generating ANY asset, you MUST read these files to understand the current rules:

1. **`content_pipeline/assets/asset_catalog.md`**
   - Contains complete, ready-to-use generation prompts for all Roy poses
   - Defines what assets exist vs. what's pending
   - Specifies exact file naming conventions
   - **DO NOT GENERATE without reading this first**

2. **`knowledge/brand/roy_profile.md`**
   - Contains the "frozen prompt" CHARACTER DEFINITION block
   - Defines Roy's appearance, antenna states, and consistency requirements
   - **Use this CHARACTER DEFINITION exactly - do not rewrite or modify**

3. **`knowledge/brand/visual_style_guide.md`**
   - Defines color palette (hex codes and names)
   - Specifies visual aesthetic and style keywords
   - Provides generation guidelines for sticker style
   - Defines metaphors for data/process visualization

## Workflow

### Step 1: Read All Required Files
**CRITICAL:** Before doing ANYTHING, read these files in this order:
```
1. Read: content_pipeline/assets/asset_catalog.md
2. Read: knowledge/brand/roy_profile.md
3. Read: knowledge/brand/visual_style_guide.md
```

These files contain ALL the rules. Do not proceed with hard-coded assumptions.

### Step 2: Locate Asset in Catalog
Search `asset_catalog.md` for the requested asset:
- **If exists (with file path):** Inform user, provide path, STOP
- **If pending (has prompt but no file):** Proceed to Step 3
- **If completely new:** Construct prompt using guidelines from the files you just read

### Step 3: Extract or Construct Prompt

**For Roy Poses (PREFERRED):**
1. Find the asset entry in `asset_catalog.md`
2. Locate the "Generation Prompt" section
3. Copy the ENTIRE prompt exactly as written
4. Do NOT modify, rewrite, or "improve" the prompt
5. The prompt already includes the CHARACTER DEFINITION from `roy_profile.md`

**For New Assets (Elements/Backgrounds):**
1. Read `visual_style_guide.md` for:
   - Color palette (use exact hex codes specified)
   - Style keywords and aesthetic requirements
   - Generation guidelines for the asset type
2. Read `roy_profile.md` if the asset involves Roy
3. Construct prompt following the style guide's templates
4. Use colors and terminology exactly as defined in the files

### Step 4: Generate with Gemini
1. Use the exact detailed prompt from `roy_profile.md` combined with the specific action.
2. Generate using Gemini's nano-banana image generation.
3. For Roy poses: Follow the catalog's variation instructions (with/without toolbox).
4. Background transparency:
   - Roy and Elements: Transparent background
   - Backgrounds: Opaque (as specified in visual_style_guide.md)

### Step 5: Save Generated Images
... [Existing saving logic] ...

### Step 6: Update Asset Catalog (MANDATORY)
... [Existing catalog logic] ...

### Step 7: Proportional Audit & Quality Check (Joint Detection)
Before saving, verify the generated asset matches the requirements:

1. **Verify Joint Definition**: Check if 'Roy' has acquired joints. If the limbs show a distinct 'point' or 'bend' that looks like an elbow, **REJECT** and re-prompt with: "STRICT ADHERENCE REQUIRED: Smooth curves only, remove joint points from limbs."
2. **Verify Identity Match**: Check against `knowledge/brand/visual_benchmark.md` and the master reference sheet.
3. **Verify Slender Build**: Ensure the torso is a slim oval, not a stout pear shape, following the 1:3 ratio.

### Step 8: User Confirmation
Provide user with:
- ✅ Confirmation message
- 📁 File path(s) of generated asset(s)
- 📝 Brief description of what was created
- 🎨 Variations generated (if applicable)
- 📊 Updated catalog status

## Core Principles

**Single Source of Truth:**
- ✅ ALL rules live in external markdown files (knowledge base)
- ✅ This skill file only defines the PROCESS, not the content
- ✅ Always read the files to get current specifications
- ❌ Never rely on hard-coded assumptions or outdated information

**Mandatory Workflow:**
1. **Read first:** Load current specifications from the 4 required files
2. **Use exact prompts:** Copy from `asset_catalog.md` without modification
3. **Generate:** Use Gemini's nano-banana image generation
4. **Verify:** Check output against specifications in the files
5. **Update:** Modify `asset_catalog.md` to reflect new status
6. **Confirm:** Inform user with file paths and details

**What This Skill Does NOT Do:**
- ❌ Generate full social media posts (use content-generation skill for that)
- ❌ Add text overlays or captions to images
- ❌ Create one-off images (only reusable, cataloged assets)
- ❌ Modify or "improve" prompts from the catalog
- ❌ Guess at specifications without reading the files

**Character Consistency (Roy):**
All images of Roy MUST be the same character across all poses. The CHARACTER DEFINITION in `roy_profile.md` is frozen and must be used exactly as written. If you notice inconsistencies between generated images:
1. Compare against `roy_profile.md` specifications
2. Regenerate with stricter adherence to the frozen prompt
3. If issues persist after 2-3 attempts, inform user

**Asset Variations:**
- Roy poses: Follow variation instructions in `asset_catalog.md` (typically with/without toolbox)
- File naming: Follow conventions specified in `asset_catalog.md`
- Transparency: Follow specifications in `visual_style_guide.md`

## Example Usage

**User Request:** "Generate Roy in a confident pose"

**Correct Workflow:**

1. **Read all required files (FIRST):**
   ```
   Read: content_pipeline/assets/asset_catalog.md
   Read: knowledge/brand/roy_profile.md
   Read: knowledge/brand/visual_style_guide.md
   ```

2. **Locate asset in catalog:**
   - Search `asset_catalog.md` for "confident"
   - Find entry: "Roy - Confident (Arms Crossed)"
   - Check status: "Pending generation"
   - Note file paths: `roy_confident_arms_crossed.png` and `roy_confident_arms_crossed_no_toolbox.png`

3. **Extract exact prompt:**
   - Locate "Generation Prompt" section in the catalog entry
   - Copy the ENTIRE prompt block (do not modify)
   - The prompt already includes CHARACTER DEFINITION from `roy_profile.md`

4. **Generate both variations:**
   - First: Use prompt with "His toolbox sits at his feet"
   - Second: Use prompt with "no toolbox visible"
   - Save using exact file names from catalog

5. **Quality verification:**
   - Re-read `roy_profile.md` → Compare generated image to CHARACTER DEFINITION
   - Re-read `visual_style_guide.md` → Verify colors and style match

6. **Update catalog status:**
   ```
   From: - **Status:** Pending generation
   To:   - **Status:** Generated 2026-02-02
   ```

7. **Confirm with user:**
   - Provide file paths
   - Note both variations were created
   - Confirm catalog was updated

## Tips for Efficient Asset Generation

- **Always read files first:** Don't assume you know the current specifications
- **Batch generation:** Generate multiple Roy poses in one session (read files once, generate many)
- **Use catalog prompts:** The 7 core Roy poses have complete prompts - don't recreate
- **Suggest related assets:** If user requests one pose, offer complementary ones
- **Verify early:** Check first generated asset against files before batch-generating rest
- **Update as you go:** Update catalog immediately after each generation (don't batch updates)

## Troubleshooting

**If Generated Asset Doesn't Match Specifications:**

1. **Compare against source files:**
   - Re-read `roy_profile.md` for character requirements
   - Re-read `visual_style_guide.md` for style/color requirements

2. **Identify the discrepancy:**
   - Which specification from which file is being violated?
   - Is the prompt from `asset_catalog.md` being followed exactly?
   - Did you modify the CHARACTER DEFINITION block? (Don't do this)

3. **Attempt regeneration:**
   - Use the exact prompt again (no modifications)
   - If issue persists after 2-3 attempts, proceed to step 4

4. **Escalate to user:**
   - Report which specification is not being met
   - Reference the specific file and section containing the requirement
   - Suggest options:
     - Manual editing in image editor
     - Alternative generation tool
     - Updating the source file specification (requires user approval)

**Common Root Causes:**
- Modified the prompt from `asset_catalog.md` (don't do this)
- Didn't read all 3 required files before generating
- Used outdated information instead of reading current files
- Assumed specifications instead of reading the files

**Maintaining Consistency:**
All Roy images must be the same character. If you notice variation between generated poses:
1. Compare each image against `roy_profile.md` CHARACTER DEFINITION
2. Identify which pose deviates and in what way
3. Regenerate the inconsistent pose(s)
4. If issues persist, inform user and suggest updating `roy_profile.md` with stricter constraints
