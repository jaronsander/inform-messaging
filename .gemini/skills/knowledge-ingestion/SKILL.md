---
name: knowledge-ingestion
description: Interactively ingest documents from raw_files/unprocessed into the knowledge base. Use when processing raw documents, adding content to the knowledge repository, or organizing unprocessed files.
allowed-tools: Read, Grep, Glob, Edit, Write, Bash
---

# Knowledge Ingestion Skill

## Purpose

Guide users through the interactive process of ingesting raw documents into the structured knowledge base following repository protocols defined in CONTRIBUTING.md.

## Quick Start

1. Scan `raw_files/unprocessed/` for files
2. Read CONTRIBUTING.md and relevant INSTRUCTIONS.md files
3. Collaborate with user to route and refactor content
4. Move to processed/ and commit changes

## Critical Rules (from CONTRIBUTING.md)

1. **Refactor, Don't Append** - Always integrate into existing sections, never paste at bottom
2. **Single Source of Truth** - Check for ripple effects when updating core truths
3. **Delete Legacy** - Remove deprecated content immediately
4. **Raw → Processed Pipeline** - File must be moved to `raw_files/processed/` after successful ingestion

---

## Interactive Workflow

### Step 1: Discovery

**Goal:** Find and select files to process

**Actions:**
1. List files in `raw_files/unprocessed/`:
   ```bash
   ls -lh raw_files/unprocessed/
   ```

2. If files exist, show user:
   - Filename
   - Size
   - Modified date

3. Ask user: "Which file would you like to process?" or "Process all files?"

4. If no files exist, inform user the unprocessed folder is empty

**Example:**
```
Found 2 files in raw_files/unprocessed/:
  1. case_studies.md (8KB, modified 2 hours ago)
  2. new_pricing.md (3KB, modified yesterday)

Which file would you like to process? (1/2/all/cancel)
```

---

### Step 2: Read & Understand

**Goal:** Understand the content and repository protocols

**Actions:**
1. Read the selected raw file completely
2. Read `CONTRIBUTING.md` to understand:
   - The "Raw → Processed" workflow
   - The routing table (which content goes where)
   - The Golden Rules (Refactor not Append, Single Source of Truth, etc.)

3. Read relevant protocol files based on content type:
   - `knowledge/brand/INSTRUCTIONS.md` - for brand/strategy content
   - `knowledge/icp/INSTRUCTIONS.md` - for ICP updates
   - `knowledge/proof_points/README.md` - for case studies

4. Summarize to user:
   - What content you found in the raw file
   - Key protocols that apply
   - Initial thoughts on routing

**Example:**
```
I've read case_studies.md. It contains:
- 3 client case studies with metrics
- Some brand positioning notes
- A pricing update mention

Key protocols from CONTRIBUTING.md:
- Must refactor content into existing files (never append)
- ICP changes ripple to Prospecting playbook
- Case studies need both detailed file + ROI Master Sheet update
```

---

### Step 3: Analyze & Route

**Goal:** Determine where content should be integrated

**Actions:**
1. Analyze content and identify distinct sections/topics

2. For each section, reference the routing table from CONTRIBUTING.md:
   | Content Type | Target File |
   |---|---|
   | Identity, tone, persona, competitors | `knowledge/brand/00_CORE_Identity_Positioning.md` |
   | Service offerings, deliverables, pricing, ROI | `knowledge/brand/01_CORE_Services_Pricing.md` |
   | Cold outreach, lead gen, triggers | `knowledge/brand/playbooks/Prospecting.md` |
   | Sales scripts, objections, closing | `knowledge/brand/playbooks/Sales_Calls.md` |
   | Marketing content, LinkedIn, voice | `knowledge/brand/playbooks/Content_Marketing.md` |
   | ICP updates, target audience | `knowledge/icp/00_ICP_Definition.md` |
   | Case studies | `knowledge/proof_points/case_studies/[Name].md` + `00_ROI_Master_Sheet.md` |

3. Present routing suggestions to user with confidence level

4. Ask user to confirm or modify routing

**Example:**
```
Routing Analysis:

Section 1: Case study "Agency Data Lake"
  → Suggested: Create knowledge/proof_points/case_studies/Agency_Data_Lake.md
  → Also update: knowledge/proof_points/00_ROI_Master_Sheet.md
  → Confidence: HIGH

Section 2: Brand positioning notes
  → Suggested: knowledge/brand/00_CORE_Identity_Positioning.md
  → Confidence: MEDIUM

Section 3: Pricing mention ($5k-$10k)
  → Suggested: knowledge/brand/01_CORE_Services_Pricing.md
  → Confidence: HIGH
  → ⚠️  Warning: Pricing changes may require updates to Sales_Calls.md

Does this routing look correct? (y/n/modify)
```

---

### Step 4: Refactor Content

**Goal:** Integrate content properly without duplicating or appending

**Actions:**
1. For each target file:
   - Read the current content
   - Identify the specific section where new content belongs
   - Show user the existing content in that section

2. Discuss with user:
   - Is this new information or an update to existing?
   - Should we replace existing content or merge?
   - Are there any contradictions to resolve?

3. Check for ripple effects:
   - **If updating ICP**: Ask "Should we also update Prospecting.md qualification checklist?"
   - **If updating pricing**: Ask "Should we update Sales_Calls.md objection handling?"
   - **If updating services**: Ask "Does this affect brand positioning claims?"

4. Get user confirmation before making changes

