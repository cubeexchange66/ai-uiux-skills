# 🎨 AI UI/UX Skills - Anti-Generic Design System

> Transform your AI agent into a UI/UX expert that creates **unique, memorable designs** instead of generic AI-generated interfaces.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![AI Agent Ready](https://img.shields.io/badge/AI%20Agent-Ready-brightgreen.svg)]()
[![ChatGPT Compatible](https://img.shields.io/badge/ChatGPT-Compatible-orange.svg)]()
[![Claude Compatible](https://img.shields.io/badge/Claude-Compatible-purple.svg)]()

## 🚀 Quick Start

### For ChatGPT

1. **Copy Custom Instructions:**
   - Go to ChatGPT Settings → Custom Instructions
   - Copy content from [`chatgpt/custom-instructions.md`](chatgpt/custom-instructions.md)
   - Paste into "How would you like ChatGPT to respond?"
   - Save

2. **Start Creating:**
   ```
   You: "Create a landing page for my fintech startup"
   ChatGPT: *generates unique UI with sophisticated colors, rare fonts, and distinctive style*
   ```

### For Claude (Projects)

1. **Create a New Project:**
   - Open Claude.ai → Projects → New Project
   - Name it: "UI/UX Design Expert"

2. **Add Project Knowledge:**
   - Upload all files from [`claude/project-files/`](claude/project-files/)
   - Or copy-paste content from [`claude/combined-instructions.md`](claude/combined-instructions.md)

3. **Start Creating:**
   ```
   You: "Design a dashboard for my SaaS product"
   Claude: *applies 8-point grid, 60-30-10 color ratio, action-oriented UX*
   ```

### For API-Based Agents (LangChain, AutoGPT, etc.)

```python
from langchain import OpenAI, PromptTemplate

# Load skill instructions
with open("api/system-prompt.txt", "r") as f:
    system_prompt = f.read()

llm = OpenAI(
    model="gpt-4",
    system=system_prompt  # Inject UI/UX skills
)

response = llm.invoke("Create a login page with unique design")
```

See full examples in [`api/`](api/) directory.

---

## 📦 What's Included?

This repository contains **3 powerful UI/UX skills** that work together:

### 1. 🎨 **UI/UX Design Skill**
Creates UNIQUE, memorable designs that don't look AI-generated.

**Features:**
- ✅ Sophisticated color palettes (NO AI clichés like #3B82F6 blue)
- ✅ Rare font collections (20+ fonts that aren't Inter/Roboto)
- ✅ Functional animations (purpose-driven, not decorative)
- ✅ Component library with personality
- ✅ Modern 2026 tech stack (Radix UI, Framer Motion, shadcn/ui)
- ✅ Mobile-first responsive design
- ✅ WCAG AA accessibility compliance

**Best For:**
- Landing pages
- Dashboards
- Forms & data displays
- Design systems
- Marketing sites

### 2. 🚫 **Uncodixfy**
Prevents generic AI/Codex UI patterns in your code.

**What It Blocks:**
- ❌ Oversized rounded corners everywhere
- ❌ Floating glassmorphism shells
- ❌ Generic dark SaaS UI composition
- ❌ Hero sections inside dashboards
- ❌ Decorative copy and fake charts
- ❌ Transform animations on hover

**What It Enforces:**
- ✅ Normal, functional components (like Linear, Raycast, Stripe)
- ✅ Simple borders and subtle shadows
- ✅ Clear hierarchy without decoration
- ✅ Professional aesthetics without trying too hard

**Best For:**
- Dashboards & internal tools
- SaaS products
- Developer tools
- Enterprise applications

### 3. ⚡ **UX-OMNI Protocol**
Automated design decision-making for consistent, premium UI.

**Auto-Applied Rules:**
- 🎯 8-Point Grid System (8px, 16px, 24px, 32px...)
- 🎨 60-30-10 Color Harmony (Surface 60%, Secondary 30%, Accent 10%)
- 🔘 Global Radius Uniformity (ONE value for all components)
- 📝 Action-Oriented Copywriting (Verbs > Generic labels)
- ✨ Interactive States (Hover/Active/Focus required)

**Best For:**
- Design consistency across projects
- Fast prototyping
- Design system foundation
- Premium market-ready UI

---

## 🎯 Why Use These Skills?

### ❌ Without These Skills

Your AI generates:
```css
/* Generic AI UI */
--primary: #3B82F6;      /* Obvious Tailwind blue */
--font: 'Inter';         /* Everyone uses this */
--radius: 8px;           /* Everywhere */
--shadow: 0 10px 30px;   /* Too dramatic */
```

Result: **Looks like every other AI-generated UI**

### ✅ With These Skills

Your AI generates:
```css
/* Unique, Human-Curated UI */
--primary: #6B4964;      /* Deep Plum (distinctive) */
--secondary: #D4A243;    /* Golden Mustard (warm) */
--font: 'Satoshi';       /* Rare, memorable font */
--radius: 12px;          /* Unified across all */
--shadow: 0 2px 8px;     /* Subtle, professional */
```

Result: **Unique, memorable, looks professionally designed**

---

## 📂 Repository Structure

```
ai-uiux-skills/
├── README.md                          # You are here
├── LICENSE                            # MIT License
│
├── chatgpt/                           # ChatGPT Integration
│   ├── custom-instructions.md         # Copy to ChatGPT settings
│   ├── examples/                      # Example prompts
│   └── README.md                      # Setup guide
│
├── claude/                            # Claude Integration
│   ├── project-files/                 # Upload to Claude Project
│   │   ├── uiux-design-skill.md
│   │   ├── uncodixfy.md
│   │   └── ux-omni-protocol.md
│   ├── combined-instructions.md       # Single-file version
│   ├── examples/                      # Example prompts
│   └── README.md                      # Setup guide
│
├── api/                               # API-Based Agents
│   ├── system-prompt.txt              # Combined system prompt
│   ├── langchain-example.py           # LangChain integration
│   ├── openai-example.js              # OpenAI API example
│   ├── autogpt-config.yaml            # AutoGPT configuration
│   └── README.md                      # Integration guides
│
├── reference/                         # Reference Materials
│   ├── color-palettes.md              # 8 sophisticated palettes
│   ├── rare-fonts.md                  # 20+ unique fonts
│   ├── component-library.md           # Reusable patterns
│   ├── anti-generic-checklist.md      # Verification list
│   └── modern-stack-2026.md           # Tech recommendations
│
├── examples/                          # Real-World Examples
│   ├── landing-page/                  # Fintech landing page
│   ├── dashboard/                     # SaaS dashboard
│   ├── login-form/                    # Auth pages
│   └── README.md                      # Example guide
│
└── docs/                              # Documentation
    ├── installation.md                # Detailed setup
    ├── customization.md               # Adapt to your needs
    ├── troubleshooting.md             # Common issues
    └── contributing.md                # Contribution guide
```

---

## 🎨 Color Palette Preview

### ❌ Banned AI Colors (Never Use)
```
Blue:   #3B82F6, #0066FF  ← Screams "AI-generated"
Violet: #8B5CF6, #A855F7  ← AI favorite cliché
Pink:   #EC4899, #DB2777  ← Too obvious
Cyan:   #06B6D4, #0891B2  ← Overused
```

### ✅ Sophisticated Alternatives (Use These)

**Earthy & Natural:**
```css
Terracotta & Sage:  #E0624B + #6B8E6F  (Professional, grounded)
Olive & Rust:       #6F7545 + #BF6B3F  (Organic, authentic)
```

**Muted & Elegant:**
```css
Slate & Burgundy:   #5B6771 + #8B4851  (Luxury, premium)
Charcoal & Coral:   #3F4448 + #D4725C  (Bold, modern)
```

**Bold & Distinctive:**
```css
Plum & Mustard:     #6B4964 + #D4A243  (Creative, memorable)
Ink Blue & Bronze:  #3D5A6C + #A67C52  (Sophisticated, unique)
```

See all 8 palettes in [`reference/color-palettes.md`](reference/color-palettes.md)

---

## 🔤 Rare Font Collection

Stop using Inter, Roboto, Poppins! Use these instead:

| Category | Fonts | Personality |
|----------|-------|-------------|
| **Geometric Rare** | Rational TW, Scto Grotesk, Replica | Clean, modern, structured |
| **Humanist Rare** | Moranga, GT America, Soehne | Warm, readable, friendly |
| **Display Rare** | Cirka, Roslindale, Agrandir | Bold, distinctive, premium |
| **Monospace Rare** | Berkeley Mono, Commit Mono, Victor Mono | Tech, code-friendly, unique |

Full list with usage guide: [`reference/rare-fonts.md`](reference/rare-fonts.md)

---

## 🛠️ Advanced Usage

### Combine with Your Existing Prompts

```
You: "Create an e-commerce product page with unique design.
      Use the Terracotta & Sage palette and Satoshi font.
      Apply Uncodixfy principles for clean, functional UI."

AI: *generates professional, distinctive UI following all rules*
```

### Override Specific Rules

```
You: "Design a dashboard but use glassmorphism (override Uncodixfy for this case)"

AI: *generates UI with controlled glassmorphism, still maintaining other principles*
```

### Choose Style Preset

```
You: "Create admin panel using UX-OMNI Industrial preset"

AI: *applies 8-point grid, dark charcoal colors, monospace fonts, dev-tool aesthetic*
```

---

## 📖 Learn More

- **[Installation Guide](docs/installation.md)** - Detailed setup for each platform
- **[Customization Guide](docs/customization.md)** - Adapt skills to your brand
- **[Real-World Examples](examples/)** - See it in action
- **[API Integration](api/)** - Use in your own agents
- **[Troubleshooting](docs/troubleshooting.md)** - Common issues & fixes

---

## 🤝 Contributing

We welcome contributions! See [`docs/contributing.md`](docs/contributing.md) for:
- Adding new color palettes
- Suggesting rare fonts
- Sharing real-world examples
- Improving documentation

---

## 📜 License

MIT License - Use freely in personal and commercial projects.

See [LICENSE](LICENSE) for full details.

---

## 🙏 Credits

Originally created for **GitHub Copilot CLI** user skills.

Adapted for universal AI agent compatibility by the community.

**Inspiration:**
- Linear (clean, functional design)
- Raycast (fast, accessible UI)
- Stripe (elegant, trustworthy)
- Apple (refined, intentional)
- Framer (smooth, physics-based motion)

---

## 💬 Support

- **Issues:** [GitHub Issues](https://github.com/yourusername/ai-uiux-skills/issues)
- **Discussions:** [GitHub Discussions](https://github.com/yourusername/ai-uiux-skills/discussions)
- **Examples:** Share your creations in Discussions!

---

**Made with ❤️ for AI agents that create beautiful, unique UI**

⭐ Star this repo if it helps you create better designs!
