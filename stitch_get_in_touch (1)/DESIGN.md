# Design System Strategy: Editorial Vibrancy

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Energetic Curator."** 

This system moves beyond the sterile, "default" look of many minimalist portfolios by blending the structural authority of high-end editorial magazines with a punchy, vibrant spirit. While it inherits the spaciousness and sophisticated type hierarchy of the source inspiration, it rejects the monochromatic safety of standard minimalism. 

We break the "template" look through:
*   **Intentional Asymmetry:** Off-setting content blocks and using varying column widths to create a sense of movement.
*   **Tonal Depth:** Replacing harsh lines with soft background shifts and layered "glass" surfaces.
*   **Dynamic Contrasts:** Pairing large-scale, assertive display typography with electric pops of color to guide the eye and inject personality.

The result is a digital experience that feels custom-built, professional, and approachable—balancing the precision of a creative director with the energy of a boutique studio.

---

## 2. Colors
Our palette is anchored by a high-clarity background (`#fcf8ff`) and punctuated by high-chroma accents that demand attention without overwhelming the content.

### The Palette
*   **Primary (`#b60058`):** An electric pink used for critical actions and brand signatures.
*   **Secondary (`#904d00` / `#fd8b00`):** A vibrant orange used for secondary focus and playful highlights.
*   **Surface System:** Ranging from `surface` (`#fcf8ff`) to `surface_container_highest` (`#e2e0f8`), these tones provide the "air" and structural hierarchy of the layout.

### Architectural Rules
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Structural boundaries must be defined solely through background color shifts. For example, a content section using `surface_container_low` should sit directly against a `surface` background to define its territory.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers. An inner card (`surface_container_lowest`) should be nested within a section (`surface_container_low`) to create "natural" depth.
*   **The "Glass & Gradient" Rule:** Use Glassmorphism for floating elements. Combine `surface` colors with a 20-30px backdrop-blur and 60% opacity to create a "frosted glass" effect.
*   **Signature Textures:** For Hero sections or primary CTAs, use a subtle linear gradient transitioning from `primary` (`#b60058`) to `primary_container` (`#e11170`). This adds a premium "soul" that flat fills cannot replicate.

---

## 3. Typography
Typography is the primary engine of authority in this system. We use a high-contrast scale to create an editorial rhythm.

*   **Display & Headlines (Epilogue):** An assertive, geometric sans-serif that feels modern and architectural. Use `display-lg` for hero statements to command immediate attention.
*   **Titles & Body (Inter):** A workhorse typeface chosen for its mathematical clarity. `title-lg` provides a sophisticated bridge between headlines and content.
*   **Labels (Manrope):** A clean, slightly more friendly sans-serif used for utility text and metadata.

**The Editorial Rhythm:** Headlines should be set with tight letter-spacing (-2% to -4%) to feel like a printed magazine masthead, while body text uses generous line-height (1.6x) to ensure effortless readability against the "pop" accents.

---

## 4. Elevation & Depth
In "The Energetic Curator," depth is a feeling, not a drop-shadow.

*   **The Layering Principle:** Depth is achieved by "stacking" the surface-container tiers. Placing a `surface_container_highest` element on a `surface` background creates a clear hierarchy without a single line of CSS border.
*   **Ambient Shadows:** If a floating element (like a modal or navigation bar) requires a shadow, it must be an "Ambient Shadow." Use a blur value of 40px+, an opacity of 4%-6%, and a color derived from `on_surface` (a deep indigo-tinted shadow) rather than pure black.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline_variant` token at 15% opacity. It should be felt, not seen.
*   **Glassmorphism:** For the navigation bar or floating action buttons, use the surface tint with a `backdrop-filter: blur(12px)`. This integrates the component into the page layout by letting the vibrant background "pops" bleed through softly.

---

## 5. Components

### Buttons
*   **Primary:** Fill with the `primary` to `primary_container` gradient. White text (`on_primary`). High roundedness (`xl`).
*   **Secondary:** `surface_container_highest` background with `primary` text. No border.
*   **Tertiary:** Text-only in `primary` or `secondary`, with a `secondary_fixed` underline on hover.

### Cards & Lists
*   **Rule:** Forbid divider lines.
*   **Implementation:** Use vertical whitespace (Spacing `12` or `16`) to separate list items. For cards, use a `surface_container_low` background with an `xl` corner radius. 
*   **Hover State:** On hover, shift the background to `surface_container_high` and apply an Ambient Shadow.

### Inputs & Selection
*   **Input Fields:** Use `surface_container_low` for the field body. On focus, transition the "Ghost Border" to 100% opacity of the `primary` color.
*   **Chips:** Use `secondary_fixed` backgrounds for selection chips to provide that "vibrant" personality without the weight of a full button.

### Additional Portfolio Components
*   **Project Hero:** Use asymmetrical layout—title at `display-lg` on the left, high-quality imagery overlapping a `primary_fixed` decorative block on the right.
*   **The "Vibe" Quote:** Blockquotes should use `headline-md` in `tertiary`, styled with a large decorative quote mark in 10% opacity `primary`.

---

## 6. Do's and Don'ts

### Do
*   **Do** use the Spacing Scale rigorously. Generous margins (e.g., `24` for section padding) are what make the "minimalism" feel intentional.
*   **Do** mix your display sizes. A small `label-md` next to a `display-lg` creates a high-end, editorial feel.
*   **Do** use `primary` and `secondary` colors for highlights, like text selection color or "New" badges.

### Don't
*   **Don't** use 100% black text. Use `on_surface` (#1a1a2b) for a softer, more sophisticated contrast.
*   **Don't** use standard "drop shadows." If a component doesn't look right without a shadow, your surface layering isn't distinct enough.
*   **Don't** center-align everything. The source inspiration uses strong left-alignment; maintain this "grid-breaking" feel to avoid looking like a template.