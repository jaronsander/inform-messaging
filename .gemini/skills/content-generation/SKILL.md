---
name: content-generation
description: Generates LinkedIn/social content from drafts and suggests appropriate visual assets from the catalog for Canva composition.
allowed-tools: Read, Write, Edit, Bash
---

# Content Generation Skill

## Purpose
Transform raw content ideas into polished LinkedIn/social posts and suggest appropriate visual assets for Canva composition. This skill does NOT generate images - it suggests existing assets or flags when new assets are needed.

## Dependencies
- **Asset Catalog:** `content_pipeline/assets/asset_catalog.md` (check for matching assets)
- **Brand Voice:** `knowledge/brand/playbooks/Content_Marketing.md`
- **Content Drafts:** `content_pipeline/02_drafts/` or `content_pipeline/03_ready/`

## Workflow

### Step 1: Read the Content
1. **Read the draft file** provided by user
2. **Identify the content type:**
   - Problem post (pain point, diagnostic)
   - Solution post (how-to, fix)
   - Success post (results, ROI, wins)
   - Educational post (teaching, explaining)
   - Authority post (positioning, bold claim)

### Step 2: Analyze Theme & Emotion
Determine the dominant emotion/theme:
- **Confident/Authority** → Bold claims, "we've got this"
- **Concerned/Problem** → Pain points, diagnostics, "here's what's wrong"
- **Excited/Insight** → Breakthroughs, aha moments, key insights
- **Explaining/Teaching** → Educational, how-to, process
- **Celebrating/Success** → Wins, results, ROI reveals
- **Problem-Solving/Technical** → Fixing, hands-on, technical deep-dive

### Step 3: Check Asset Catalog
1. **Read:** `content_pipeline/assets/asset_catalog.md`
2. **Search keywords:** Look for Roy poses and elements matching the theme
3. **Match assets:**
   - Find 1-2 Roy poses that fit the emotion
   - Find any relevant elements (pipes, tools, effects)
   - Note any backgrounds if needed

### Step 4: Generate Canva Suggestions
Output format:
```
## Visual Asset Suggestions

### Primary Asset
- **Roy Pose:** [Name of pose from catalog]
  - File: `content_pipeline/assets/roy/[filename].png`
  - Why: [Brief explanation of why this matches the content]

### Supporting Elements (Optional)
- **Element:** [Element name if available]
  - File: `content_pipeline/assets/elements/[filename].png`
  - Suggestion: [How to use it - e.g., "Place behind Roy as background context"]

### Canva Composition
- Place [Roy pose] in [position suggestion - e.g., bottom-right, center]
- [Any layering suggestions if using elements]
- Use carbon gray background or blueprint overlay
- Keep text overlay space in [position]

### If No Match Found
⚠️ New asset needed: [Describe what should be generated]
→ Use the image-generation skill to create: [specific request]
```

### Step 5: Polish Content Copy
If the content needs copywriting improvements:
1. Read `knowledge/brand/playbooks/Content_Marketing.md` for voice/tone
2. Apply brand voice principles:
   - Clinical, technical, authoritative
   - No marketing fluff
   - Use RevOps/engineering language
3. Ensure hook → insight → CTA structure
4. Keep LinkedIn-friendly length (150-300 words for posts)

### Step 6: Output Final Package
Provide user with:
1. **Polished content copy** (if edits were made)
2. **Visual asset suggestions** (from catalog)
3. **Canva assembly instructions** (simple, not overly prescriptive)
4. **New asset requests** (if existing assets don't match)

## Special Rules

**CRITICAL:**
- Never generate images yourself - always reference the asset catalog
- If no matching asset exists, explicitly flag it and suggest what to generate
- Do NOT create text overlay instructions for image generation
- Keep Canva suggestions flexible (e.g., "Place Roy in corner" not "Place Roy at x=234, y=567")
- Always read the asset catalog before making suggestions

**Content Voice:**
- Follow "The Funnel Plumber" brand voice
- Technical/clinical tone, not marketing fluff
- Avoid: synergy, holistic, ideate, disrupt
- Use: refactor, latency, throughput, telemetry, leakage, schema

**Asset Matching Priority:**
1. Exact emotion match (confident content → confident Roy)
2. Thematic match (technical content → problem-solving Roy)
3. Contrasting emotion (problem post might use concerned OR confident Roy depending on angle)

## Example Usage

**User Request:** "Generate content for my draft about data leaks"

**Workflow:**
1. Read the draft file
2. Identify: Problem post, concerned/urgent tone
3. Read asset catalog
4. Find match: "Roy - Concerned (Hand on Chin)" or "Roy - Problem Solving (Wrench in Hand)"
5. Check for elements: "pipes_leaking.png" if available
6. Output suggestions:
   ```
   ## Visual Asset Suggestions

   ### Primary Asset
   - **Roy Pose:** Roy - Concerned (Hand on Chin)
     - File: `content_pipeline/assets/roy/roy_concerned_thinking.png`
     - Why: Matches the diagnostic tone of identifying data leakage issues

   ### Supporting Elements
   - ⚠️ New asset needed: Leaking pipes element
     → Use the image-generation skill to create a "pipes with green liquid leaking" element

   ### Canva Composition
   - Place Roy in bottom-right corner
   - If leaking pipes element is created, position in upper-left as context
   - Use carbon gray background
   - Keep text overlay space in center-left
   ```

## Tips
- Suggest batching asset generation if multiple new assets are needed
- If content theme is unclear, ask user for clarification before searching catalog
- When multiple Roy poses could work, present options and let user choose
- Keep suggestions simple - user knows their Canva workflow better than you
- Focus on matching emotion first, then theme
