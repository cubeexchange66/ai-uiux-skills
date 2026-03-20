---
name: uiux-design-skill
description: Automated design decision-making for AI agents. Implements 8-point grid, 60-30-10 color harmony, global radius uniformity, and action-oriented UX. Generates premium market-ready UI without manual design input.
---

# UX Omni-Protocol (Global Standard)

**Version:** 2.0 (Deep Learning Optimized)
**Context:** Universal / Global (Applicable to SaaS, E-commerce, Dashboards, Mobile, Web)

This skill is a **Decision Engine** for UI/UX. It replaces "guessing" with **researched standards** derived from cognitive psychology, optical physics, and conversion rate optimization (CRO).

## 🧠 The "Deep Research" Core

Do not generate "creative" UI. Generate **scientifically optimized** UI based on these 5 pillars:

### 1. Kinetic Physics (The "Feel")
User trust increases when digital objects behave like physical ones.
*   **The Spring Rule:** All animations must use **Spring Physics**, not Linear/Ease-In-Out.
    *   *Config:* Mass: 1, Tension: 170, Friction: 26 (The "Apple" feel).
    *   *Why:* Real objects don't start/stop instantly; they carry momentum.
*   **Tactile Response:**
    *   **Buttons:** `active:scale-[0.96]` (Simulates material compression).
    *   **Cards:** `hover:translate-y-[-2px]` (Simulates magnetic lift).
    *   **Inputs:** `focus:ring-2` + `transition-all` (Simulates energy focus).

### 2. Cognitive Color (The "Look")
Colors must guide attention, not just decorate.
*   **The 60-30-10 Rule (Strict):**
    *   **60% Neutral:** Backgrounds, Surfaces (White, Off-White, Soft Gray).
    *   **30% Secondary:** Borders, Dividers, Subtext (Cool Gray, Slate).
    *   **10% Accent:** **ONLY** for Primary Actions (Submit, Buy, Login).
    *   *Why:* Reduces cognitive load. Users instantly know where to click.
*   **The "Vantablack" Ban:**
    *   ⛔ **NEVER** use `#000000` (Pure Black). It causes eye strain (smearing on OLED).
    *   ✅ **USE** `#111827` (Gray-900) or `#0F172A` (Slate-900).

### 3. Typographic Rhythm (The "Voice")
Typography determines readability and authority.
*   **The Golden Ratio Type Scale (1.618):**
    *   Base: 16px (1rem).
    *   h3: 26px (~1.618rem).
    *   h2: 42px (~2.618rem).
    *   h1: 68px (~4.236rem).
*   **Optical Alignment:**
    *   Headings must have `tracking-tight` (-0.02em) to feel solid.
    *   Captions/Uppercase must have `tracking-wide` (+0.05em) to breathe.
    *   Line-height (Leading) must reduce as font size increases.

### 4. Spatial Geometry (The "Flow")
Spacing is the most important indicator of design quality.
*   **The 4pt Hard Grid:**
    *   All dimensions (margin, padding, height) **MUST** be divisible by 4.
    *   Common stops: 4, 8, 12, 16, 24, 32, 48, 64, 96.
    *   ⛔ **BANNED:** 13px, 21px, 5px.
*   **Proximity Law:**
    *   Space *within* a component < Space *between* components.
    *   Label-to-Input: 8px. Input-to-Input: 16px. Section-to-Section: 48px+.

### 5. Human Microcopy (The "Soul")
Robotic text kills immersion.
*   **The "Benefit-First" Rule:**
    *   ⛔ "Settings Updated."
    *   ✅ "Changes saved successfully." (Focus on outcome)
    *   ⛔ "Wrong Password."
    *   ✅ "That password doesn't look right." (Polite correction)

---

## 🛠️ Implementation Specs (Tailwind/CSS)

### Global Reset (The "Premium" Base)
Apply these classes to the root `body` or main wrapper to instantly upgrade any app.
```tsx
className="antialiased text-gray-900 bg-gray-50 selection:bg-indigo-500/30 selection:text-indigo-900"
```

### The "God-Tier" Button
Universal primary button that works in any context.
```tsx
<button className="
  group relative inline-flex items-center justify-center
  px-6 py-2.5 
  font-medium text-white transition-all duration-200 
  bg-gray-900 rounded-lg 
  hover:bg-gray-800 hover:shadow-lg hover:-translate-y-0.5
  active:scale-95 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-900
">
  <span>Start Free Trial</span>
  {/* Shine Effect */}
  <div className="absolute inset-0 -z-10 bg-gradient-to-r from-transparent via-white/10 to-transparent opacity-0 group-hover:animate-shine" />
</button>
```

### The "Glass" Card (Modern Standard)
Clean, depth-aware surface for content.
```tsx
<div className="
  relative overflow-hidden
  bg-white/80 backdrop-blur-xl
  border border-gray-200/50 rounded-2xl
  shadow-[0_8px_30px_rgb(0,0,0,0.04)]
  transition-all duration-300
  hover:shadow-[0_8px_30px_rgb(0,0,0,0.08)]
">
  {children}
</div>
```

### Input Field (Focus Physics)
```tsx
<input className="
  w-full px-4 py-3
  bg-gray-50 border-gray-200 rounded-xl
  text-gray-900 placeholder:text-gray-400
  transition-all duration-200
  focus:bg-white focus:border-indigo-500 focus:ring-4 focus:ring-indigo-500/10
  hover:bg-gray-100
"/>
```

---

## 🚫 The "Seven Deadly Sins" of UI (BANNED)

1.  **Hamburger Menus on Desktop:** Always show navigation if space permits.
2.  **Carousels:** Users don't click them. Use Grids.
3.  **Scrolljacking:** Never alter the browser's native scroll physics.
4.  **"Click Here":** Use descriptive links ("View Dashboard").
5.  **Low Contrast:** Text must pass WCAG AA (4.5:1). No gray-on-gray.
6.  **Destructive Defaults:** "Delete" buttons should never be the primary focus.
7.  **Modals over Modals:** Never stack popups. Use a slide-over or new page.

## 📥 When to Invoke
Use this protocol for **ANY** UI task:
- "Design a landing page"
- "Fix this form"
- "Make it look better"
- "Create a dashboard"

**Output Requirement:**
Always provide the **React/Tailwind code** that strictly adheres to these physics and spacing rules. Do not ask "what style?". **YOU** dictate the standard.

