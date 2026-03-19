# API Integration - Use Skills in Your Own Agents

Integrate UI/UX skills into your custom AI agents and applications.

---

## 📦 What's Included

- **`system-prompt.txt`** - Complete system prompt for API use
- **Python Examples** - OpenAI API, LangChain
- **JavaScript Examples** - Node.js, OpenAI SDK
- **Framework Examples** - AutoGPT, CrewAI configs

---

## 🚀 Quick Start

### Python (OpenAI API)

```python
# Install: pip install openai

import openai
from pathlib import Path

# Load UI/UX system prompt
system_prompt = Path("system-prompt.txt").read_text()

client = openai.OpenAI(api_key="YOUR_API_KEY")

response = client.chat.completions.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "Design a login page"}
    ]
)

print(response.choices[0].message.content)
```

---

### Node.js (OpenAI SDK)

```javascript
// Install: npm install openai

import OpenAI from 'openai';
import fs from 'fs';

const systemPrompt = fs.readFileSync('system-prompt.txt', 'utf8');

const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY
});

const completion = await openai.chat.completions.create({
  model: "gpt-4",
  messages: [
    { role: "system", content: systemPrompt },
    { role: "user", content: "Create a dashboard component" }
  ]
});

console.log(completion.choices[0].message.content);
```

---

## 🧠 LangChain Integration

### Python

```python
# Install: pip install langchain openai

from langchain.chat_models import ChatOpenAI
from langchain.prompts import SystemMessagePromptTemplate, ChatPromptTemplate
from pathlib import Path

# Load skills
system_prompt = Path("system-prompt.txt").read_text()

# Create model
chat = ChatOpenAI(model="gpt-4", temperature=0.7)

# Create prompt
system_msg = SystemMessagePromptTemplate.from_template(system_prompt)
human_msg = HumanMessagePromptTemplate.from_template("{input}")
prompt = ChatPromptTemplate.from_messages([system_msg, human_msg])

# Generate
chain = prompt | chat
response = chain.invoke({"input": "Design a pricing page"})
print(response.content)
```

### TypeScript

```typescript
// Install: npm install langchain @langchain/openai

import { ChatOpenAI } from "@langchain/openai";
import { ChatPromptTemplate } from "@langchain/core/prompts";
import fs from 'fs';

const systemPrompt = fs.readFileSync('system-prompt.txt', 'utf8');

const chat = new ChatOpenAI({
  modelName: "gpt-4",
  temperature: 0.7
});

const prompt = ChatPromptTemplate.fromMessages([
  ["system", systemPrompt],
  ["human", "{input}"]
]);

const chain = prompt.pipe(chat);

const response = await chain.invoke({
  input: "Create a button component"
});

console.log(response.content);
```

---

## 🤖 Framework Integration

### AutoGPT

Create `autogpt-uiux-config.yaml`:

```yaml
name: "UIUXDesigner"
description: "AI agent for creating unique, accessible UI/UX designs"

system_prompt: |
  [Paste content from system-prompt.txt here]

goals:
  - Create sophisticated UI designs (NO AI clichés)
  - Use rare fonts and muted color palettes
  - Follow 8-point grid spacing system
  - Ensure WCAG AA accessibility
  - Apply Uncodixfy principles

commands:
  design_component:
    description: "Design a UI component"
    args:
      component_type: "button|card|input|etc"
      style: "brand personality"
      
  create_palette:
    description: "Generate sophisticated color palette"
    args:
      industry: "fintech|ecommerce|saas|etc"
      
  verify_design:
    description: "Verify design against checklist"
    args:
      design: "component or page design"
```

Usage:
```bash
autogpt --config autogpt-uiux-config.yaml
```

---

### CrewAI

```python
# Install: pip install crewai

from crewai import Agent, Task, Crew
from pathlib import Path

# Load UI/UX skills
system_prompt = Path("system-prompt.txt").read_text()

# Create UI/UX Designer Agent
designer = Agent(
    role='UI/UX Designer',
    goal='Create unique, accessible UI designs',
    backstory=system_prompt,
    verbose=True
)

# Create Task
design_task = Task(
    description='Design a landing page for a fintech startup',
    agent=designer,
    expected_output='Complete landing page design with code'
)

# Create Crew
crew = Crew(
    agents=[designer],
    tasks=[design_task],
    verbose=True
)

# Execute
result = crew.kickoff()
print(result)
```

---

## 🎯 Advanced Usage

### Custom Color Palette Injection

```python
import openai
from pathlib import Path

# Load base prompt
base_prompt = Path("system-prompt.txt").read_text()

# Add company-specific colors
company_colors = """
COMPANY BRAND COLORS (Use these):
- Primary: #YOUR_HEX
- Secondary: #YOUR_HEX
- Accent: #YOUR_HEX
"""

full_prompt = base_prompt + "\n\n" + company_colors

client = openai.OpenAI()
response = client.chat.completions.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": full_prompt},
        {"role": "user", "content": "Design our login page"}
    ]
)
```

