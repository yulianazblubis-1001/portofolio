```markdown
# Design System Document: The Kinetic Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Energetic Strategist"**
This design system rejects the "corporate blue" monotony of traditional Product Management portfolios. Instead, it embraces a high-end editorial aesthetic characterized by **Organic Kineticism**. We move beyond static, grid-bound layouts to create a sense of forward motion and professional playfulness. 

The system achieves a premium feel not through complexity, but through **intentional asymmetry**, massive typographic scales, and a "gravity-defying" layering logic. By pairing the friendliness of rounded forms with the stark authority of a pure white canvas and vibrant orange accents, we signal a PM who is both approachable and results-driven.

---

## 2. Colors & Tonal Logic
The palette is rooted in high-contrast energy. We use a "Pure White" base (`surface-container-lowest: #ffffff`) to ensure the vibrant orange (`primary`) feels electric rather than muddy.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders are strictly prohibited for sectioning or containment. Boundaries must be defined solely through background color shifts.
*   Use `surface-container-low` (#f0f1f1) for large secondary sections.
*   Use `surface-container` (#e7e8e8) for nested information blocks.
*   This creates a "molded" look rather than a "boxed" look.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. 
*   **Base Layer:** `surface` (#f6f6f6) or `surface-container-lowest` (#ffffff).
*   **Interaction Layer:** Use `surface-container-high` (#e1e3e3) for cards that need to "pop" against a low-contrast background.
*   **The Signature Pop:** Reserve `primary` (#a63400) and `primary-fixed` (#ff7948) for elements requiring immediate kinetic attention (CTAs, active states).

### The "Glass & Gradient" Rule
To avoid a flat, "template" feel, use **Backdrop Blurs** on floating navigation bars and modal overlays. Apply a subtle linear gradient to main CTAs transitioning from `primary` (#a63400) to `primary-container` (#ff7948) at a 135-degree angle. This adds "soul" and dimension to the vibrant orange.

---

## 3. Typography
We use a dual-font strategy to balance "Playful PM" with "Senior Leader."

*   **Display & Headlines (Plus Jakarta Sans):** This is our "Kinetic" voice. It is modern, clean, and has a subtle geometric friendliness. 
    *   *Usage:* Use `display-lg` (3.5rem) for hero statements. Tighten letter-spacing (-0.02em) to create a tight, editorial impact.
*   **Body & Titles (Be Vietnam Pro):** This provides the "Approachability." It is highly legible and works perfectly for long-form case studies.
    *   *Usage:* `body-lg` (1rem) for core project descriptions.

**Hierarchy Note:** Always lead with scale. A `display-lg` headline should feel massive compared to `body-md` text to create the "High-Contrast" style requested.

---

## 4. Elevation & Depth
Depth is achieved through **Tonal Layering** and physics-based logic, not heavy drop shadows.

*   **The Layering Principle:** Place a `surface-container-lowest` card (Pure White) on a `surface-container-low` (#f0f1f1) background. The 2% shift in brightness provides a "Soft Lift" that feels high-end and intentional.
*   **Ambient Shadows:** For floating elements (like the caricature or a floating menu), use a shadow with a 40px blur, 0% spread, and 6% opacity. The shadow color must be derived from `on-surface` (#2d2f2f) to look natural.
*   **The "Ghost Border" Fallback:** If a divider is essential for mobile accessibility, use `outline-variant` (#acadad) at **15% opacity**. It should be felt, not seen.
*   **Kinetic Motion:** Elements should appear to float at different "altitudes." Use the caricature as an overlapping element that breaks the container bounds, creating a 3D layered effect.

---

## 5. Components

### Buttons (The Kinetic Triggers)
*   **Primary:** `primary` background, `on-primary` text. Use `rounded-full` (9999px) for a "pill" shape that feels friendly and modern.
*   **Secondary:** `surface-container-highest` background. No border.
*   **States:** On hover, shift the background to `primary-fixed-dim` (#fe5e1e) and apply a subtle "lift" using the Ambient Shadow.

### Cards & Case Study Blocks
*   **Forbid Dividers:** Use `spacing-10` (3.5rem) or `spacing-16` (5.5rem) to separate content blocks. 
*   **Structure:** A card should be a simple `surface-container-lowest` block with a `rounded-lg` (2rem) corner radius.

### Chips (Meta-Data)
*   Use `secondary-container` (#ffc3be) with `on-secondary-container` text for "Skills" or "Tools." 
*   Keep them `rounded-full` to maintain the approachable, non-rigid feel.

### Input Fields
*   Background: `surface-container-low`. 
*   Border: None, until focus. 
*   Focus State: 2px solid `primary`.

### Navigation
*   Use a floating "Dock" style navigation at the bottom or top center. 
*   Background: `surface` at 80% opacity with a `20px` backdrop blur (Glassmorphism).

---

## 6. Do's and Don'ts

### Do:
*   **Embrace White Space:** Use `spacing-20` (7rem) between major sections to let the "Pure White" background breathe.
*   **Use Asymmetry:** Place the caricature off-center, overlapping a text block to create kinetic energy.
*   **Bold Accents:** Use the Vibrant Orange for 10% of the screen real estate only—it’s a lightning bolt, not a floodlight.

### Don't:
*   **No Sharp Corners:** Never use `rounded-none`. Everything must have at least `rounded-sm` to maintain the "approachable" brand.
*   **No Rigid Grids:** Avoid perfectly symmetrical two-column layouts. Try a 60/40 split to create visual interest.
*   **No Pure Black:** Use `on-background` (#2d2f2f) for text. Pure black is too harsh for this "friendly" system.
*   **No Standard Lists:** Avoid bullet points. Use `primary` colored checkmarks or small `primary-container` circles to maintain the "Senior PM" polish.

---
*Director's Final Note: Remember, the white space is as much a design element as the orange. If the layout feels "busy," increase the spacing scale values and remove a container.*```