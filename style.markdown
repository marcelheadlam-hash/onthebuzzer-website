# Design System Strategy: Broadcast Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Cinematic Broadcast."** 

This system moves away from the static, "boxed-in" nature of traditional corporate sites, instead adopting the high-octane, polished aesthetic of a premium television production. We achieve this through a "High-End Editorial" lens: utilizing bold, oversized typography, intentional asymmetry, and a focus on "The Frame." 

By leveraging sharp edges (`0px` radius) and deep tonal layering, we create a sense of professional authority. The layout should feel like a motion graphics storyboard—dynamic, confident, and expensive. We break the template look by allowing elements to overlap, using wide-measure spacing, and treating the background not as a flat canvas, but as a multi-dimensional stage.

## 2. Colors: Tonal Depth & The Amber Glow
The palette is rooted in a "Late Night" environment. We use the deep `#131313` (`surface`) as our base, with the terracotta `#C4856A` (`primary_container`) acting as a spotlight.

*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. To separate content blocks, use a shift from `surface` to `surface_container_low`. This creates a natural, sophisticated transition that feels like light falling on different planes rather than a grid.
*   **Surface Hierarchy & Nesting:** Treat the UI as layers of light.
    *   **Base:** `surface` (#131313)
    *   **Recessed Content:** `surface_container_lowest` (#0E0E0E) for deep, immersive sections.
    *   **Elevated Content:** `surface_container_high` (#2A2A2A) for interactive cards or floating elements.
*   **The "Glass & Gradient" Rule:** For key call-outs, use a subtle radial gradient from `primary` (#FDB699) to `primary_container` (#C4856A) at a 45-degree angle. This adds "soul" and prevents the amber from looking flat. For floating navigation or overlays, apply a `backdrop-blur` (20px+) to the `surface_variant` at 60% opacity to maintain the cinematic depth.

## 3. Typography: The Editorial Voice
Our type system is designed to mimic high-end magazine spreads and broadcast titles.

*   **Display & Headlines (Epilogue):** These are your "Hero" voices. Use `display-lg` for impactful punchlines. The tight kerning and bold weight of Epilogue provide a modern, architectural feel. For a "Broadcast" look, try using `headline-lg` in all-caps with increased letter spacing (`0.1em`).
*   **Body (Inter):** Inter provides a neutral, highly readable counterpoint to the aggressive headlines. Ensure `body-lg` is used for introductory paragraphs to maintain a premium feel.
*   **Labels (Space Grotesk):** This is our "technical" font. Used for dates, timestamps, or "Live" indicators, Space Grotesk adds a touch of digital precision that aligns with the 'On The Buzzer' production theme.

## 4. Elevation & Depth: Tonal Layering
In this system, we do not use shadows to create "pop." We use light.

*   **The Layering Principle:** To make a card feel interactive, place a `surface_container_high` element on top of a `surface` background. The contrast is enough to define the boundary without visual clutter.
*   **Ambient Shadows:** If a floating element (like a modal) requires a shadow, use a large blur (40px) with the color `on_secondary_fixed_variant` at 10% opacity. This creates a warm, ambient glow rather than a cold, grey drop shadow.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline_variant` (#52443E) at 20% opacity. It should be barely perceptible—a "whisper" of a line.
*   **Sharp Edges:** All containers must maintain a `0px` border radius. The "Broadcast" aesthetic is built on precision and sharp, architectural lines. Curves are prohibited.

## 5. Components

### Buttons
*   **Primary:** Background: `primary_container`. Text: `on_primary_container`. Shape: Sharp (0px). Hover: Transition to `primary` with a slight "glow" effect (subtle outer stroke).
*   **Secondary:** Background: Transparent. Border: 1.5px `outline`. Text: `on_surface`.
*   **Tertiary:** Text: `primary`. No background. Used for low-emphasis actions within body copy.

### Cards & Content Blocks
*   **Layout:** Forbid the use of divider lines. Use the spacing scale `10` (3.5rem) or `12` (4rem) to separate content vertically.
*   **Image Treatments:** Use high-contrast photography. Apply a subtle gradient overlay from `transparent` to `surface_container_lowest` at the bottom of images to allow text to sit comfortably over photography.

### Input Fields
*   **Style:** Underline only. Use `outline_variant` for the default state and `primary` for the active/focus state. This mimics a "production checklist" aesthetic.
*   **Labels:** Always use `label-md` (Space Grotesk) in all-caps above the input.

### "The Buzzer" Indicator (Signature Component)
*   A custom chip using `primary_container` with a pulsing animation. Use `label-sm` text. This is used for "Live Now" or "Action Required" moments to reinforce the brand's energetic tone.

## 6. Do's and Don'ts

### Do
*   **Use Asymmetry:** Place a `display-lg` headline on the left and a small `body-md` block on the far right, leaving the center empty. Embrace the "Editorial" void.
*   **Use Oversized Spacing:** When in doubt, add more space. Use `spacing-24` (8.5rem) between major sections to let the design breathe.
*   **Stick to the Grid... then break it:** Align text to a strict 12-column grid, but allow images or accent terracotta shapes to bleed off the edge of the screen.

### Don't
*   **No Rounded Corners:** Never use border-radius. It softens the brand and loses the "Broadcast" edge.
*   **No Standard Greys:** Avoid pure greys (#808080). Always use the tinted neutrals (e.g., `outline` #9F8D86) to keep the warmth of the terracotta palette alive.
*   **No Centered Text for Long Copy:** Keep body text left-aligned to maintain the professional, structured editorial feel. Only center-align `display` headlines for massive impact.