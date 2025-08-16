# PromptLibrary
Prompts to share with the world.

# GPT-5 XML Prompt Template Package

Tiered XML prompt templates and guides for crafting high-quality prompts in GPT-5.  
Designed for users who have experience with ChatGPT but want more discipline, structure, and control over the model’s output.

This package includes **three levels** of templates:
- **Basic** — For quick, low-stakes prompts
- **Intermediate** — For structured tasks with predictable output
- **Advanced** — For high-stakes, deep-research, and mission-critical work

---

## 📦 Contents
- `/templates/Basic.xml` — Minimal template with Role, Context, Task, OutputFormat  
- `/templates/Intermediate.xml` — Adds Scope, Constraints, QualityBar  
- `/templates/Advanced.xml` — Full-featured with Meta, NonGoals, AdvancedInstructions, Examples, AmbiguityHandling, Acceptance, CallToAction  
- `/docs/User_Guide.pdf` — Complete guide on how to use the templates effectively

---

## 🚀 How to Use

### 1. Pick a Template
Choose the tier based on the complexity and stakes of your task:
- **Basic** — Quick drafts, brainstorming, factual queries
- **Intermediate** — Research summaries, study guides, planning documents
- **Advanced** — Job targeting, strategic planning, technical analysis

### 2. Fill the Sections
Each section is marked with XML comments (`<!-- ... -->`) explaining what to put there.
- **Optional sections** are clearly labeled — skip them if they’re not relevant.
- **Required sections** should always be filled for best results.

### 3. Paste into GPT-5
- Select GPT-5 in ChatGPT (thinking/deep research mode recommended for Advanced template).
- Paste the filled-in XML into the chat window.
- Review the output against your **QualityBar** (Intermediate/Advanced templates).

---

## 📝 Example: Intermediate Tier
```xml
<GPT5Prompt>
  <Role>Travel planner specializing in European family vacations</Role>
  <Context>Family of 4 traveling in June, mid-range budget, loves history and food, prefers trains</Context>
  <Task>Create a 7-day Rome + Florence itinerary with verified train times and daily costs</Task>
  <Scope>
    <InScope>Historic landmarks, museums, food tours</InScope>
    <OutOfScope>No nightlife, no more than 2 hotel changes</OutOfScope>
  </Scope>
  <Constraints>Warm, practical tone; 1,000–1,200 words; train times accurate to ±30 min</Constraints>
  <QualityBar>(1) Train times accurate; (2) ≤2 major sites/day; (3) At least 2 unique cultural experiences</QualityBar>
  <OutputFormat>
    1. Day-by-Day Plan
    2. Cost Table
    3. Packing Tips
    4. Cultural Notes
  </OutputFormat>
</GPT5Prompt>


## License

This repository, including the GPT-5 Prompt Template and documentation, is licensed under the 
[Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material in any medium or format.
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.

Under the following terms:
- **Attribution** — Give appropriate credit, provide a link to this repository, 
  and indicate if changes were made.

No additional restrictions — You may not apply legal terms or technological measures that 
legally restrict others from doing anything the license permits.

---
*© 2025 Howard Pincham. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*
