# Visual Style Guide: The "Inform" Aesthetic

This document defines the visual identity for Inform Messaging's content. It bridges the gap between **Mid-Century Modern Design** (Exclusive, Refined) and **Industrial Reliability** (Plumbing, Trade Heritage).

## 🎨 Core Aesthetic: "Montecito Modern"

Our visual language channels 1950s/60s West Coast modernism—think luxury lifestyle magazines explaining industrial infrastructure. It uses the "cartoon" charm of vintage commercial art but with architectural precision.

*   **Keywords:** Mid-Century, Vintage Commercial, Offset Printing, Hunter Green, Matte Copper, Refined Mascot.
*   **Vibe:** "A 1960s luxury plumbing manual found in a Santa Barbara estate."

## 🌈 Color Palette

*   **Background:** Cream / Off-White (`#FDFBF7`) — mimicking aged high-end paper.
*   **Primary (West Coast):** Hunter Green (Foliage) & Deep Teal (Pacific Ocean).
*   **Accent (Warmth):** Mustard Yellow (Sun) & Terracotta (Roof tiles).
*   **The "Pipe" Metal:** Matte Copper / Bronze.

## 🖼️ Nano-Banana Generation Guidelines

When using the `/image` or `/icon` commands, adhere to these defaults.

### Standard Post Images
*   **Style:** `vintage`, `vector-art`, `flat-design`
*   **Prompt Structure:** `[Subject] in the style of mid-century modern commercial art. Flat geometric shapes, inky variable-width outlines, offset printing effect. Palette: Cream background, Hunter Green, Deep Teal, Terracotta accents. High-end, refined, exclusive.`
*   **Negative Constraints:** No photorealistic people, no 3D renders, no gradients (unless mimicking print texture), no generic corporate Memphis style.

### Icons / Mascots
*   **Style:** `minimalist`, `vintage-cartoon`
*   **Features:** Stylized trade mascots (e.g., a walking wrench in a bow tie, an anthropomorphic valve).
*   **Lines:** Thick, slightly imperfect ink lines.
*   **Metaphors:**
    *   *Data:* Fluid flowing through copper tubes.
    *   *Problems:* Rusted "bad" pipes in muted grey vs. clean Copper.
    *   *Solutions:* A refined mascot "fixing" the flow with a golden wrench.

## 📝 Usage in Pipeline

1.  **Read the Post:** Identify the core "Pain Point" or "Solution".
2.  **Translate to Metaphor:**
    *   *Bad Pricing* -> Leaky bucket or rusted meter.
    *   *Complex Data* -> Tangled knot of pipes.
    *   *Streamlined Ops* -> Clean, straight copper piping.
3.  **Generate:** Use the `generate_image` or `generate_icon` tools.
4.  **Save:** Store in `content_pipeline/assets/`.
