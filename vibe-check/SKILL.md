---
name: vibe-check
description: Use this when a stakeholder or teammate vibe-coded a prototype (Lovable, v0, Cursor, HTML, screenshots) and you must separate requirements from assumptions and AI filler before designing.
---

# Vibe-Check — Prototype Design Review

**Framework:** Vibe-Check (Marian Torrealba) — [Stop Designing Upon What the PM Vibe-Coded](https://uxsidekick.substack.com/p/stop-designing-upon-what-the-pm-vibe)

## Reframe

The prototype is **not a spec**. It is a **brief in disguise** — a mix of real requirements, stakeholder assumptions, and AI filler. Your job is to separate those layers before designing in Figma or writing specs.

Review **intent**, not pixels. This skill complements a visual design review; it does not replace one. Do **not** start Figma, rewrite the prototype, or invent metrics.

## When to use

- A PM, founder, or client shared a vibe-coded prototype (Lovable, v0, Cursor, Bolt, Magic Patterns, HTML, screenshots, or a repo) and design is about to start.
- You need to know what is required vs assumed vs generator filler before opening Figma.
- You are preparing for an alignment call and need exactly five decisions that unblock MVP.

## What to gather from the user

Ask for (or infer from context) whatever is available:

| Input | How to use it |
|-------|---------------|
| **Prototype URL** (Lovable, v0, deployed preview) | Open in browser when possible; walk the primary user path end-to-end |
| **Local HTML / repo path** | Prefer opening in browser; else read source for layout and field inventory |
| **Screenshots / screen recording** | Walk screens in journey order; note what cannot be validated from static images |
| **Stakeholder notes** (Slack, workshop notes, email, PRD excerpt) | Primary evidence for REQ tags — cite file or quote |
| **Existing design review** | Input only — complement, do not copy wholesale |

**Language:** Write the review in the language of the source material and intended audience (English or Spanish). Do not mix languages in one document.

## References (load on demand)

Read only what you need:

- `references/framework.md` — method notes, tag definitions, SCQR guidance
- `references/analysis-template.md` — output skeleton for the review document
- `references/examples.md` — fictional example of a five-question set (calibration only)

## Workflow

### Step 0 — Orient

1. Identify the **primary user path** (the happy path the stakeholder demoed or cares about most).
2. List all inputs you have and note gaps ("no stakeholder notes — triage will rely on prototype-only evidence").
3. If `insights/` exists in the project, write output there; otherwise write to the current working directory.

**Output file:** `vibe-check-analysis.md` (in `insights/` if that folder exists, else cwd).

### Step 1 — Unpack (solo analysis)

Work the **primary user path** first, then note other roles or edge paths briefly.

#### 1a. North Star statements

One sentence per navigable surface: **what is this screen's job?**

For each North Star, add:

- **Stakeholder intent** (from their notes, if any)
- **Prototype execution** (what the UI actually does)
- Mark misalignments in **bold**

#### 1b. Layout anatomy + flags

Per screen, document:

- **Regions** (sidebar, main panel, footer CTA, master-detail, etc.)
- **Primary action** (what the UI pushes the user to do)
- **Flags** — cannot validate from prototype alone:
  - Pre-fill source unknown
  - Routing destinations after approve/submit
  - Delegation or reassignment behavior
  - Channel indicator (Teams vs in-app, etc.)
  - Empty / loading / error states
  - Bulk actions in production

#### 1c. Triage matrix (internal)

Tag every major UI block using internal tags:

| Tag | Definition |
|-----|------------|
| **REQ** | Backed by stakeholder notes, PRD, survey, or other cited evidence |
| **ASSUMP** | Plausible stakeholder thinking, not explicitly scoped |
| **HALL** | No source; likely AI tool filler |
| **FLAG** | Needs stakeholder walkthrough to classify |

Build a block-by-block table: `# | UI block | Tag | Basis (cite source)`.

**Stakeholder-facing translation:** In Part 1 of the output, map tags to verdicts:

| Internal tag | Stakeholder verdict |
|--------------|---------------------|
| REQ (confirmed) | **Keep** |
| REQ (unverified) or ASSUMP | **Validate** or **Clarify** |
| HALL or explicit out-of-scope | **Out of scope** |
| FLAG | **Clarify** |

Never use "brief in disguise", "hallucination", or "HALL" in stakeholder-facing prose.

### Step 2 — The Gaps (stakeholder alignment)

Produce **exactly 5 prioritized questions**. Each must:

1. Name the **prototype element** that triggered it
2. State the **intent vs execution gap**
3. Include a **suggested default** if the stakeholder has no answer
4. Map to the **design decision** it unblocks

Include a **conversation opener** (2–3 sentences, collaborative expert tone — not a roast):

> "A prototype is a great way to think out loud, and this one gives us a lot to work with. I've gone through it and sorted what's ready to keep from what we'd validate or leave out. There are five things I'd love to align on so I can shape the MVP with confidence."

Adapt the opener to the project's language and tone.

### Step 3 — Scale Up (field inventory)

AI handles volume; you handle intention and judgment.

#### 3a. Data field inventory

Master table grouped by domain (metadata, proposal, knowledge, compliance, feedback, etc.):

| Field / artifact | Screen | Pre-filled? | Editable? | Approve action? | Verdict | Consistent label elsewhere? | MVP status |

Only include fields you can see or infer from cited sources. Never invent fields or metrics.

#### 3b. Cross-screen consistency check

Flag patterns:

- Approval vocabulary ("Confirm" vs "Approve" vs bulk actions)
- Progress model (step count vs unified process)
- Role surfaces (demo personas vs MVP scope)
- Duplicate concepts across screens
- Missing counterparts (stakeholder says "valuable" but UI absent)

#### 3c. Synthesis

Three columns plus clarify:

- **Keep** — REQ elements worth preserving
- **Remove** — filler + explicit out-of-scope cuts
- **Redesign** — ASSUMP + misaligned REQ (right intent, better execution)
- **Clarify** — surface in stakeholder session

Optional appendix: verdict counts per screen (only if calculable from your triage — never invent percentages).

### Step 4 — SCQR narrative

At the top of the output (after title + intro), write a **SCQR narrative**:

- **Situation** — what is true today that everyone agrees on (neutral, factual)
- **Complication** — choices or tensions that benefit from a decision before building
- **Question** — how do we evolve this prototype into something users will actually use?
- **Resolution** — keep proven patterns; remove out-of-scope modules; redesign where intent is right but execution is off

Collaborative expert-review tone. Do not use internal tag names in SCQR prose.

### Step 5 — Write the deliverable

Follow `references/analysis-template.md` for structure.

**Rules:**

1. Every recommendation must **cite a source** — stakeholder note, screen id, URL, or explicit "prototype only, no external source".
2. **Never invent** metrics, field names, user counts, or business outcomes.
3. **Complement** an existing design review if one was provided — do not replace it.
4. **Do not** start Figma, create specs, or rewrite the prototype.
5. For HTML prototypes: prefer opening in a browser; parse source for the field inventory if browser is unavailable.
6. Walk the **primary user path** first.

## Deliverable

One markdown file: **`vibe-check-analysis.md`**

Location: `insights/vibe-check-analysis.md` if an `insights/` folder exists in the project; otherwise `./vibe-check-analysis.md`.

After writing, tell the user:

- Where the file was saved
- The five questions (titles only) as a quick preview
- Any critical gaps in inputs that would strengthen a second pass
