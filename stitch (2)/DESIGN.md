```markdown
# Design System: The Kinetic Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Curated Kinetic"**
This design system moves away from the static, rigid grids of traditional corporate portfolios. For a Senior Product Manager, the design must balance high-level strategic authority with the "fun" energy of a builder. We achieve this through **Intentional Asymmetry** and **Dynamic Whitespace**. 

The system rejects the "boxed-in" look of standard templates. Instead, it treats the browser as an open gallery floor where content floats with purpose. By utilizing extreme typography scales and overlapping "ghost" layers, we create a sense of forward motion—mirroring the iterative, fast-paced nature of modern product management.

---

## 2. Colors & Surface Logic
The palette is anchored by a high-octane orange (`primary: #ab3600`) set against a pristine, breathable canvas (`surface_container_lowest: #ffffff`).

### The "No-Line" Rule
**Explicit Instruction:** Use of 1px solid borders for sectioning or containment is strictly prohibited. Structure must be defined through background color shifts or the "Ghost Border" technique. 
- Use `surface_container_low` (#f3f3f3) to define a section background against the main `surface` (#f9f9f9).
- Use `surface_container_high` (#e8e8e8) to create subtle inset areas for code snippets or data highlights.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine paper.
- **Base Layer:** `surface` (#f9f9f9).
- **Secondary Content Blocks:** `surface_container` (#eeeeee).
- **Interactive Cards:** `surface_container_lowest` (#ffffff) to create a "pop" effect against the slightly darker background.

### The "Glass & Gradient" Rule
To inject "soul" into the minimalism, avoid flat orange blocks. Use a subtle linear gradient for hero CTAs:
- **Signature Gradient:** `primary` (#ab3600) to `primary_container` (#ff5f1f) at a 135-degree angle.
- **Glassmorphism:** For floating navigation or modal overlays, use `surface` at 80% opacity with a `20px` backdrop-blur.

---

## 3. Typography
The typography is the voice of the system: **Plus Jakarta Sans** provides a friendly, geometric authority for headers, while **Inter** ensures relentless readability for complex product case studies.

*   **Display (Plus Jakarta Sans):** Use `display-lg` (3.5rem) for hero statements. Set with tight letter-spacing (-0.02em) to feel "heavy" and authoritative.
*   **Headlines (Plus Jakarta Sans):** `headline-lg` (2rem) should be used for section titles, often paired with an orange accent underline or a leading `01.` `02.` numbering system in `primary`.
*   **Body (Inter):** `body-lg` (1rem) is the workhorse. Increase line-height to 1.6 for long-form case studies to ensure maximum breathability.
*   **Label (Inter):** Use `label-md` (0.75rem) in all-caps with increased letter-spacing (+0.05em) for category tags or metadata.

---

## 4. Elevation & Depth
We eschew heavy shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by placing a `surface_container_lowest` card (Pure White) on a `surface_container_low` (Light Gray) background. This creates a "soft lift" that feels architectural rather than digital.
*   **Ambient Shadows:** For floating elements (like a "Let's Chat" button), use an ultra-diffused shadow: `0px 20px 40px rgba(171, 54, 0, 0.08)`. This tints the shadow with the primary orange, mimicking natural light reflection.
*   **The "Ghost Border" Fallback:** If visual separation is failing, use `outline_variant` (#e3bfb3) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary_container`), `xl` (0.75rem) rounded corners, and `on_primary` (#ffffff) text. Use `spacing-5` for horizontal padding.
- **Secondary:** `surface_container_highest` (#e2e2e2) background with `on_surface` text. No border.
- **Tertiary:** Pure text in `primary` with a 2px bottom margin that expands on hover.

### Cards & Case Study Previews
- **Strict Rule:** No dividers. Use `spacing-8` or `spacing-10` to separate content blocks.
- **Style:** Background `surface_container_lowest`, `xl` rounded corners. Images within cards should have a `md` (0.375rem) corner radius to feel nested and "held."

### Input Fields
- **Background:** `surface_container_low`. 
- **Active State:** Shift background to `surface_container_lowest` and apply a 2px "Ghost Border" using `primary`. 
- **Label:** Always use `label-md` floating above the input, never placeholder text alone.

### Interactive "Product DNA" Chips
- Used for PM skills (e.g., "SQL", "Roadmapping").
- **Style:** `surface_container_high` background, `full` (9999px) roundedness, `body-sm` typography. On hover, the chip should transform to the `primary` color.

---

## 6. Do's and Don'ts

### Do
- **Use "Power Grids":** Align text to a strict left-margin, but let images and orange accent shapes bleed off the right edge of the screen to create energy.
- **Embrace the Orange:** Use the orange for impact—large quotes, bullet points, or "View Project" arrows.
- **Prioritize Breathing Room:** If a section feels "busy," double the vertical padding using `spacing-20` (7rem).

### Don't
- **Don't use 100% Black:** Never use #000000. Use `on_surface` (#1a1c1c) for high-contrast text to keep the vibe sophisticated.
- **Don't use Box Shadows on everything:** Only "floating" interactive elements get shadows. Content cards stay flat and rely on tonal shifts.
- **Don't use sharp corners:** This is an "approachable" system. Avoid `none` or `sm` roundedness scales; stick to `lg` and `xl`.

---

## 7. Signature Interaction: The "Kinetic Hover"
When hovering over a project card or a primary CTA, the element should not just change color—it should scale slightly (1.02x) and the "Ambient Shadow" should increase in spread. This provides the "high-energy" feedback the user requested, signaling a product that is responsive and alive.```