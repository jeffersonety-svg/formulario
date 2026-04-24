# Design System Strategy: Precision Industrialism

This design system is engineered for the high-stakes environment of fleet management, where clarity, velocity, and reliability are paramount. Moving away from the generic "SaaS-blue" template, this system adopts an **Industrial Editorial** aesthetic. It combines the utilitarian precision of heavy machinery with the sophisticated layering of high-end digital interfaces.

## 1. Creative North Star: "The Kinetic Engine"
The design system is built on the concept of **Kinetic Engine**—a visual language that feels active, powered, and meticulously organized. We break the traditional "box-in-a-box" layout by using intentional asymmetry and tonal depth. By utilizing high-contrast typography and a signature crimson velocity gradient, we guide the user’s eye to critical telemetry data without overwhelming the senses.

---

## 2. Color Architecture & The Tonal Rulebook
The palette transitions from cold, industrial tech-blues to high-energy, aggressive reds.

### The "No-Line" Rule
To maintain a premium, modern feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through:
1.  **Tonal Shifts:** Placing a `surface-container-low` (#e6f6ff) section against a `surface` (#f3faff) background.
2.  **Vertical Space:** Utilizing the spacing scale to create distinct content groups.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Fleet management requires complex data density; layering prevents visual "clutter":
*   **Base Level:** `surface` (#f3faff) – The canvas.
*   **Secondary Grouping:** `surface-container-low` (#e6f6ff) – Used for large grouped sections.
*   **Active Elements:** `surface-container-highest` (#cfe6f2) – Used for cards or items currently in focus.

### The Signature Gradient
For primary actions and critical "Active" states, use the **Velocity Gradient**:
*   **Start:** `primary` (#b7131a)
*   **End:** `on_secondary_fixed_variant` (#8e120a)
*   **Angle:** 135 degrees.
*   **Application:** Primary CTAs, active progress bars, and high-priority status indicators.

---

## 3. Typography: The Technical Serif
We utilize **Inter** not just for legibility, but as a technical instrument.

*   **Display (lg/md):** Reserved for high-level fleet metrics (e.g., "Total Active Units"). Use `on_surface` (#071e27) with a slight tracking reduction (-0.02em).
*   **Headline (sm):** Used for section headers within complex forms.
*   **Body (md/lg):** The workhorse for data entries and fleet logs. Ensure a line height of 1.5 for maximum scanability.
*   **Label (sm):** Used for technical metadata (VIN numbers, GPS coordinates). These should often be set in `on_surface_variant` (#5b403d) to create a clear hierarchy against the data values.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "web 2.0" for this system. We use **Ambient Depth**.

*   **The Layering Principle:** Place a `surface-container-lowest` (#ffffff) card on a `surface-container-low` (#e6f6ff) background. The subtle shift in hex value creates a "lift" that feels integrated into the hardware.
*   **Ghost Borders:** If a separator is required for accessibility in complex forms, use `outline-variant` (#e4beb9) at **15% opacity**. It should be felt, not seen.
*   **Glassmorphism:** For floating overlays (like map tooltips or vehicle quick-views), use `surface_container_lowest` at 80% opacity with a `20px` backdrop-blur. This keeps the fleet map visible behind the data.

---

## 5. Components: Industrial Precision

### Primary Buttons
*   **Visual:** Apply the Velocity Gradient. 
*   **Radius:** `md` (0.375rem) for a grounded, industrial feel. 
*   **State:** On hover, shift the gradient towards `primary_container` (#db322f).

### Complex Form Groups
*   **Structure:** Do not use fieldsets with borders. Use a `surface-container-low` background block with a `title-lg` header.
*   **Conditional Logic Visibility:** When a field is revealed via logic, use a "slide-and-fade" transition. Use a 2px vertical accent bar of `primary` (#b7131a) to the left of the newly appeared field to signal that it requires attention.

### Chips & Status Indicators
*   **Active Vehicle:** `tertiary_container` (#008097) with `on_tertiary_container` (#f9fdff).
*   **In Maintenance:** `secondary_container` (#fd644f) with `on_secondary_container` (#650000).
*   **Shape:** `full` (9999px) to contrast against the sharp, rectangular nature of the forms.

### Input Fields
*   **Background:** `surface_container_lowest` (#ffffff).
*   **Border:** None. Use a bottom-only "active bar" that expands from the center using `surface_tint` (#bb171c) when focused.
*   **Error State:** Background shifts to `error_container` (#ffdad6).

---

## 6. Do’s and Don’ts

### Do
*   **Do** use `surface-dim` (#c7dde9) for disabled states to maintain the industrial "cold" aesthetic.
*   **Do** use asymmetrical spacing. Give more room to the top of a section than the bottom to create an editorial "downward" flow.
*   **Do** use `display-sm` for numbers and `label-md` for units (e.g., **450** *km/h*).

### Don’t
*   **Don't** use 100% black text. Always use `on_surface` (#071e27) to maintain tonal harmony.
*   **Don't** use "Card Shadows." If a card needs to pop, increase its surface tier (e.g., from `low` to `highest`).
*   **Don't** use standard blue for links. Use `tertiary` (#006578) for a sophisticated, professional alternative.