---

### Streaming Responses

```python
import openai
from pathlib import Path

system_prompt = Path("system-prompt.txt").read_text()

client = openai.OpenAI()

stream = client.chat.completions.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "Design a dashboard"}
    ],
    stream=True
)

for chunk in stream:
    if chunk.choices[0].delta.content:
        print(chunk.choices[0].delta.content, end='')
```

---

### Multi-Turn Conversation

```python
import openai
from pathlib import Path

system_prompt = Path("system-prompt.txt").read_text()
client = openai.OpenAI()

messages = [
    {"role": "system", "content": system_prompt},
    {"role": "user", "content": "Design a button"}
]

# First response
response1 = client.chat.completions.create(
    model="gpt-4",
    messages=messages
)

# Add to conversation
messages.append({
    "role": "assistant", 
    "content": response1.choices[0].message.content
})

# Follow-up
messages.append({
    "role": "user",
    "content": "Now make it larger and add an icon"
})

response2 = client.chat.completions.create(
    model="gpt-4",
    messages=messages
)

print(response2.choices[0].message.content)
```

---

## 📊 Token Usage Optimization

The full `system-prompt.txt` is ~3000 tokens. For cost optimization:

### Option 1: Use GPT-4 Turbo
```python
model="gpt-4-turbo-preview"  # Cheaper, same quality
```

### Option 2: Condense System Prompt
Use only critical sections for specific tasks:

```python
# For colors only
colors_prompt = """
Use sophisticated color palettes:
- Terracotta & Sage: #E0624B + #6B8E6F
- Slate & Burgundy: #5B6771 + #8B4851
- Plum & Mustard: #6B4964 + #D4A243

NEVER use: #3B82F6, #8B5CF6, #EC4899
"""

# For spacing only
spacing_prompt = """
Use 8-point grid: 8px, 16px, 24px, 32px, 48px, 64px
NEVER use arbitrary: 13px, 17px, 23px
"""
```

### Option 3: Cache System Prompt (Anthropic Claude)
```python
# Claude supports prompt caching
import anthropic

client = anthropic.Anthropic()

message = client.messages.create(
    model="claude-3-5-sonnet-20241022",
    max_tokens=1024,
    system=[
        {
            "type": "text",
            "text": system_prompt,
            "cache_control": {"type": "ephemeral"}  # Cache this!
        }
    ],
    messages=[
        {"role": "user", "content": "Design a login page"}
    ]
)
```

---

## 🧪 Testing

```python
# test_uiux_skills.py

import openai
from pathlib import Path

def test_color_verification():
    """Test that AI avoids banned colors"""
    system_prompt = Path("system-prompt.txt").read_text()
    
    client = openai.OpenAI()
    response = client.chat.completions.create(
        model="gpt-4",
        messages=[
            {"role": "system", "content": system_prompt},
            {"role": "user", "content": "Show me colors for a tech startup"}
        ]
    )
    
    content = response.choices[0].message.content
    
    # Should NOT contain banned colors
    assert "#3B82F6" not in content
    assert "#8B5CF6" not in content
    assert "#EC4899" not in content
    
    print("✅ Color verification passed")

def test_spacing_system():
    """Test that AI uses 8-point grid"""
    system_prompt = Path("system-prompt.txt").read_text()
    
    client = openai.OpenAI()
    response = client.chat.completions.create(
        model="gpt-4",
        messages=[
            {"role": "system", "content": system_prompt},
            {"role": "user", "content": "Design a card component with CSS"}
        ]
    )
    
    content = response.choices[0].message.content
    
    # Should contain 8-point grid values
    assert any(val in content for val in ["8px", "16px", "24px", "32px"])
    
    # Should NOT contain arbitrary values
    assert "13px" not in content
    assert "17px" not in content
    
    print("✅ Spacing system passed")

if __name__ == "__main__":
    test_color_verification()
    test_spacing_system()
    print("\n🎉 All tests passed!")
```

Run tests:
```bash
python test_uiux_skills.py
```

---

## 💰 Cost Estimation

Based on OpenAI pricing (as of 2026):

| Model | Input (per 1M tokens) | Output (per 1M tokens) | Typical Request |
|-------|----------------------|----------------------|-----------------|
| GPT-4 Turbo | $10 | $30 | ~$0.10 |
| GPT-4 | $30 | $60 | ~$0.20 |
| GPT-3.5 Turbo | $0.50 | $1.50 | ~$0.01 |

**Recommendation:** Use GPT-4 Turbo for best quality/cost ratio.

---

## 📚 See Also

- [`system-prompt.txt`](system-prompt.txt) - Full prompt file
- [`examples/`](../examples/) - Real-world implementations
- [`../docs/installation.md`](../docs/installation.md) - Setup guide

---

**Need help?** [Open an issue](https://github.com/yourusername/ai-uiux-skills/issues)