**Example:**
```
Target: knowledge/brand/01_CORE_Services_Pricing.md
Section: ## 1. The Service Tiers → Tier 1: The Deep-Scan

Current content (lines 21-23):
"Investment: $4,000 - $8,000"

New content from raw file:
"Pricing: $5,000 - $10,000"

This is a pricing change. How should I handle this?
  [1] Replace old pricing with new (recommended for updates)
  [2] Keep existing pricing (discard new)
  [3] Show me both and I'll manually merge

⚠️  Ripple Effect Warning:
This pricing is also mentioned in:
- knowledge/brand/playbooks/Sales_Calls.md (objection handling)
- knowledge/brand/playbooks/Prospecting.md (qualification criteria)

Should I update those files too? (y/n/selective)
```

---

### Step 5: Execute Changes

**Goal:** Make the actual file modifications

**Actions:**
1. For each target file, use the Edit tool to:
   - Locate the specific section
   - Rewrite the section integrating new information
   - Delete any deprecated content

2. For case studies:
   - Look at existing case study files for format (e.g., `knowledge/proof_points/case_studies/Agency_Data_Lake.md`)
   - Create new file following the "Problem → Plumbing → Flow" structure
   - Extract metrics and update `knowledge/proof_points/00_ROI_Master_Sheet.md`

3. After each modification:
   - Show user a summary of changes (lines added/removed)
   - Ask for confirmation before proceeding to next file

4. Keep track of all modified files for commit message

**Example:**
```
Executing changes...

✓ Modified knowledge/brand/01_CORE_Services_Pricing.md
  - Updated pricing in Tier 1 section
  - Lines changed: +3, -2

✓ Modified knowledge/brand/playbooks/Sales_Calls.md
  - Updated pricing reference in objection handling
  - Lines changed: +1, -1

✓ Created knowledge/proof_points/case_studies/Agency_Data_Lake.md
  - New file following Problem → Plumbing → Flow format
  - Lines: +87

✓ Modified knowledge/proof_points/00_ROI_Master_Sheet.md
  - Added metrics to "Cost Reduction" section
  - Lines changed: +2, -0

Total: 3 modified, 1 created
```

---

### Step 6: Cleanup & Git

**Goal:** Archive processed file and create commit

**Actions:**
1. Move the processed file:
   ```bash
   mv raw_files/unprocessed/[filename] raw_files/processed/[filename]_[date]
   ```

2. Create a descriptive git commit:
   ```bash
   git add -A
   git commit -m "Ingest: [Summary]

   [Details of changes]
   - Modified: [list of files]
   - Created: [list of files]
   - Ripple updates: [list of files]

   Processed: raw_files/unprocessed/[filename]"
   ```

3. Show user summary:
   - Files modified/created
   - Where raw file was moved
   - Commit message

4. Ask: "Process another file?" or "All done!"

**Example:**
```
✅ Ingestion Complete!

Files Modified:
  - knowledge/brand/01_CORE_Services_Pricing.md
  - knowledge/brand/playbooks/Sales_Calls.md
  - knowledge/proof_points/00_ROI_Master_Sheet.md

Files Created:
  - knowledge/proof_points/case_studies/Agency_Data_Lake.md

Processed File:
  Moved: raw_files/unprocessed/case_studies.md
  To: raw_files/processed/case_studies_2026-01-06.md

Git Commit:
  Message: "Ingest: Case study updates and pricing revision"
  Status: Committed ✓

The unprocessed folder now has 1 remaining file.
Process next file? (y/n)
```

---

## Content Routing Reference

Instead of hardcoding all rules, reference these repository files:

- **`CONTRIBUTING.md`** - Global workflow and routing table
- **`knowledge/brand/INSTRUCTIONS.md`** - Brand content routing and update protocol
- **`knowledge/icp/INSTRUCTIONS.md`** - ICP update protocols and verification
- **`knowledge/proof_points/README.md`** - Case study ingestion format

---

## Examples & Templates

Point to existing files as examples:

### Case Study Format
See `knowledge/proof_points/case_studies/Agency_Data_Lake.md` for the standard structure:
- Section 1: The Context (The "Before")
- Section 2: The "Plumbing" (The Fix)
- Section 3: The "Flow" (Results & ROI)

### Refactoring Examples
Compare git history to see how content was refactored (not appended) in previous commits

### Routing Decisions
Check `CONTRIBUTING.md` routing table for the authoritative mapping of content types to target files

---

## Tips for Success

1. **Always read CONTRIBUTING.md first** - It contains the authoritative protocols
2. **Ask user questions** - Don't guess routing or make assumptions
3. **Show before/after** - Let user see what will change before executing
4. **Check ripple effects** - ICP, pricing, and service changes often affect multiple files
5. **Use existing files as templates** - Especially for case studies
6. **Never append** - Always integrate into existing sections
7. **Git commits tell a story** - Make them descriptive with context

---

## Common Patterns

### Pattern 1: Simple Content Addition
Raw file contains new case study → Create new case study file + update ROI Master Sheet

### Pattern 2: Content Update (Refinement)
Raw file has updated pricing → Replace pricing in Services file + update Sales playbook

### Pattern 3: Content Update (Pivot)
Raw file changes core positioning → Update Identity file + verify consistency across all playbooks

### Pattern 4: Multi-Target Content
Raw file has multiple topics → Route each section to appropriate file, process sequentially

### Pattern 5: Deprecated Content
Raw file says "we no longer do X" → Search for X across all files, delete all mentions
