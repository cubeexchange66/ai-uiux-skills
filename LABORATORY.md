# Laboratory Protocol (The R&D Department)

This document defines the workflow for **Experimental Design Generation**. Unlike the standard `uiux-design-skill.md` which produces "Safe" results, this Lab produces "First-Mover" innovations.

## 🧪 The Experiment Process

When the user asks to "experiment", "innovate", or "lab" a component, follow this exact 3-step process.

### Step 1: Generate 3 Variants

You must always generate THREE distinct versions of the requested component:

#### **Variant A: The Standard (Control Group)**
*   **Source:** `uiux-design-skill.md`
*   **Philosophy:** Clean, production-ready, safe.
*   **Style:** Linear/Stripe/Raycast standard.
*   **Use Case:** When reliability is key.

#### **Variant B: The Evolution (Iterative Improvement)**
*   **Source:** `MUTATION_PROTOCOL.md` (Roll 1-15)
*   **Philosophy:** "Standard + 10% Magic".
*   **Mutation:** Tweak **one** major variable (e.g., Typography OR Physics).
*   **Style:** Fresh, modern, polished.
*   **Use Case:** To look "newer" than competitors.

#### **Variant C: The Mutation (First-Mover)**
*   **Source:** `MUTATION_PROTOCOL.md` (Roll 16-20 + Custom)
*   **Philosophy:** "What if we break the rules?".
*   **Mutation:** Combine opposing concepts (e.g., Brutalism + Glassmorphism).
*   **Style:** Unique, unexpected, trend-setting.
*   **Use Case:** For "Wow" moments or hero sections.

---

### Step 2: The "Uncodixfy" Filter

Run all 3 variants through the `uncodixfy.md` checklist.
*   *Does Variant C look like a generic AI dashboard?* -> **REJECT & REGENERATE.**
*   *Does Variant B use neon blue gradients?* -> **REJECT & REGENERATE.**

**CRITICAL:** Even experimental designs must not look "Cheap AI". They must look "Intentional Human Design".

---

### Step 3: Cataloging (The Library)

If the user approves a variant, you must:
1.  Extract the code (React/Tailwind).
2.  Clean it up (Remove comments, optimize imports).
3.  Save it to the `library/` folder with a descriptive name.
    *   `library/experimental/magnetic-button-v1.tsx`
    *   `library/standard/card-dashboard-v2.tsx`

---

## 🔬 Example Prompt

**User:** "Agent, lab button."

**Agent Output:**
1.  **Variant A:** Standard 8px radius, solid color, slight hover lift.
2.  **Variant B:** "Elastic" button. 12px radius. Scale 0.9 on click (spring physics). Font-weight 550.
3.  **Variant C:** "Ghost-Glass". 0px radius (sharp). Blur 20px background. 1px gradient border that rotates on hover.

---

## ⚠️ Warning

**Do not hallucinate physics.** Use real CSS variables or Framer Motion values defined in `uiux-design-skill.md` or `MUTATION_PROTOCOL.md`.
