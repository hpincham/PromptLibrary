# GPT-5 XML Prompt Templates — Tiered Manual (with Verification Toggle)

<!--
  GPT-5 Prompt Manual
  © 2025 Howard Pincham & Sage (OpenAI Assistant)
  License: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/)
  Contact: howard@example.com
-->

A practical, tiered system for crafting clear, reliable prompts for GPT-5.  
Now includes a **feature-flagged VerificationMode** to control evidence rigor per prompt.

---

## 🔎 Why Three Tiers?

| Tier | Best for | Fill Time | Control |
|---|---|---:|---:|
| **Basic** | Everyday queries, brainstorming, short factual tasks | 2–3 min | Low |
| **Intermediate** | Study guides, planning, structured briefs | 5–7 min | Medium |
| **Advanced** | Research, strategy, publish-ready deliverables | 8–15 min | High |

---

## 🚀 Quick Start

1) Pick a tier (table above).  
2) Fill the XML (short, specific sentences).  
3) **Set `<VerificationMode><Mode>`**: `off` (default), `report`, or `strict`.  
4) Paste into GPT-5 (enable thinking/deep research for Advanced).  
5) Check against your **QualityBar**; revise and re-run if needed.

---

## 🧩 VerificationMode (new)

**What it does:** Governs how the model handles claims, uncertainty, and citations.

- `<Mode>off</Mode>` — **Inactive.** Ignore all rules in `<VerificationMode>`.  
- `<Mode>report</Mode>` — No noisy inline tags. The body stays clean; add a final **“Confidence & Sources”** section listing claims with confidence + citations.  
- `<Mode>strict</Mode>` — Inline caution for high-risk language. Prefix high-risk sentences with `[Unverified]`, `[Inference]`, or `[Speculation]`. Use when accuracy matters more than prose polish.

**Other controls:**
- **`<VerificationRule>`** — Define what counts as *verified* (e.g., provided inputs, primary sources within 12 months).  
- **`<WhenCannotVerify>`** — Behavior when tools/browsing are off or data is missing (ask up to N questions; label assumptions).  
- **`<Labeling>`** — Trigger terms (e.g., *prevent/guarantee/eliminates/ensures*) auto-flag unless sourced.  
- **`<InputHandling>`** — Do not alter quoted facts/numbers unless asked; still allow requested rewrites.  
- **`<CorrectionProtocol>`** — One-line corrective note if an unsourced assertion slipped through.

> **Default:** `off` in Intermediate/Advanced; **`strict`** in the Evidence-Critical template.

---

## 🟢 Tier 1 — Basic Template

**Use for:** quick drafts, short explanations, simple Q&A.  
**Sections:** `Role (optional)`, `Context (required)`, `Task (required)`, `OutputFormat (optional)`  
*No VerificationMode in Basic.*

---

## 🟡 Tier 2 — Intermediate Template (retrofitted)

Adds **Scope**, **Constraints**, **QualityBar**, and optional **VerificationMode** (default `off`).  
Use VerificationMode when your output will be used for decisions or published.

**Pass/fail examples for QualityBar:**
- “Contains a timeline table with dates”  
- “≤ 2 major recommendations per section”  
- “Every claim referencing numbers has a source & date”

---

## 🔴 Tier 3 — Advanced Template (retrofitted)

Adds **Meta**, **Inputs**, **NonGoals**, **AdvancedInstructions**, and **VerificationMode** (default `off`).  
Use `report` when you want a clean body plus a claims table; use `strict` for audits/compliance.

---

## 🧪 Evidence-Critical Template (new)

Purpose-built for compliance, audit, academic, or safety work.  
Pre-sets **`<Mode>strict</Mode>`** and a rigorous **OutputFormat** with an **Evidence Table**.

---

## 🧭 Best Practices

1. **Task is king.** One sentence, action-led, scoped.  
2. **Context prevents guesses.** Include only relevant facts.  
3. **OutputFormat = usability.** Dictate sections/tables.  
4. **QualityBar = self-check.** Make checks measurable.  
5. **Use VerificationMode only when it adds value.**  
6. **If tools are off**, expect more “[Unverified]” or clarifying questions — that’s correct.

---

## ✅ Validation Checklist

- [ ] Task is clear, single sentence.  
- [ ] Context has only relevant, true facts.  
- [ ] OutputFormat lists exact sections/tables.  
- [ ] QualityBar has 3–6 measurable checks (if used).  
- [ ] VerificationMode mode set: `off | report | strict`.  
- [ ] No contradictions across sections.  
- [ ] Tools policy matches VerificationMode expectations.

---

## 📝 Mini Examples of the Toggle

**Report mode (clean body + final claims table):**
```xml
<VerificationMode>
  <Mode>report</Mode>
  <IfOff>Ignore all rules in this block; proceed with normal instructions.</IfOff>
  <VerificationRule>VERIFIED = provided inputs or primary source ≤12 months old.</VerificationRule>
</VerificationMode>
