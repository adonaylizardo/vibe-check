# Vibe-Check Framework — Method Notes

**Origin:** Marian Torrealba — [Stop Designing Upon What the PM Vibe-Coded](https://uxsidekick.substack.com/p/stop-designing-upon-what-the-pm-vibe)

**Packaged for agents by:** [Adonay Design OS](https://github.com/adonaylizardo/adonay-design-os) (method + templates; this skill is a portable extract, not the Design OS CLI).

Marian Torrealba created the Vibe-Check framework. Adonay Lizardo packaged workflow templates for design operations. Neither invented the other's work.

---

## Core idea

When a PM or stakeholder vibe-codes a prototype, teams often treat it as the spec. Design starts copying AI chrome. Vibe-Check separates three layers **before** Figma:

1. **Real requirements** — backed by evidence
2. **Stakeholder assumptions** — plausible but unscoped
3. **AI filler** — no source, likely generator defaults

The prototype is a **brief in disguise**. Review intent, not pixels.

---

## Three phases

| Phase | Name | Output |
|-------|------|--------|
| 1 | **Unpack** | North Star per screen, layout anatomy, triage tags |
| 2 | **Gaps** | Exactly 5 questions + conversation opener |
| 3 | **Scale Up** | Field inventory, consistency check, Keep / Remove / Redesign |

---

## Internal triage tags

Use these during solo analysis:

| Tag | Definition | Stakeholder-facing verdict |
|-----|------------|----------------------------|
| **REQ** | Backed by stakeholder notes, PRD, survey, or cited evidence | **Keep** (if confirmed) or **Validate** (if evidence is thin) |
| **ASSUMP** | Plausible stakeholder thinking, not explicitly scoped | **Validate** or **Clarify** |
| **HALL** | No source; likely AI tool filler | **Out of scope** |
| **FLAG** | Needs stakeholder walkthrough to classify | **Clarify** |

---

## Stakeholder-facing language

In the walkthrough table and SCQR, use only:

- **Keep**
- **Validate**
- **Clarify**
- **Out of scope**

Do **not** say "brief in disguise", "hallucination", "HALL", or "AI filler" in stakeholder-facing prose. Those terms are for internal analysis only.

Tone: collaborative expert review — not a roast, not a compliance audit.

---

## SCQR (stakeholder narrative)

SCQR structures the opening narrative:

| Block | Purpose |
|-------|---------|
| **Situation** | What everyone already agrees is true — neutral, factual |
| **Complication** | Tensions or choices that need a decision before building — frame as choices, not blame |
| **Question** | What must be decided to move forward (often implicit) |
| **Resolution** | Direction: keep, cut, redesign — grounded in the walkthrough |

Rules:

- Situation = uncontested facts the stakeholder already knows
- Complication = the hook — where prototype and intent diverge
- Resolution = specific enough to unblock design, not vague aspirations

---

## The five questions

Exactly **five**, prioritized. Each question must include:

1. **Prototype element** — screen, block, or field name
2. **Gap** — stakeholder intent vs what the prototype shows
3. **Suggested default** — what you'd assume if they have no answer
4. **Unblocks** — the design decision it enables (IA, scope cut, field model, flow order, etc.)

Do not pad with generic questions ("Who is the user?"). Anchor every question in something visible in the prototype or cited in notes.

---

## Relationship to design review

| Activity | Vibe-Check | Visual design review |
|----------|------------|----------------------|
| When | Before Figma | During or after design exploration |
| Focus | Intent, scope, evidence | Visual hierarchy, patterns, accessibility |
| Output | Prototype Design Review markdown | Design critique / annotated frames |
| Starts Figma? | No | Often yes |

Vibe-Check **complements** a design review. If the user provides both a prototype and an existing design review, reference the review as input — do not duplicate or replace it.

---

## Evidence rules

1. **Cite sources** — file name, URL, quote, screen id, or "prototype only".
2. **Never invent** metrics, user counts, field names, or business outcomes not visible in inputs.
3. **Flag uncertainty** — use **Clarify** and `[validate]` flags instead of guessing.
4. **Primary path first** — triage the demoed happy path before edge cases.

---

## Common prototype sources

| Source | How to analyze |
|--------|----------------|
| Lovable / v0 / Bolt / Magic Patterns URL | Open in browser; walk primary path |
| Cursor / local repo | Read key screens; open `index.html` or dev preview if available |
| HTML / Tailwind click-dummy | Browser preferred; else parse source for fields and labels |
| Screenshots | Journey order; note static limitations in flags |
| Figma link (vibe-coded) | Treat as prototype artifact; same triage applies |

---

## When NOT to use

- **Designer-built prototypes** created as intentional design exploration — use design review instead.
- **Production code review** — this is not a code audit.
- **Post-launch analytics** — no invented metrics; if no data was provided, say so.
