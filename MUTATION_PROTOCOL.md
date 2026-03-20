# Mutation Protocol (The Genetic Code of Design)

This document defines the **safe ranges** and **variables** the AI agent is allowed to mutate when running in Laboratory Mode. It ensures that experiments remain functional, accessible, and performant, even when pushing boundaries.

## 🧬 Primary Mutation Variables

When asked to "mutate" or "evolve" a design, the agent may tweak the following parameters within the specified ranges.

### 1. Typography (The Voice)
*   **Variable Weights:** Instead of standard 400/500/700, use specific values.
    *   *Range:* 350 - 850 (Step: 10)
    *   *Example:* `font-weight: 420` (Custom CSS required)
*   **Line Height (Leading):**
    *   *Headings:* 0.95 - 1.2 (Tighter is trendier)
    *   *Body:* 1.4 - 1.8 (Readability first)
*   **Letter Spacing (Tracking):**
    *   *Caps:* +0.05em to +0.2em
    *   *Headings:* -0.01em to -0.04em (Tight packing)

### 2. Physics & Motion (The Feel)
*   **Spring Tension (Stiffness):** How fast it snaps.
    *   *Range:* 120 - 300 (Standard: 170)
*   **Spring Friction (Damping):** How much it wobbles.
    *   *Range:* 10 - 40 (Standard: 26)
*   **Micro-Interactions:**
    *   *Scale:* 0.95 - 0.99 (Click) / 1.01 - 1.05 (Hover)
    *   *Rotation:* -2deg to +2deg (Subtle playfulness)
    *   *Lift:* -1px to -8px (Hover elevation)

### 3. Geometry (The Shape)
*   **Border Radius:**
    *   *Range:* 0px (Brutalist) to 999px (Pill)
    *   *Squircle:* Use `clip-path` for super-ellipse shapes (Apple-like).
*   **Stroke Width:**
    *   *Range:* 0.5px to 4px
    *   *Opacity:* 10% to 100%

### 4. Color & Depth (The Atmosphere)
*   **Surface Translucency:**
    *   *Range:* 40% - 95% (Backdrop Blur: 4px - 40px)
*   **Shadows:**
    *   *Color:* Never pure black. Use primary-colored shadows at 5-15% opacity.
    *   *Offset:* Y: 2px - 32px.

---

## 🛡️ Safety Constraints (The Firewall)

No mutation is allowed to violate these rules. If a generated design fails these checks, **discard it immediately**.

1.  **WCAG AA Compliance:** Contrast ratio must be ≥ 4.5:1 for text.
2.  **Touch Target Size:** Interactive elements must be ≥ 44x44px (including padding).
3.  **No "Seizure" Animations:** No flashing/strobing > 3Hz.
4.  **Performance:** No layout thrashing (animate `transform` & `opacity` only).
5.  **No "Generic AI" Artifacts:** (See `uncodixfy.md`).

---

## 🎲 Mutation Roll Table (D20)

When experimenting, roll a D20 to determine the "X-Factor":

| Roll | Mutation Type | Description |
|------|---------------|-------------|
| 1-5 | **Minimalist** | Reduce elements. Remove borders. Use whitespace. |
| 6-10 | **Tactile** | Increase depth. Add inner shadows. Make it "pressable". |
| 11-15 | **Typographic** | Make text HUGE. Use aggressive tracking. |
| 16-19 | **Glass/Fluid** | High blur. Gradient borders. Mesh gradients. |
| 20 | **Experimental** | Asymmetric grid. Broken layout. Brutalist. |
