# ChatGPT Integration Guide

Quick setup for using UI/UX skills in ChatGPT.

---

## ⚡ 2-Minute Setup

1. **Open ChatGPT Settings**
   - Go to [ChatGPT](https://chat.openai.com)
   - Click your profile icon → Settings
   - Select "Custom Instructions"

2. **Paste Instructions**
   - Open [`custom-instructions.md`](custom-instructions.md)
   - Copy ENTIRE content
   - Paste into: **"How would you like ChatGPT to respond?"**
   - Click "Save"

3. **Test It**
   ```
   You: "Create a login page with unique design"
   ChatGPT: *generates sophisticated UI with rare fonts and muted colors*
   ```

**Done!** ✅

---

## 📋 What's Included

When you add these custom instructions, ChatGPT will:

- ✅ Use sophisticated color palettes (NO AI clichés like #3B82F6)
- ✅ Choose rare fonts (NOT Inter/Roboto)
- ✅ Apply 8-point grid spacing automatically
- ✅ Follow Uncodixfy principles (clean, functional UI)
- ✅ Create accessible designs (WCAG AA)
- ✅ Use functional animations only
- ✅ Verify with 10-point checklist

---

## 🎯 Example Prompts

### Basic Usage
```
You: "Design a button component"

ChatGPT will:
- Choose sophisticated color (e.g., #E0624B Terracotta)
- Use 8-point grid padding (12px 24px)
- Apply unified radius (10px)
- Include hover/active states
- Ensure WCAG AA contrast
```

### Page Design
```
You: "Create a landing page for a fintech startup"

ChatGPT will:
- Choose "Slate & Burgundy" or "Ink Blue & Bronze" palette
- Use rare font like "Satoshi" or "Space Grotesk"
- Apply responsive design (mobile-first)
- Include action-oriented copy ("Mulai Gratis" not "Submit")
- Verify accessibility
```

### Component System
```
You: "Build a complete design system for my SaaS product"

ChatGPT will:
- Define color tokens (60-30-10 ratio)
- Choose rare typography scale
- Create reusable components
- Document spacing system (8-point grid)
- Include accessibility guidelines
```

---

## 🎨 Try These Prompts

### Test 1: Color Verification
```
"What color palette would you use for a wellness app?"
```
Expected: Olive & Rust or Terracotta & Sage  
Should NOT suggest: Blue #3B82F6 or Purple #8B5CF6

### Test 2: Font Selection
```
"What fonts should I use for a creative agency website?"
```
Expected: Clash Display + Satoshi or Cabinet Grotesk  
Should NOT suggest: Inter, Roboto, or Open Sans

### Test 3: Complete Page
```
"Design a pricing page for a B2B SaaS product"
```
Expected:
- Sophisticated colors (NOT Tailwind defaults)
- Rare fonts
- 8-point grid
- Clean components (Uncodixfy compliant)
- Mobile responsive

---

## ⚙️ Customization

### Add Your Brand Colors
Append to custom instructions:
```markdown
IMPORTANT: Always use these brand colors:
- Primary: #YOUR_HEX
- Secondary: #YOUR_HEX
- Accent: #YOUR_HEX
```

### Set Default Font
Append to custom instructions:
```markdown
IMPORTANT: Always use [Your Font Name] for headings and body text.
```

### Override Specific Rules
In your prompt:
```
"Design a dashboard but use glassmorphism (override Uncodixfy for this case)"
```

---

## 🐛 Troubleshooting

### Issue: Still getting generic AI colors
**Solution:**
1. Delete old custom instructions completely
2. Paste fresh from `custom-instructions.md`
3. Start a NEW chat (old chats cache behavior)

### Issue: Not following 8-point grid
**Solution:**
Explicitly mention in prompt: "Use 8-point grid spacing (8px, 16px, 24px...)"

### Issue: Using Inter font by default
**Solution:**
Add to instructions: "NEVER use Inter, Roboto, or common fonts. Always use rare fonts."

---

## 📚 See Also

- [`examples/`](examples/) - Real prompts with outputs
- [`../docs/installation.md`](../docs/installation.md) - Detailed setup
- [`../reference/color-palettes.md`](../reference/color-palettes.md) - All 8 palettes

---

**Need help?** [Open an issue](https://github.com/yourusername/ai-uiux-skills/issues)
