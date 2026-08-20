# {Project or prototype name} — Prototype Design Review

> Expert read on the directional prototype shared by {stakeholder name or role}: what's working and worth keeping, what to leave out of the MVP, what to redesign, and the questions that will get design off to the strongest start.

{One sentence on what was shared — link or path to prototype, plus stakeholder notes if any.}

This document **complements** (does not replace) any existing visual design review. The walkthrough sorts every UI block into **Keep / Validate / Clarify / Out of scope**, then scales with a data-field inventory.

---

## SCQR narrative

**Situation.** {What is true today that everyone agrees on — neutral, factual}

**Complication.** {Two or three areas that would benefit from a decision before building — frame as choices}

**Question.** {How do we evolve this prototype into something users will actually use?}

**Resolution.** {Keep proven patterns; remove out-of-scope modules; redesign where intent is right but execution is off. Include approximate Keep/Validate/Clarify/Out-of-scope counts only if calculable from triage — never invent percentages}

---

# Part 1 — Walkthrough (screen by screen)

*North Star per screen, layout anatomy, and explicit flags for what can't be settled from the prototype alone.*

## 1a. North Star statements

| Surface | North Star job | Execution vs. stakeholder intent |
|---------|----------------|----------------------------------|
| {screen id or name} | {one sentence} | {alignment or **bold misalignment**} |

**Pattern:** {One sentence on the biggest structural finding across screens}

## 1b. Layout anatomy + flags

### `{screen_id}`

- **Regions:** {sidebar, header, main, footer CTA, etc.}
- **Primary action:** {what the UI pushes the user toward}
- **Flags:** `[clarify]` … `[validate]` …

{Repeat per screen on the primary user path}

## 1c. Block-by-block assessment

| # | UI block | Verdict | Basis |
|---|----------|---------|-------|
| 1 | {block name} | **Keep** / **Validate** / **Clarify** / **Out of scope** | {cite source — stakeholder note, screen, or "prototype only"} |

**The one structural thing to settle:**

{One paragraph or short code citation on the highest-impact structural choice, with source}

---

# Part 2 — Questions to start design

*Five that matter most. Each names the prototype element, frames the choice, offers a default, and maps to the decision it unblocks.*

### How I'd open the conversation

> "{Conversation opener — 2–3 sentences, collaborative. Do not use internal tag names.}"

### The five questions

**Q1 — {Topic}.**
{Gap: intent vs execution, naming the prototype element}
- *Suggested default:* {answer if stakeholder is silent}
- *Unblocks:* {design decision}

**Q2 — {Topic}.**
{Gap description}
- *Suggested default:* {answer}
- *Unblocks:* {design decision}

**Q3 — {Topic}.**
{Gap description}
- *Suggested default:* {answer}
- *Unblocks:* {design decision}

**Q4 — {Topic}.**
{Gap description}
- *Suggested default:* {answer}
- *Unblocks:* {design decision}

**Q5 — {Topic}.**
{Gap description}
- *Suggested default:* {answer}
- *Unblocks:* {design decision}

---

# Part 3 — Field inventory & consistency

## 3a. Data field inventory

### Domain: {domain_name}

| Field / artifact | Screen | Pre-filled? | Editable? | Action | Verdict | MVP status |
|------------------|--------|-------------|-----------|--------|---------|------------|
| {field} | {screen} | {Y/N/?} | {Y/N/?} | {approve/submit/none} | **Keep** / etc. | {in / out / clarify} |

{Repeat per domain — only fields visible in prototype or cited in notes}

## 3b. Cross-screen consistency check

- **Approval vocabulary:** {Confirm vs Approve vs bulk — flag drift}
- **Progress model:** {steps vs unified process}
- **Role surfaces:** {demo personas vs MVP scope}
- **Duplicate concepts:** {same idea, different labels}
- **Missing counterparts:** {stakeholder said X, UI shows Y or nothing}

## 3c. Synthesis

### Keep (proven, on-strategy)

- {bullet}

### Remove (out of scope — set aside without losing the idea)

- {bullet}

### Redesign (right intent, better execution)

- {bullet}

### Clarify (surface in stakeholder session)

- {bullet}

## Appendix — Verdict density per screen (optional)

| Screen | Keep | Validate | Out of scope | Clarify |
|--------|------|----------|--------------|---------|
| {screen} | {n} | {n} | {n} | {n} |

**Read:** {One sentence summary — only if counts were computed from triage}

---

## Sources

- {Prototype — URL, file path, or description}
- {Stakeholder notes — file, channel, date if known}
- {PRD, workshop notes, or other evidence — if provided}
- {Existing design review — if complemented, not replaced}
- Framework: [Vibe-Check (Marian Torrealba)](https://uxsidekick.substack.com/p/stop-designing-upon-what-the-pm-vibe) + SCQR stakeholder narrative
