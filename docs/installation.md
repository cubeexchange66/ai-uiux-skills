# Installation Guide

Complete setup instructions for all platforms.

---

## 🚀 Quick Start (5 Minutes)

### For ChatGPT Users

1. **Go to ChatGPT Settings**
   - Open [ChatGPT](https://chat.openai.com)
   - Click your profile → Settings
   - Go to "Custom Instructions"

2. **Copy & Paste**
   - Open [`chatgpt/custom-instructions.md`](../chatgpt/custom-instructions.md)
   - Copy ALL content
   - Paste into: **"How would you like ChatGPT to respond?"**
   - Save

3. **Test It**
   ```
   You: "Create a landing page for a fintech startup"
   ChatGPT: *generates unique UI with Terracotta & Sage colors, Satoshi font*
   ```

**Done!** ChatGPT now has UI/UX expert skills.

---

### For Claude Users (Projects)

1. **Create New Project**
   - Open [Claude.ai](https://claude.ai)
   - Click "Projects" → "New Project"
   - Name: "UI/UX Design Expert"

2. **Upload Knowledge Files**
   - Click "Add content" → "Upload files"
   - Upload ALL files from [`claude/project-files/`](../claude/project-files/)
   
   **OR** single-file option:
   - Copy content from [`claude/combined-instructions.md`](../claude/combined-instructions.md)
   - Paste into Project Instructions

3. **Test It**
   ```
   You: "Design a SaaS dashboard with unique colors"
   Claude: *applies 8-point grid, sophisticated palette, Uncodixfy principles*
   ```

**Done!** Claude Project has UI/UX skills.

---

## 📚 Detailed Instructions

### ChatGPT: Advanced Setup

#### Option 1: Full Integration (Recommended)
```
1. Settings → Custom Instructions
2. Paste entire chatgpt/custom-instructions.md
3. Save and test
```

#### Option 2: Selective Integration
If you already have custom instructions, append these sections:
```
1. Copy "Color System" section → Paste after your existing color rules
2. Copy "Typography System" → Paste after your font preferences
3. Copy "Verification Checklist" → Add at the end
```

#### Testing Checklist:
- [ ] Generates sophisticated colors (NOT #3B82F6)
- [ ] Uses rare fonts (NOT Inter by default)
- [ ] Applies 8-point grid spacing
- [ ] Components are simple (Uncodixfy compliant)
- [ ] Animations are functional only

---

### Claude: Advanced Setup

#### Option 1: Upload Individual Files
**Best for:** Maximum context & flexibility

1. Create Project: "UI/UX Expert"
2. Upload these files (in order):
   - `claude/project-files/uiux-design-skill.md`
   - `claude/project-files/uncodixfy.md`
   - `claude/project-files/ux-omni-protocol.md`
   - `reference/color-palettes.md` (optional)
   - `reference/rare-fonts.md` (optional)

3. Project Instructions (paste this):
   ```
   Apply UI/UX design skills automatically.
   Use sophisticated color palettes (NO AI clichés).
   Follow Uncodixfy principles for clean UI.
   Apply UX-OMNI protocol for consistency.
   Verify with checklist before finalizing.
   ```

#### Option 2: Combined Single File
**Best for:** Quick setup

1. Create Project
2. Copy ENTIRE content from `claude/combined-instructions.md`
3. Paste into Project Instructions
4. Save

#### Testing Checklist:
- [ ] Color palette selection works
- [ ] 60-30-10 ratio applied
- [ ] 8-point grid enforced
- [ ] Global radius uniformity
- [ ] Accessibility rules followed

---

## 🔧 API Integration

### OpenAI API (Python)

```python
# install: pip install openai

import openai
from pathlib import Path

# Load system prompt
system_prompt = Path("api/system-prompt.txt").read_text()

client = openai.OpenAI(api_key="YOUR_API_KEY")

response = client.chat.completions.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "Create a login page with unique design"}
    ]
)

print(response.choices[0].message.content)
```

### OpenAI API (Node.js)

```javascript
// install: npm install openai

import OpenAI from 'openai';
import fs from 'fs';

const systemPrompt = fs.readFileSync('api/system-prompt.txt', 'utf8');

const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY
});

const completion = await openai.chat.completions.create({
  model: "gpt-4",
  messages: [
    { role: "system", content: systemPrompt },
    { role: "user", content: "Design a dashboard for SaaS product" }
  ]
});

console.log(completion.choices[0].message.content);
```

### LangChain (Python)

```python
# install: pip install langchain openai

from langchain.chat_models import ChatOpenAI
from langchain.prompts import SystemMessagePromptTemplate, HumanMessagePromptTemplate, ChatPromptTemplate
from pathlib import Path

# Load system instructions
system_prompt = Path("api/system-prompt.txt").read_text()

# Create chat model
chat = ChatOpenAI(
    model="gpt-4",
    temperature=0.7
)

# Create prompt template
system_message = SystemMessagePromptTemplate.from_template(system_prompt)
human_message = HumanMessagePromptTemplate.from_template("{user_input}")
chat_prompt = ChatPromptTemplate.from_messages([system_message, human_message])

# Generate response
messages = chat_prompt.format_prompt(
    user_input="Create a pricing page with unique design"
).to_messages()

response = chat(messages)
print(response.content)
```

---

## 🛠️ Customization

### Adapt to Your Brand

1. **Edit Color Palette**
   ```markdown
   # In your custom instructions, replace:
   --primary: #E0624B;  # Terracotta
   
   # With your brand color:
   --primary: #YOUR_BRAND_COLOR;
   ```

2. **Set Default Font**
   ```markdown
   # Add to instructions:
   "Always use [Your Brand Font] for headings"
   "Always use [Your Body Font] for body text"
   ```

3. **Define Radius**
   ```markdown
   # Add to instructions:
   "Always use 8px border-radius (sharp, modern)"
   # OR
   "Always use 12px border-radius (soft, friendly)"
   ```

See [`docs/customization.md`](customization.md) for full guide.

---

## ✅ Verification

After installation, test with these prompts:

### Test 1: Color Verification
```
Prompt: "Show me the color palette you'll use for a finance app"

Expected: Should NOT suggest #3B82F6, #8B5CF6, etc.
Should suggest: Slate & Burgundy or similar sophisticated palette
```

### Test 2: Component Design
```
Prompt: "Design a button component"

Expected: 
- Specific hex color (NOT Tailwind defaults)
- 8-point grid padding
- Unified border radius
- Functional hover/active states
- WCAG AA compliant
```

### Test 3: Full Page
```
Prompt: "Create a landing page for eco-friendly product"

Expected:
- Olive & Rust or Terracotta & Sage palette
- Rare fonts (NOT Inter)
- 8-point grid spacing
- Simple, functional components
- Mobile-responsive
- Accessibility compliant
```

---

## 🆘 Troubleshooting

### ChatGPT Issues

**Problem:** Still generating generic AI colors  
**Solution:** 
1. Clear custom instructions
2. Paste again (ensure FULL content copied)
3. Start new chat (old chats may have cached behavior)

**Problem:** Not following 8-point grid  
**Solution:** In prompt, explicitly say: "Use 8-point grid spacing"

---

### Claude Issues

**Problem:** Not applying skills automatically  
**Solution:**
1. Check Project Instructions include: "Apply automatically"
2. Ensure files uploaded successfully
3. Try combined-instructions.md instead of separate files

**Problem:** Colors still generic  
**Solution:** In Project Instructions, add at top:
```
CRITICAL: NEVER use #3B82F6, #8B5CF6, #EC4899, #06B6D4.
ALWAYS use sophisticated palettes from color-palettes.md.
```

---

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/yourusername/ai-uiux-skills/issues)
- **Discussions:** [GitHub Discussions](https://github.com/yourusername/ai-uiux-skills/discussions)
- **Examples:** See [`examples/`](../examples/) directory

---

**Next Steps:**
- Read [`customization.md`](customization.md) to adapt to your brand
- See [`examples/`](../examples/) for real-world implementations
- Check [`troubleshooting.md`](troubleshooting.md) for common issues

