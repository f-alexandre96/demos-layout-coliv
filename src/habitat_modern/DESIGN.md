# Design System Specification: The Curated Sanctuary

## 1. Overview & Creative North Star
To design for co-living is to design for the intersection of private sanctuary and collective energy. This design system moves away from the rigid, "boxed-in" feel of traditional real-estate apps, adopting a Creative North Star we call **"The Curated Sanctuary."**

The aesthetic is **High-End Editorial**: it treats screen real estate like a premium lifestyle magazine. We break the "template" look through intentional asymmetry, generous white space (breathing room), and high-contrast typography. The goal is to make the user feel they are not just browsing a list of rooms, but entering a professionally managed community.

---

## 2. Color Language & Tonal Depth
The palette utilizes deep Navy for authority, Mint for freshness, and a sophisticated Gray scale for structural depth.

### The "No-Line" Rule
Explicitly prohibited: 1px solid borders to define sections. Boundaries must be defined solely through background color shifts or subtle tonal transitions. For example, a card (`surface-container-lowest`) should sit on a (`surface-container-low`) background to define its shape.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine paper.
*   **Base:** `surface` (#f7f9fb)
*   **Secondary Content Areas:** `surface-container-low` (#f2f4f6)
*   **Elevated Components (Cards):** `surface-container-lowest` (#ffffff)
*   **Interactive Overlays:** `surface-container-high` (#e6e8ea)

### The Glass & Gradient Rule
To achieve a signature feel, use **Glassmorphism** for floating elements (like Bottom Navigation or Header blurs). Use a 20-40px backdrop-blur with a semi-transparent `surface` color. 
*   **Signature Textures:** For primary CTAs, use a subtle linear gradient from `primary` (#031636) to `primary_container` (#1a2b4c) at a 135-degree angle to add "visual soul."

---

## 3. Typography: The Editorial Voice
We use two distinct typefaces to balance modern authority with approachable community vibes.

*   **Display & Headlines:** `Plus Jakarta Sans`. This is our "Editorial" voice. Use `display-lg` for hero welcome messages with tight letter-spacing (-0.02em) to create a high-fashion, premium impact.
*   **Body & UI Labels:** `Manrope`. Chosen for its humanist qualities and exceptional legibility at small sizes. 
*   **The Hierarchy:** Use dramatic scale shifts. A `display-md` headline paired with a `body-md` description creates an intentional "Design-Led" look that feels more expensive than standard "balanced" layouts.

---

## 4. Elevation & Depth: Atmospheric Layering
We convey hierarchy through **Tonal Layering** rather than traditional structural lines or heavy shadows.

*   **The Layering Principle:** Depth is achieved by "stacking." A host's profile card should be `surface-container-lowest` placed on a `surface-container` background. This creates a soft, natural lift.
*   **Ambient Shadows:** When a floating effect is required (e.g., a "Book Now" FAB), use extra-diffused shadows:
    *   *Blur:* 24px to 40px.
    *   *Opacity:* 4% to 8%.
    *   *Color:* Tint the shadow with `on-surface` (#191c1e) rather than pure black to mimic natural light.
*   **The Ghost Border Fallback:** If a border is required for accessibility, use the "Ghost Border": `outline-variant` (#c5c6cf) at **15% opacity**. Never use 100% opaque borders.

---

## 5. Signature Components

### Buttons: The Tactile Interaction
*   **Primary:** Gradient of `primary` to `primary_container`. Border radius: `md` (0.75rem). Text: `label-md` in all-caps with 0.05em tracking for a "boutique" feel.
*   **Secondary (Community Action):** `secondary_container` (#79f7ea) background with `on_secondary_container` (#007169) text. This mint-on-mint look is modern and fresh.

### Cards: The Content Vessel
*   **Rule:** Forbid divider lines.
*   **Style:** Use `xl` (1.5rem) rounding for image containers and `md` (0.75rem) for the outer card. Overlap the property price tag (using `primary`) slightly over the image edge to break the grid.

### Input Fields: The Soft Entry
*   **Style:** Instead of a white box with a border, use a `surface-variant` background with a `none` border. On focus, transition the background to `surface-container-lowest` and add a 1px "Ghost Border" of `primary`.

### Co-Living Specific Components
*   **Trust Badges:** Use `secondary_fixed` (#79f7ea) with `on_secondary_fixed` text for "Verified Host" tags.
*   **Amenity Chips:** Use `surface-container-high` with `on_surface_variant`. Shapes should be `full` (pill-shaped) for a friendly, modern touch.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts (e.g., left-aligned headlines with right-aligned imagery).
*   **Do** use "Breathing Room." If you think there is enough margin, add 8px more.
*   **Do** use `secondary` (Mint) to highlight community-driven features (e.g., "Join Dinner," "Chat with Roommates").

### Don't
*   **Don't** use 1px solid dividers to separate list items. Use 16px of vertical whitespace or a subtle background shift.
*   **Don't** use pure black (#000000) for text. Always use `on_surface` (#191c1e) to maintain the high-end tonal softness.
*   **Don't** use sharp corners. The minimum radius should be `sm` (0.25rem), but the preference is `md` (0.75rem) to ensure the system feels "friendly" and "approachable."

---

## 7. Interaction & Motion
Motion should feel "weighted" and "organic." 
*   **Transitions:** Use a "Shared Axis" transition for navigating between room details. 
*   **Feedback:** When a user clicks a "Like" or "Save" button, use a soft scale-up (1.05x) rather than a simple color change to provide a premium, tactile response.