# Infrastructure Assets — Generation Guide

All visual assets for the Inform Growth website. Infrastructure-focused, no mascot.

---

## Core Rules

1. **Cyan (#00FFFF) background only** — utility color for chroma-key removal. Zero cyan inside any sticker.
2. **No text on images** — no labels, numbers, tick marks, brand names, or descriptive text. Dollar signs ($) are acceptable as visual symbols.
3. **Flat vector only** — no gradients, no 3D shading, no photorealism.
4. **Element limits** — 6-8 elements max for major illustrations, 3-4 for icons.
5. **Gauges** — color zones only (Rust Orange danger / ROI Green safe). No numbers.
6. **Die-cut sticker** — white border (8-10px standard, 6-8px small icons) follows the IRREGULAR SILHOUETTE of the subject. NOT a circle, NOT a rectangle, NOT a badge. No additional frames or geometric shapes around the subject.
7. **1930s rubber hose animation style** — bendy, rounded, exaggerated proportions. Personality through mechanical elements, not characters.
8. **Mobile readability** — all assets must pass a 375px width test.

---

## Brand Color Palette (Sticker Colors Only)

| Color | Hex | Usage |
| :--- | :--- | :--- |
| Carbon Gray | `#2B2B2B` | Final composite backgrounds (NOT in generation) |
| ROI Green | `#39FF14` | Success, healthy flow, clean systems |
| Rust Orange | `#D35400` | Problems, corrosion, leaks, warnings |
| Light Gray | `#8A8A8A` | Pipe bodies, tools, structural elements |
| Dark Gray | `#3A3A3A` | Panel bodies, depth, housings |
| Vintage Cream | `#F5F5DC` | Gauge faces, highlights, paper |
| White | `#FFFFFF` | Sticker borders |
| Black | `#000000` | Outlines (3-4px), linework |
| Cyan | `#00FFFF` | Background ONLY (chroma-key utility) |

---

## Generation Priority

### Phase 1: Critical (Generate First)
1. `01_hero_isometric_pipe_system.md` — Homepage hero
2. `02_data_debt_tangled_pipes.md` — Problem section
3. `03_stage_icons_methodology.md` — Three methodology icons

### Phase 2: Service Tiers
4. `04_tier1_diagnostic_cutaway.md` — Tier 1 visualization
5. `05_tier2_before_after_transformation.md` — Tier 2 visualization
6. `06_tier3_control_panel_dashboard.md` — Tier 3 visualization

### Phase 3: Supporting
7. `07_supporting_problem_icons.md` — 7 modular icons
8. `10_case_study_icons.md` — 4 small card icons

### Phase 4: Additional
9. `09_toolbox_illustration.md` — Services page header
10. `08_background_patterns.md` — Background textures (lowest priority)

---

## Quality Checklist

**Before marking any asset complete:**

- [ ] Cyan background only (zero cyan inside sticker)
- [ ] White border follows the subject's irregular silhouette (NOT a circle, rectangle, or badge)
- [ ] No additional frames, outlines, or geometric shapes around the subject
- [ ] No text, labels, or numbers anywhere on the image
- [ ] Flat colors only (no gradients, no 3D)
- [ ] Bold black outlines (3-4px) on all elements
- [ ] White die-cut border present and consistent
- [ ] Colors match exact hex codes
- [ ] Readable at 375px mobile width
- [ ] Element count within limits
- [ ] Gauges use color zones only

---

## File Delivery

**Naming:** `category_description.png`
**Format:** PNG with transparent background, 300 DPI
**Location:** `/public/` for website, `/content_pipeline/assets/infrastructure/` for source files
