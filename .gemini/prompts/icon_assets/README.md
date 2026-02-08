# Icon Assets — Generation Guide

Small modular icons for the Inform Growth website. Infrastructure-focused, no mascot, no faces on objects.

---

## Core Rules

1. **Cyan (#00FFFF) is the IMAGE background only** — chroma-key utility color for post-production removal. It fills the area OUTSIDE the white sticker border. **Zero cyan inside any sticker.**
2. **No text on images** — no labels, numbers, tick marks, brand names. Dollar signs ($) acceptable as visual symbols.
3. **No faces or characters on objects** — no eyes, mouths, smiles, or expressions on tools, pipes, gauges, or lenses. Exception: `01_ai_clog.md` has a small generic robot (not a mascot).
4. **Flat vector only** — no gradients, no 3D shading, no photorealism.
5. **Element limits** — 3-4 elements max for icons.
6. **Die-cut sticker** — white border (6-8px) follows the IRREGULAR SILHOUETTE of the subject. NOT a circle, NOT a rectangle, NOT a badge. No additional frames or geometric shapes around the subject.
7. **1930s rubber hose animation style** — bendy, rounded, exaggerated proportions. Personality through mechanical elements, not characters.
8. **Gauges** — color zones only (Rust Orange danger / ROI Green safe). No numbers.

---

## Sticker Color Palette (use ONLY these inside stickers)

| Color | Hex | Usage |
| :--- | :--- | :--- |
| ROI Green | `#39FF14` | Success, healthy flow, clean systems |
| Rust Orange | `#D35400` | Problems, corrosion, leaks, warnings |
| Light Gray | `#8A8A8A` | Pipe bodies, tools, structural elements |
| Dark Gray | `#3A3A3A` | Panel bodies, depth, housings |
| Vintage Cream | `#F5F5DC` | Gauge faces, highlights |
| White | `#FFFFFF` | Sticker borders |
| Black | `#000000` | Outlines (2-3px for icons), linework |

## Chroma-Key Background (NOT a sticker color)

| Color | Hex | Usage |
| :--- | :--- | :--- |
| Cyan | `#00FFFF` | Fills ONLY the area outside the white sticker border |

---

## Icon List

1. `01_ai_clog.md` — Robot stuck in funnel (only icon with a character)
2. `02_broken_gauge.md` — Shattered pressure gauge in danger zone
3. `03_data_debt_pipes.md` — Tangled, leaking pipe mess
4. `04_gauge_antenna.md` — Healthy gauge with telemetry antenna
5. `05_magnifying_glass_pipe.md` — Magnifying glass revealing pipe leak
6. `06_time_debt.md` — Clock clogging a pipe
7. `07_wrench_pipes.md` — Wrench tightening a clean pipe
8. `08_clean_pipe.md` — High-pressure clean pipe (success state)
9. `09_rusty_pipe.md` — Corroded, leaking pipe (problem state)
10. `10_control_panel.md` — Dashboard with healthy gauges

---

## Quality Checklist

**Before marking any icon complete:**

- [ ] Cyan background ONLY outside the white sticker border (zero cyan inside)
- [ ] White border follows the subject's irregular silhouette (NOT a circle, rectangle, or badge)
- [ ] No additional frames, outlines, or geometric shapes around the subject
- [ ] No text, labels, or numbers anywhere on the image
- [ ] No faces, eyes, mouths, or expressions on objects (except 01_ai_clog robot)
- [ ] Flat colors only (no gradients, no 3D)
- [ ] Bold black outlines (2-3px) on all elements
- [ ] White die-cut border present and consistent (6-8px)
- [ ] Colors match exact hex codes from sticker palette above
- [ ] Readable at 375px mobile width
- [ ] Element count within limits (3-4 max)
- [ ] Gauges use color zones only (no numbers)

---

## File Delivery

**Naming:** `icon_description.png`
**Format:** PNG with transparent background, 300 DPI
**Location:** `/public/icons/` for website
