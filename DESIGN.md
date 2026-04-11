# Design System: Antigravity & Floating Reality

## 1. Overview & Creative North Star
**Creative North Star: "The Celestial Ethereal"**

This design system is engineered to evoke the sensation of drifting through a weightless, cosmic void. We are moving away from the "grounded" nature of traditional web design—where elements sit on rigid grids and hard containers—toward a liquid, immersive experience. The goal is to make the user feel like they are navigating a high-end HUD (Heads-Up Display) suspended in a nebula.

To break the "template" look, we utilize **intentional asymmetry**. Hero elements should never be perfectly centered; instead, they should "float" slightly off-axis, overlapping with background atmospheric gradients. We rely on optical balance rather than mathematical centering to create a sense of organic motion.

---

## 2. Colors & Surface Philosophy

The palette is a deep-space spectrum designed to pull the eye into the screen, using light as the primary navigational tool.

### The "No-Line" Rule
Standard 1px borders are strictly prohibited for defining sections. In this system, boundaries are created through **Tonal Transitions**. A section shift is indicated by moving from `surface` (#0e0e14) to `surface-container-low` (#13131a). If a harder break is needed, use a wide, soft gradient fade rather than a line.

### Surface Hierarchy & Nesting
We treat the UI as a series of floating glass panes. 
- **Base Layer:** `surface` or `surface-container-lowest` (The Void).
- **Secondary Layer:** `surface-container` (The Atmospheric Layer).
- **Interactive Layer:** `surface-container-high` or `highest` (The Floating Pane).

### The Glass & Gradient Rule
To achieve "Floating Reality," all primary containers must utilize **Glassmorphism**.
- **Fill:** Use `surface-variant` at 40-60% opacity.
- **Blur:** Apply a minimum of `20px` to `40px` backdrop-blur.
- **Signature Glow:** Main CTAs should not be flat. Use a linear gradient from `primary` (#8ff5ff) to `primary-container` (#00eefc) to simulate a self-illuminating neon light source.

---

## 3. Typography: The Sci-Fi Editorial
We pair the technical precision of **Space Grotesk** with the human-centric clarity of **Manrope**.

- **Display & Headlines (Space Grotesk):** These are your "HUD" elements. Use `display-lg` (3.5rem) with tighter letter-spacing (-0.02em) to create an authoritative, futuristic look. Headlines should often be presented in `on-surface` or `primary` for high-impact statements.
- **Body & Titles (Manrope):** Manrope provides a grounded contrast to the sci-fi headers. Use `body-lg` (1rem) for readability.
- **Labels (Space Grotesk):** Small caps or wide tracking (+0.1em) should be applied to `label-md` to mimic technical readouts or coordinates.

---

## 4. Elevation & Depth

### The Layering Principle
Depth is achieved through **Tonal Layering**. Instead of using shadows to lift an object, use the `surface-container` tiers. A `surface-container-highest` card sitting on a `surface` background provides a sophisticated, "built-in" lift that feels like part of the environment rather than an after-thought.

### Ambient Shadows
When an element must truly "float" (e.g., a modal or a primary floating action button), use **Ambient Shadows**. 
- **Color:** Use a tinted version of `secondary` (#d575ff) or `primary` (#8ff5ff) at 5% opacity.
- **Properties:** Large blur (60px+), 0px offset. This creates a "glow" rather than a shadow, reinforcing the "weightless" theme.

### The "Ghost Border" Fallback
If a container requires a edge for accessibility, use the **Ghost Border**:
- **Stroke:** 1px.
- **Color:** `outline-variant` (#48474f) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Glass Cards (The Hero Component)
The fundamental building block.
- **Background:** `surface-container-low` at 50% opacity.
- **Blur:** Backdrop-blur 30px.
- **Edge:** A top-down linear gradient stroke (1px) using `primary` at 20% opacity fading to 0%.
- **Padding:** Always use `xl` (1.5rem) or greater to ensure the "breathable" feel.

### Floating Buttons
- **Primary:** Gradient fill (`primary` to `primary-dim`). No border. Roundedness: `full`.
- **Secondary:** Transparent fill with a `Ghost Border` and `on-surface` text.
- **Motion:** On hover, the button should "lift" (scale 1.05) and increase the intensity of its ambient glow.

### Kinetic Chips
- **Style:** Small, pill-shaped elements using `surface-container-highest`.
- **Interaction:** When selected, they should transition to `tertiary` (#ac89ff) with a subtle pulse animation.

### Inputs & Fields
- **Style:** Never use a solid box. Use a bottom-only border (Ghost Border style) that illuminates to 100% opacity `primary` when focused.
- **Text:** Input text should use `on-surface`, while helper text uses `on-surface-variant` in `label-sm`.

### Navigation (The Horizon Line)
Forgo the standard top-bar. Use a floating dock at the bottom of the viewport using the **Glassmorphism** rules, making it feel like a control panel in a cockpit.

---

## 6. Do’s and Don’ts

### Do:
- **Use White Space as a Structure:** Use the `xl` spacing scale to separate ideas. Let the background "breath" through the layout.
- **Embrace Overlaps:** Allow images or typography to partially overlap the edges of Glassmorphism cards to create a 3D parallax effect.
- **Limit Neon:** Use `primary` and `secondary` accents sparingly—like stars in the night sky. If everything glows, nothing glows.

### Don’t:
- **No Hard Dividers:** Never use a solid 100% opacity line to separate list items. Use a `16px` gap or a subtle shift in `surface-container` color.
- **No Pure Black Shadows:** This kills the "cosmic" depth. Shadows should always be tinted with the system’s purples or blues.
- **No Sharp Corners:** Avoid `none` or `sm` roundedness. Stick to `md` (0.75rem) and `lg` (1rem) to maintain the "dreamy" and "soft" aesthetic.