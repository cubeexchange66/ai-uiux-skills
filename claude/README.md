# Claude Integration Guide

Use UI/UX skills in Claude Projects for consistent, premium design.

---

## ⚡ 3-Minute Setup

### Method 1: Combined File (Fastest)

1. **Create New Project**
   - Go to [Claude.ai](https://claude.ai) → Projects → New Project
   - Name: "UI/UX Design Expert"

2. **Add Instructions**
   - Click "Project Instructions"
   - Copy ENTIRE content from [`combined-instructions.md`](combined-instructions.md)
   - Paste and Save

3. **Test It**
   ```
   You: "Design a dashboard for my SaaS product"
   Claude: *applies 8-point grid, 60-30-10 colors, Uncodixfy principles*
   ```

**Done!** ✅

---

### Method 2: Upload Files (More Flexible)

1. **Create New Project**
   - Claude.ai → Projects → New Project
   - Name: "UI/UX Expert"

2. **Upload Knowledge Files**
   - Click "Add content" → Upload files
   - Upload ALL files from [`project-files/`](project-files/) directory:
     - `uiux-design-skill.md`
     - `uncodixfy.md`
     - `ux-omni-protocol.md`

3. **Add Project Instructions**
   Paste this:
   ```markdown
   Apply UI/UX design skills automatically:
   - Use sophisticated color palettes (NO AI clichés)
   - Follow Uncodixfy for clean, functional UI
   - Apply UX-OMNI protocol for consistency
   - Verify with checklist before finalizing
   - Think: Linear, Raycast, Stripe - NOT generic AI dashboards
   ```

4. **Test It**
   Same as Method 1

---

## 📋 What's Included

Claude will automatically:

- ✅ Choose sophisticated colors (8 curated palettes)
- ✅ Use rare fonts (20+ unique typefaces)
- ✅ Apply 8-point grid system
- ✅ Enforce 60-30-10 color ratio
- ✅ Use ONE border radius (global uniformity)
- ✅ Create functional animations only
- ✅ Follow Uncodixfy (anti-generic) principles
- ✅ Ensure WCAG AA accessibility
- ✅ Write action-oriented copy

---

## 🎯 Example Conversations

### Designing Components

**You:**
```
Design a button component for a fintech app
```

**Claude:**
```tsx
// Slate & Burgundy palette (financial sophistication)
<motion.button
  whileHover={{ scale: 1.02 }}
  whileTap={{ scale: 0.96 }}
  style={{
    backgroundColor: '#5B6771',  // Deep Slate (NOT #3B82F6!)
    color: 'white',
    padding: '12px 24px',        // 8-point grid
    borderRadius: '10px',        // Unified radius
    fontWeight: 550,             // Variable weight
    fontFamily: 'Space Grotesk', // Rare font
  }}
>
  Setujui Transaksi →
</motion.button>

Accessibility:
- Contrast: 7.2:1 (WCAG AAA) ✅
- Focus ring: 2px solid #5B6771
- Touch target: 48x48px ✅
```

---

### Designing Pages

**You:**
```
Create a landing page for an eco-friendly product
```

**Claude:**
```markdown
# Landing Page Design

## Color Palette: Olive & Rust (Natural, Authentic)
- Primary: #6F7545 (Deep Olive)
- Secondary: #BF6B3F (Rust Orange)
- Background: #FBF9F7 (Warm White)
- Text: #2B2826

## Typography
- Headings: Plus Jakarta Sans (friendly, organic)
- Body: Plus Jakarta Sans
- Accent numbers: Azeret Mono

## Layout
[Provides full component structure with 8-point grid spacing]

## Components
[Button, Card, Hero implementations with code]

## Accessibility
- All text meets WCAG AA contrast
- Semantic HTML throughout
- Focus indicators visible
- Touch targets 44x44px minimum
```

---

### Building Design Systems

**You:**
```
Build a design system for my B2B SaaS product
```

**Claude:**
```markdown
# Design System: [Your Product Name]

## 1. Color Tokens (60-30-10 Ratio)
Primary: #3D5A6C (Ink Blue - 10% accents)
Surface: #F9FAFB (Canvas - 60% backgrounds)
Container: #FFFFFF (Cards - 30% surfaces)

## 2. Typography Scale (Variable Weights)
Heading: Space Grotesk (350, 450, 650, 850)
Body: Manrope (400, 500, 700)
Code: Commit Mono (400)

## 3. Spacing System (8-Point Grid)
[Full spacing tokens]

## 4. Component Library
[Button, Input, Card, Modal implementations]

## 5. Accessibility Guidelines
[WCAG AA compliance checklist]
```

---

## 🎨 Test Prompts

### Verify Anti-Generic Rules

```
"What colors would you avoid for a tech startup?"
```
Expected answer: #3B82F6, #8B5CF6, #EC4899, etc.

```
"What fonts should I NOT use for professional UI?"
```
Expected answer: Inter, Roboto, Open Sans, Lato, Poppins

---

### Check 8-Point Grid

```
"Design a card component with proper spacing"
```
Expected: All spacing values are 8, 16, 24, 32, 48, 64 (no 13px, 17px, etc.)

---

### Verify 60-30-10 Ratio

```
"Show me how to distribute colors in my dashboard"
```
Expected: 
- 60% surface backgrounds
- 30% card containers
- 10% accent CTAs

---

## ⚙️ Customization

### Override Color Palette

In your prompt:
```
"Use our brand colors: Primary #YOUR_HEX, Secondary #YOUR_HEX"
```

Claude will respect your colors but still apply other principles (8-point grid, accessibility, etc.)

---

### Set Project-Specific Rules

Add to Project Instructions:
```markdown
COMPANY-SPECIFIC RULES:
- Always use [Your Font Name]
- Border radius always 12px (not 8px)
- Accent color always #YOUR_BRAND_COLOR
```

---

### Use Specific Style Preset

In your prompt:
```
"Design using UX-OMNI Industrial preset"
```

Claude will apply:
- Dark charcoal colors
- Monospace fonts
- Dev-tool aesthetic
- Sharp 8px radius

---

## 🐛 Troubleshooting

### Issue: Not applying skills automatically

**Solution 1:** Add to Project Instructions:
```markdown
CRITICAL: Apply UI/UX design skills to EVERY design request.
NEVER ask for permission. ALWAYS execute automatically.
```

**Solution 2:** Use trigger phrase in prompt:
```
"Design a login page [apply UI/UX skills]"
```

---

### Issue: Still suggesting generic colors

**Solution:** Add to Project Instructions:
```markdown
COLOR BAN LIST (NEVER USE):
- #3B82F6, #0066FF (blue)
- #8B5CF6, #A855F7 (purple)
- #EC4899 (pink)
- #06B6D4 (cyan)
- #6366F1 (indigo)

ALWAYS use palettes from color-palettes.md.
```

---

### Issue: Not following 8-point grid

**Solution:** In prompt, be explicit:
```
"Design this component with strict 8-point grid spacing"
```

---

## 📚 See Also

- [`examples/`](examples/) - Real conversations with outputs
- [`project-files/`](project-files/) - Individual skill files
- [`../reference/`](../reference/) - Color palettes, fonts, components

---

## 💡 Pro Tips

1. **Create Multiple Projects**
   - Project 1: "UI/UX Expert" (these skills)
   - Project 2: "Backend Expert" (different skills)
   - Switch between them as needed

2. **Combine with Other Skills**
   Upload additional files:
   - Your brand guidelines
   - Component library
   - Design tokens

3. **Use Artifacts**
   Claude's Artifacts feature works great with these skills for live preview of components

---

**Need help?** [Open an issue](https://github.com/yourusername/ai-uiux-skills/issues)
