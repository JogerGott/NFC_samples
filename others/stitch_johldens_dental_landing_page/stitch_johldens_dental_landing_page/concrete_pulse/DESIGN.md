# Design System: High-End Editorial Urbanism

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Kinetic Brutalist."** 

Unlike generic e-commerce layouts that rely on soft edges and predictable grids, this system embraces the raw, high-contrast energy of urban fashion. We move beyond "minimalism" into "intentional subtraction." By utilizing the `0px` roundedness scale, we create a sharp, architectural aesthetic that feels engineered rather than merely designed. The experience breaks the template look through bold, asymmetric typography scales, overlapping structural elements, and a high-energy interplay between monolithic black surfaces and vibrant, kinetic orange accents.

## 2. Colors
This system is built on a high-contrast foundation where the tension between light and dark is punctuated by "Vibrant Orange."

### Palette Strategy
*   **Primary (`#ad2c00`) & Primary Container (`#d83900`):** These represent our "Vibrant Orange" core. Use these for high-action items and kinetic accents that demand immediate attention against the monochrome base.
*   **Surface Hierarchy:** We utilize `surface` (#f9f9f9) as our pristine gallery floor. `surface_container` levels (Lowest to Highest) are used to create structural depth without the need for primitive lines.
*   **The "No-Line" Rule:** Explicitly prohibit 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. For example, a product description card in `surface_container_lowest` (#ffffff) should sit on a `surface_container_low` (#f3f3f4) section to define its perimeter.

### Signature Textures
*   **The Glass Rule:** For floating navigation or quick-view modals, use `surface` colors with 80% opacity and a 20px backdrop-blur. This "frosted glass" look ensures the urban energy of the background photography bleeds through the UI.
*   **Kinetic Gradients:** Main CTAs should utilize a subtle linear gradient from `primary` (#ad2c00) to `primary_container` (#d83900) at a 135-degree angle. This adds a "weighted" premium feel that flat hex codes lack.

## 3. Typography
The typography is the voice of the brand: authoritative, loud, and meticulously clean.

*   **Display & Headlines (Epilogue):** This is our "Bold Sans-Serif." It should be used with tight letter-spacing (-2%) to mimic high-end fashion mastheads. `display-lg` (3.5rem) is reserved for hero statements that bleed off the edge of the grid.
*   **Title & Body (Manrope):** Chosen for its technical, clean execution. `body-lg` (1rem) provides the readability required for product specs, while `title-lg` (1.375rem) serves as the bridge between editorial headlines and functional content.
*   **Labels (Inter):** Used at `label-sm` (0.6875rem) in all-caps with increased letter-spacing (+5%) for "technical" metadata, like SKU numbers or material compositions.

## 4. Elevation & Depth
In this system, depth is a matter of **Tonal Layering**, not physical shadows.

*   **The Layering Principle:** Treat the UI as stacked sheets of heavy-weight paper. A `surface_container_highest` (#e2e2e2) element is physically "closer" to the user than a `surface` element. 
*   **Ambient Shadows:** Traditional drop shadows are forbidden. If a floating element (like a FAB or Cart Drawer) requires lift, use an ultra-diffused shadow: `box-shadow: 0 20px 40px rgba(26, 28, 28, 0.06)`. The tint must be derived from `on_surface` to feel like natural ambient light.
*   **The "Ghost Border" Fallback:** If accessibility requires a container boundary on similar tones, use the `outline_variant` token at 15% opacity. It should be felt, not seen.
*   **Architectural Overlap:** Encourage elements (like high-res product cutouts) to overlap container boundaries. This breaks the "boxed-in" feel of standard web design and creates a three-dimensional urban landscape.

## 5. Components
All components adhere to the **0px Roundedness** rule to maintain the "Urban Sleek" identity.

*   **Buttons:**
    *   **Primary:** `primary` background, `on_primary` text. Rectangular, no radius. Padding: `spacing-4` (1.4rem) horizontal.
    *   **Secondary:** `inverse_surface` background, `inverse_on_surface` text. For high-contrast secondary actions.
*   **Input Fields:** Use `surface_container_high` with a bottom-only "Ghost Border" (2px). Label text should use `label-md` in `on_surface_variant`.
*   **Cards:** No borders. Separate cards using `spacing-6` (2rem) and background tonal shifts (e.g., `surface_container_lowest` card on `surface` background).
*   **Accordion (FAQ):** Referencing the visual context of a modern FAQ, use `surface_container` tiers for the header and `surface` for the expanded body. Use `spacing-3` for internal padding to maintain a compact, sleek profile.
*   **Image Carousels:** Use raw edges. Navigation arrows should be "floating" glassmorphic circles or sharp squares using `surface_bright` at 90% opacity.

## 6. Do's and Don'ts

### Do:
*   **Use Asymmetric Grids:** Place a `display-lg` headline on the far left and the corresponding `body-md` description on the far right of the grid to create "tension."
*   **Embrace White Space:** Use `spacing-16` (5.5rem) and `spacing-24` (8.5rem) to separate major editorial sections.
*   **Color as Signal:** Reserve the "Vibrant Orange" (`primary`) only for the most critical conversion points or brand moments.

### Don't:
*   **No Rounded Corners:** Never use a border-radius. Every element must be sharp-edged (`0px`).
*   **No Dividers:** Never use a `1px` line to separate list items. Use a shift from `surface` to `surface_container_low` or vertical padding from the spacing scale.
*   **No Grey Shadows:** Never use a default `#000000` shadow. Always use a low-opacity tint of the `on_surface` color for ambient depth.
*   **No Center-Alignment for Long Copy:** Keep body text left-aligned to maintain the "Technical/Urban" look. Center-alignment is only for high-level display headlines.