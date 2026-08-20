# Example — Five-Question Set (Fictional)

> **This is a clearly labeled fictional example.** No real client, company, or PII. Use it to calibrate question format — not to copy content into live reviews.

**Scenario:** A PM shared a Lovable link for "FleetPulse" — an internal fleet-maintenance dashboard. Workshop notes mention "technicians need to see today's jobs" and "managers approve overtime." No PRD. Primary path: login → today's jobs → job detail → mark complete.

---

## Sample conversation opener

> "This prototype captures a lot of the workshop conversation — especially the technician daily view. I've sorted what's ready to keep from what we'd validate or park for later. Five alignment points would let me shape an MVP scope with confidence."

---

## Sample five questions

**Q1 — "AI Insights" panel on the dashboard home.**
The home screen shows an "AI Insights" card with "3 vehicles likely to fail this week." Workshop notes never mention predictive maintenance — only today's assigned jobs.
- *Suggested default:* Remove from MVP; keep a simple "Today's jobs" count and overdue badge.
- *Unblocks:* Home screen IA — whether the north star is **dispatch** or **prediction**.

**Q2 — "Approve overtime" button on job detail (technician role).**
Technicians can tap "Approve overtime" on their own jobs. Notes say managers approve overtime, not technicians.
- *Suggested default:* Hide overtime approval from technician view; surface a "Request overtime" action that routes to manager queue.
- *Unblocks:* Role-based permissions model and notification flow.

**Q3 — Step indicator "Step 2 of 5" on job detail.**
The prototype shows a five-step wizard (Inspect → Diagnose → Parts → Repair → Close). Notes describe a single "job detail" screen, not a wizard.
- *Suggested default:* Collapse to one scrollable job detail with status chips (Open / In progress / Complete); defer wizard for complex jobs only.
- *Unblocks:* Progress model — unified detail vs stepped flow.

**Q4 — "Export to PDF" in the footer of every screen.**
PDF export appears on list, detail, and settings. Notes mention "managers need weekly reports" but not per-screen export.
- *Suggested default:* One weekly manager report from the admin view; remove per-screen export from technician MVP.
- *Unblocks:* Reporting scope and admin vs technician surface split.

**Q5 — Vehicle ID field labeled "VIN" vs "Unit #" across screens.**
Job list uses "Unit #"; detail header uses "VIN"; workshop notes say "unit number." 
- *Suggested default:* Standardize on "Unit #" everywhere; map VIN to optional expanded detail.
- *Unblocks:* Field inventory and label consistency before Figma components.

---

## Internal triage snapshot (not stakeholder-facing)

| # | UI block | Tag | Basis |
|---|----------|-----|-------|
| 1 | Today's jobs list | REQ | Workshop notes: "technicians need to see today's jobs" |
| 2 | AI Insights card | HALL | No source in notes; typical Lovable filler |
| 3 | Approve overtime (technician) | ASSUMP | Plausible misread of "managers approve overtime" |
| 4 | Step 2 of 5 wizard | HALL | Notes imply single detail view |
| 5 | Export to PDF (all screens) | FLAG | Notes mention weekly reports — scope unclear |

---

## What to learn from this example

- Each question **names a visible prototype element**.
- Each gap contrasts **cited intent** vs **what the UI shows**.
- Each default is a **concrete MVP stance**, not "discuss with team."
- Each unblocks a **specific design decision** (IA, roles, progress model, reporting, labels).

Do not reuse FleetPulse names, fields, or scenarios in real reviews unless the user's prototype actually matches.
