# GPT-5 Prompt Template Manual

<!--
  GPT-5 Prompt Manual
  © 2025 Howard Pincham & Sage (OpenAI Assistant)
  License: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/)
  Contact: howard@clarusigna.com
-->

This manual explains how to use the **tiered GPT-5 Prompt Templates** (Basic, Intermediate, Advanced) effectively.  
It contains a **Quick Start Guide** for immediate use, followed by a **detailed walkthrough** of each section in the templates.

---

## 📄 Quick Start Guide (1 Page)

If you’re in a hurry:

1. **Choose Your Template Tier**  
   - **Basic** → For simple, everyday prompts.  
   - **Intermediate** → For moderately complex tasks.  
   - **Advanced** → For high-stakes, multi-step reasoning.

2. **Fill In Each Section**  
   Replace the `<tags>` with your own content. Keep instructions **clear and specific**.

3. **Run the Prompt in GPT-5**  
   Copy the filled XML into ChatGPT (or GPT-5-enabled tool).

4. **Review the Output**  
   If results aren’t right, adjust your inputs—especially in `<Task>`, `<Constraints>`, and `<OutputFormat>`.

5. **For Deep Research or Complex Reasoning**  
   Use the `<AdvancedInstructions>` section in the Advanced template to request deep thinking, self-review, and tool use.

---

## 🛠 Template Overview

We provide **three tiers** of templates:

### 1. **Basic Template** (Beginner-Friendly)
Focuses on the minimum elements for clarity and output control.

**Sections:**
- `<Task>` → What you want done. Be specific.
- `<Context>` → Relevant background info.
- `<OutputFormat>` → Desired output style or structure.

---

### 2. **Intermediate Template** (For Moderate Complexity)
Adds scope control and quality requirements.

**Sections:**
- `<Task>`
- `<Context>`
- `<Scope>` → Defines what’s in and out of scope.  
- `<Constraints>` → Time limits, tone, style rules.
- `<OutputFormat>`
- `<QualityBar>` → Define what “good” looks like.

---

### 3. **Advanced Template** (For Critical Work)
Designed for maximum control, ideal for deep reasoning, multi-step problem-solving, and high-value outputs.

**Sections:**
- `<Task>`
- `<Context>`
- `<Scope>`
- `<Constraints>`
- `<OutputFormat>`
- `<QualityBar>`
- `<AdvancedInstructions>` → Can include `<DeepResearch>`, `<SelfReview>`, and `<ToolUse>`.
- `<Meta>` → Purpose, audience, stakes.

---

## 🧩 Section-by-Section Walkthrough

### `<Task>`  
**Purpose:** Defines the main job.  
**Tip:** State your request as a single, action-oriented sentence.

### `<Context>`  
**Purpose:** Gives background info for accuracy.  
**Tip:** Include only what’s relevant.

### `<Scope>` (Intermediate & Advanced)  
**Purpose:** Clarifies what’s in and out of scope.  
**Tip:** Use sub-headings “In-Scope” and “Out-of-Scope” inside the tag.

### `<Constraints>`  
**Purpose:** Sets boundaries like time, format, tone.  
**Tip:** Avoid unnecessary constraints that might restrict creativity.

### `<OutputFormat>`  
**Purpose:** Dictates how the answer should be structured.  
**Tip:** Use bullet points, tables, JSON, or markdown for clarity.

### `<QualityBar>`  
**Purpose:** Sets the standard for quality.  
**Tip:** Define specific checks, e.g., “No more than 5% passive voice.”

### `<AdvancedInstructions>` (Advanced Only)  
**Purpose:** Engages GPT-5’s deeper reasoning and optional tool use.  
**Tip:** Explicitly request “step-by-step reasoning” or “internal self-check.”

### `<Meta>` (Advanced Only)  
**Purpose:** Helps GPT-5 adapt tone and approach.  
**Tip:** Clearly state who will read it and why.

---

## 📚 Example Prompt Uses

### Example 1: **Basic Template — Blog Post**
```xml
<Task>Write a 500-word blog post about the benefits of remote work for small businesses.</Task>
<Context>Audience: small business owners new to remote work.</Context>
<OutputFormat>Markdown format with 3 headings and bullet lists.</OutputFormat>
```

### Example 2: **Intermediate Template — Event Plan**
```xml
<Task>Create a one-day conference schedule for tech entrepreneurs.</Task>
<Context>Theme: AI and business growth.</Context>
<Scope>
    <InScope>AI in marketing, AI ethics, funding strategies.</InScope>
    <OutOfScope>Technical AI programming tutorials.</OutOfScope>
</Scope>
<Constraints>Must fit into 8 hours, include breaks.</Constraints>
<OutputFormat>Table format with time slots and session titles.</OutputFormat>
<QualityBar>At least 3 keynote speakers, balanced topic coverage.</QualityBar>
```

### Example 3: **Advanced Template — Deep Research**
```xml
<Task>Analyze the future of quantum computing for financial modeling.</Task>
<Context>Intended for CTOs of fintech companies evaluating tech investment.</Context>
<Scope>
    <InScope>Market forecasts, technical readiness, key players.</InScope>
    <OutOfScope>Quantum cryptography details.</OutOfScope>
</Scope>
<Constraints>2000-word report, use citations.</Constraints>
<OutputFormat>Markdown report with executive summary, analysis, and conclusion.</OutputFormat>
<QualityBar>All claims backed by at least two sources.</QualityBar>
<AdvancedInstructions>
    <DeepResearch>Search latest papers and market data as of 2025.</DeepResearch>
    <SelfReview>Check for logical gaps and unsupported claims.</SelfReview>
</AdvancedInstructions>
<Meta>Purpose: guide investment decisions. Audience: fintech CTOs. Stakes: multi-million dollar investments.</Meta>
```

---

## ✅ Best Practices
- Start with **Basic** if you’re new. Move to **Intermediate** or **Advanced** as you get comfortable.
- Keep language clear. Avoid ambiguity.
- Only include optional sections if they truly add value.
- Always review GPT-5’s output before using.



## 📖 Disclaimer  

These templates and instructions are provided **“as-is”** for educational and practical purposes.  
No warranties are expressed or implied regarding accuracy, completeness, or suitability for any purpose.  

The authors (Howard Pincham & Sage, OpenAI Assistant) are **not responsible** for errors, omissions, misinterpretations, or outcomes resulting from use of this material.  

Use at your own discretion and always review generated outputs before relying on them.  

---

© 2025 Howard Pincham — Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
