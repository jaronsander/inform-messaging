# Visual Style Guide: The "Inform" Aesthetic

This document defines the visual identity for Inform Messaging's content. It pivots from traditional corporate design to a bold, high-contrast **"Digital Plumbing"** aesthetic rooted in vintage animation.

## 🎨 Core Aesthetic: "Digital Plumbing Infrastructure"

Our visual language combines **1930s Rubber Hose Animation** (think early Disney or Cuphead) with a modern **Streetwear/Sticker Culture** vibe. It presents complex RevOps concepts as tangible, mechanical plumbing problems — pipes, valves, gauges, and tools rendered with vintage cartoon personality.

*   **Keywords:** Rubber Hose Animation, Die-Cut Vinyl Sticker, High Contrast, Neon on Dark, Industrial, Infrastructure.
*   **Vibe:** "A vintage mechanic's manual reimagined as a cyberpunk sticker pack."

## 🌈 Color Palette

We use a high-contrast "Dark Mode" palette to stand out in bright feeds.

| Role | Color | Hex | Usage |
| :--- | :--- | :--- | :--- |
| Canvas/Background | Carbon Gray | `#2B2B2B` | Deep industrial backdrop for final composites |
| Success/Signal | ROI Green | `#39FF14` | Healthy flow, sparks, success states, clean systems |
| Warning/Error | Rust Orange | `#D35400` | Leaks, corrosion, clogs, broken gauges, warnings |
| Infrastructure | Light Gray | `#8A8A8A` | Pipe bodies, tools, structural elements |
| Depth/Housing | Dark Gray | `#3A3A3A` | Panel bodies, housings, heavy structural elements |
| Highlights | Vintage Cream | `#F5E7D0` | Gauge faces, paper, highlights, body text |
| Border/Contrast | White | `#FFFFFF` | Mandatory bold sticker outline around assets |
| Linework | Black | `#000000` | Outlines (3-4px), structural lines |
| Utility (BG Only) | Cyan | `#00FFFF` | Chroma-key background for generation — never inside stickers |

## 🖥️ UI / Web Color System

The core palette above governs illustration and sticker assets. For the website and UI, colors adapt per theme while preserving semantic meaning.

### Core Palette (Shared)

| Name | Hex | Usage |
| :--- | :--- | :--- |
| Carbon Gray | `#2B2B2B` | Dark backgrounds, text on light mode |
| Carbon Gray Light | `#3A3A3A` | Card/section backgrounds (dark mode), muted text (light mode) |
| ROI Green | `#39FF14` (dark) / `#1A6B35` (light) | Primary accent, CTAs, borders |
| Rust Orange | `#D35400` | Secondary accent (both modes) |

### Dark Mode

| Role | Value |
| :--- | :--- |
| Page background | `#2B2B2B` Carbon Gray |
| Section/card backgrounds | `#3A3A3A` Carbon Gray Light |
| Text | `#FFFFFF` White |
| Muted text | `#F5E7D0` Vintage Cream |
| Accent | `#39FF14` ROI Green (neon) |
| Accent glow | `rgba(57, 255, 20, 0.3)` |

### Light Mode

| Role | Value |
| :--- | :--- |
| Page background | `#F5E7D0` Vintage Cream |
| Section backgrounds | `#F1E2CB` / `#E7D7BE` (warm cream variants) |
| Card backgrounds | `#F4E6D0` / `#EADCC5` (warm cream variants) |
| Text | `#2B2B2B` Carbon Gray |
| Muted text | `#3A3A3A` Carbon Gray Light |
| Accent | `#1A6B35` ROI Green (forest — replaces neon for readability on cream) |
| Border subtle | `#C9B79A` (warm tan) |
| Accent glow | `rgba(26, 107, 53, 0.2)` |

### Mode Adaptation Rules

*   **ROI Green adapts:** `#39FF14` neon on dark backgrounds, `#1A6B35` forest on light backgrounds. Same semantic role (success/CTA), different luminance.
*   **Rust Orange stays constant:** `#D35400` has sufficient contrast on both Carbon Gray and Vintage Cream.
*   **Vintage Cream inverts role:** Muted text color in dark mode, page background in light mode.
*   **Carbon Gray inverts role:** Page background in dark mode, primary text color in light mode.

## 🔠 Typography

Our typography balances vintage craft with terminal-style engineering.

*   **Headings:** **Fraunces** (Bold/Black weight). A high-contrast, classic serif that feels like an old industrial brand.
*   **Subheadings/Body:** **Space Mono**. A clean, fixed-width monospaced font that communicates "Code," "Data," and "Engineering Rigor."

## 📱 Mobile-First Design Principles

72% of LinkedIn engagement happens on mobile. All designs must be mobile-optimized.

*   **Vertical Format Preferred:** Design for vertical scroll. Horizontal layouts lose engagement.
*   **High Contrast for Small Screens:** Our Carbon Gray + ROI Green palette already optimizes for this. Ensure text is readable at phone scale.
*   **Touch-Friendly Sizing:** Buttons, CTAs, and interactive elements should be large enough for thumb interaction.
*   **Minimal Line Length:** Keep text blocks narrow for easy reading on mobile (40-60 characters max per line).
*   **No Tiny Details:** Avoid intricate illustrations that don't render clearly on small screens. Rubber hose style's bold simplicity works perfectly here.

