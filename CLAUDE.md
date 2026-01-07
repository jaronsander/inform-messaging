# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is the **Single Source of Truth** for Inform Growth's brand, sales strategy, and operational knowledge base. It is a content/documentation repository (not a code repository) that follows strict maintenance protocols to prevent knowledge decay and duplication.

## Repository Architecture

### Core Principle: "Raw → Processed" Pipeline

All new information flows through a strict ingestion workflow:

1. **Ingest** → `raw_files/unprocessed/` (temporary holding pen)
2. **Process** → Extract truth and refactor into `knowledge/` directories
3. **Cleanup** → Delete the raw file after successful integration

**Critical Rule:** The `raw_files/unprocessed/` folder should be empty at the end of every session.

### Directory Structure

```
knowledge/
├── brand/              # Brand identity, services, and playbooks
│   ├── 00_CORE_Identity_Positioning.md    # WHO we are, WHO we serve
│   ├── 01_CORE_Services_Pricing.md        # WHAT we sell, pricing, ROI
│   ├── INSTRUCTIONS.md                     # Protocol for updating brand files
│   └── playbooks/
│       ├── Prospecting.md                  # Lead gen, outreach templates
│       ├── Sales_Calls.md                  # Sales scripts, objection handling
│       └── Content_Marketing.md            # Voice, tone, content themes
│
├── icp/                # Ideal Customer Profile definitions
│   ├── 00_ICP_Definition.md                # Target audience, firmographics
│   └── INSTRUCTIONS.md                     # Protocol for updating ICP
│
└── proof_points/       # Case studies and ROI evidence
    ├── 00_ROI_Master_Sheet.md              # High-level stats and hooks
    └── case_studies/                       # Detailed client engagements

raw_files/
├── unprocessed/        # Temporary: new documents awaiting processing
└── processed/          # Archive of processed raw files
```

## Critical Protocols

### 1. Refactor, Don't Append

**NEVER** paste new text at the bottom of existing files. Always:
- Locate the relevant section
- Rewrite it to integrate the new information
- Delete deprecated content immediately

**Example:**
- ❌ Bad: Adding a new pricing table below the old one
- ✅ Good: Replacing the pricing section and updating surrounding context

### 2. Single Source of Truth

Never duplicate core truths across files. If duplication is necessary:
- Update ALL instances simultaneously
- Check ripple effects across related files

**Example:** If you update pricing in `01_CORE_Services_Pricing.md`, verify consistency in `playbooks/Sales_Calls.md`.

### 3. Routing Logic for New Information

When processing new documents, route to the correct file:

| Content Type | Target File |
|-------------|-------------|
| Identity, tone, persona, competitors | `knowledge/brand/00_CORE_Identity_Positioning.md` |
| Service offerings, deliverables, pricing, ROI | `knowledge/brand/01_CORE_Services_Pricing.md` |
| Cold outreach, lead gen, triggers | `knowledge/brand/playbooks/Prospecting.md` |
| Sales scripts, objections, closing | `knowledge/brand/playbooks/Sales_Calls.md` |
| Marketing content, LinkedIn, voice | `knowledge/brand/playbooks/Content_Marketing.md` |
| ICP updates, target audience | `knowledge/icp/00_ICP_Definition.md` |
| Case studies, proof points | `knowledge/proof_points/` |

### 4. Update Workflow

When ingesting new information:

1. **Analyze:** Is this a Refinement, Expansion, or Pivot?
   - Pivots (changing core truth) require user confirmation
2. **Check Conflicts:** Does this contradict existing core documents?
3. **Execute:** Rewrite the specific section in the target file
4. **Ripple Check:** Update related files to maintain consistency
5. **Clean:** Remove deprecated information and delete raw file

### 5. ICP-Playbook Alignment

**Critical Dependency:** Changes to `knowledge/icp/00_ICP_Definition.md` MUST trigger updates to:
- `knowledge/brand/playbooks/Prospecting.md` (qualification checklist)
- Any other ICP-dependent content

## Common Workflows

### Processing Raw Files

```bash
# 1. Check for unprocessed files
ls raw_files/unprocessed/

# 2. Read the raw file
# 3. Identify routing destination using table above
# 4. Refactor content into target file(s)
# 5. Delete raw file after successful integration
rm raw_files/unprocessed/[filename]
```

### Adding a New Case Study

1. Extract core metrics → Add to `knowledge/proof_points/00_ROI_Master_Sheet.md`
2. Identify the "hook" (compelling one-liner)
3. Create detailed file in `knowledge/proof_points/case_studies/[Name].md`
4. Follow "Problem → Plumbing → Flow" format

### Updating Brand Voice or Positioning

1. Read `knowledge/brand/00_CORE_Identity_Positioning.md` for current truth
2. Make changes with user confirmation if it's a pivot
3. Check `knowledge/brand/playbooks/Content_Marketing.md` for alignment
4. Update sales scripts in `knowledge/brand/playbooks/Sales_Calls.md` if needed

## Brand-Specific Context

**Brand Identity:** "The Funnel Plumber" - RevOps Infrastructure Engineers for B2B SaaS
**Tone:** Clinical, Technical, Authoritative, Urgent (computer engineer, not marketer)
**Avoid:** Marketing fluff, synergy, holistic, ideate
**Use:** Refactor, latency, throughput, telemetry, leakage, schema

**The Core Value Prop:** Preventing revenue leakage through continuous observability and infrastructure engineering (not one-time fixes).