## 🖼️ Nano-Banana Generation Guidelines

When using the `/image` or `/icon` commands, adhere to these updated defaults.

### Modular Asset Generation
We prefer **Modular Assets** (stickers) over full scenes. This allows for flexible composition in Canva.
*   **Style:** `sticker`, `vector-art`, `cartoon`, `infrastructure`
*   **Prompt Structure:** `[Subject] depicted as a die-cut vinyl sticker where the white border follows the irregular silhouette of the subject (not a circle or rectangle). 1930s rubber hose animation style. Industrial infrastructure. High contrast. No faces on objects.`
*   **Negative Constraints:** No photorealism, no 3D shading (flat vector only), no gradients, no text or labels on images.
*   **Background Removal:** Generate with Cyan (#00FFFF) background as chroma-key utility color for easy removal. Final composites use Carbon Gray (#2B2B2B).

### Generation Constraints
*   **No text on images:** No labels, numbers, tick marks, or brand names. Dollar signs ($) are acceptable as visual symbols.
*   **Gauges:** Use color zones only (Rust Orange for danger, ROI Green for safe). No numbers, no tick marks.
*   **Element limits:** 6-8 elements max for major illustrations, 3-4 for icons. Fewer elements = higher quality composition.
*   **Cyan containment:** Cyan (#00FFFF) is the background only. Zero cyan inside any sticker or asset.
*   **Bold outlines:** 3-4px black outlines on all elements. 2-3px for small icons (400px and under).
*   **Sticker border:** 8-10px white border for standard assets. 6-8px for small icons. Border follows the IRREGULAR SILHOUETTE of the subject — NOT a circle, rectangle, or badge shape. No additional frames or geometric shapes around the subject.

### Visual System: Infrastructure-Only
*   **No Mascot:** All visuals are infrastructure-focused (pipes, valves, gauges, tools).
*   **Character Exception:** Small generic characters acceptable for specific metaphors (e.g., tiny robot stuck in funnel for "AI clog"), but never a recurring mascot.
*   **Personality:** Rubber hose style provides playfulness through bendy pipes, exaggerated mechanical elements, and cartoon physics—not through characters.

### Metaphors
*   **Data/Process:** Illustrated as physical pipes, valves, and gauges.
*   **The Tools:** Industrial plunger, wrench, magnifying glass, toolbox—metaphors for "fixing" and "refactoring."
*   **The Problem:** Leaks (rust orange drips), clogs (knotted hoses), corrosion (rust orange patches), broken gauges.
*   **The Solution:** Clean pipe segments, glowing green pressure gauges, smooth flowing green liquid, organized valve systems.

### Infographics vs. Stock Photos
*   **Infographics outperform stock photos 2.4x** on LinkedIn. Always choose custom illustrations, diagrams, or data visualizations over generic B2B stock imagery.
*   **Personal/custom illustrations > generic assets:** Our rubber hose style is inherently custom and stands out in feeds filled with flat corporate design.

## 📝 Usage in Pipeline

1.  **Read the Post:** Identify if it's a "Problem" post or a "Solution" post.
2.  **Select Assets:**
    *   Search the `content_pipeline/assets/asset_catalog.md` for existing infrastructure elements.
    *   If missing, generate a new **Modular Sticker** version of the asset.
3.  **Check Consistency:** Ensure colors, style, and contrast match brand guidelines.
4.  **Save:** Store in `content_pipeline/assets/`.

---

## 🎠 LinkedIn Carousel Optimization

LinkedIn carousels achieve 1.45x reach multiplier and are ideal for educational content.

### Optimal Structure
*   **Slide Count:** 5-12 slides performs best. Each swipe = engagement signal.
*   **Consumption Rate Matters:** A 5-slide carousel viewed completely outperforms a 12-slide carousel where users drop off halfway. Design for full completion.
*   **Vertical Format:** Works better on mobile (72% of engagement). Design slides in vertical or square aspect ratios.

### Slide-by-Slide Design
*   **Slide 1 (The Hook):** Bold headline, strong infrastructure visual (broken gauge, tangled pipes, or problem illustration). Must grab attention instantly.
*   **Middle Slides (2-4 or 2-10):** High-contrast text with 1-2 sentences per slide. Use ROI Green for key stats, Rust Orange for warnings/problems. Each slide should take 5-8 seconds to read (optimizes dwell time).
*   **Final Slide (The Question):** End with a genuine question to drive 15+ word comments. Simple text layout with supporting infrastructure icon.

### Visual Guidelines for Carousels
*   **High Contrast:** Carbon Gray background + ROI Green/Rust Orange text ensures readability on small screens.
*   **Large, Bold Typography:** Use Fraunces Bold for headlines. Ensure text is readable at thumbnail size (users preview before swiping).
*   **Minimal Elements Per Slide:** 1-2 visual elements max. Let each slide breathe. Overcrowding kills mobile readability.
*   **Consistent Background:** Use pipes background at 20-30% opacity across all slides for brand consistency.
*   **Progress Indicator:** LinkedIn shows "1 of 5" automatically—design with this in mind (don't add your own slide numbers).