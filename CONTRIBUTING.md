# Contributing to this skills library

## The one rule
Every skill follows the house **"do + teach"** standard, which is defined in
[`coding-agent-skills:writing-agent-skills`](plugins/coding-agent-skills/skills/writing-agent-skills/SKILL.md).
Read it (or invoke `/coding-agent-skills:writing-agent-skills`) before adding or editing a skill.
Start any new skill by copying
[`SKILL.template.md`](plugins/coding-agent-skills/skills/writing-agent-skills/assets/SKILL.template.md).

## Quick reference
- A skill = `plugins/<plugin>/skills/<skill-name>/SKILL.md` (+ optional `references/`, `assets/`, `scripts/`).
- Frontmatter: `name` (== folder name, lowercase-hyphen, no `claude`/`anthropic`) and a third-person
  `description` (≤ 1024 chars) that states **what + when** and ends with `Triggers:`.
- Body sections, in order: `When to use` → `Do it` → `Why / learn` → `Common mistakes` →
  `Tailor to your environment` → `References` → (optional) `Scripts`. Keep the body under 500 lines.
- Evals go in `evals/<plugin>/<skill>.md` (positive trigger, near-miss, quality rubric) — never in SKILL.md.
- Validate with `bash scripts/validate.sh` and `claude plugin validate plugins/<plugin>`.

## Privacy
Never commit real client, bank, or account data. Sanitize to structural examples; keep raw
artifacts in `*.private.md` or `references/*.local.*` (git-ignored).

## Build status (waves)
All seven waves are complete: **83 skills across 13 plugins**, `validate.sh` clean.
- **Wave 0 — Foundation:** ✅ repo scaffold, authoring standard + template, `bank-reconciliation`
  exemplar, validator.
- **Wave 1 — Day-job core:** ✅ `cash-management-skills` (6), `oracle-otbi-skills` (5),
  accounting core, `agent-harness-config`.
- **Wave 2 — Adjacent domains + analysis base:** ✅ `banking-skills` (6), `finance-skills` (6),
  accounting remainder, BI core.
- **Wave 3 — Advanced analytics + improvement + agents:** ✅ statistics,
  `machine-learning-skills` (6), `continuous-improvement-skills` (6), coding/agents remainder.
- **Wave 4 — Fusion Financials + data tools:** ✅ `oracle-fusion-finance-skills` (6): GL/journals,
  FBDI, AP, AR, Cash Management module, period close; `data-tools-skills` (6): Excel automation,
  CSV wrangling, DuckDB, PDF extraction, REST API pulls, file hygiene.
- **Wave 5 — Advanced treasury & accounting ops:** ✅ `treasury-accounting-skills` (6): debt
  facilities & covenants, hedging & derivatives, investment policy compliance, accruals &
  prepaids, intercompany accounting, audit readiness & PBC.
- **Wave 6 — Sponsored projects AR:** ✅ `sponsored-projects-ar-skills` (11): master router,
  PPM-to-AR domain knowledge, unbilled/billed WIP reconciliation, KPIs & trend forecasts,
  reporting & recommendations, compliance risk & anomaly scanning, plus federal compliance —
  Uniform Guidance core, federal billing/cash management (LOC/PMS draws), effort reporting
  basics, cost allowability screening, and compliance/audit risk assessment.

Each plugin is independently installable and useful. Next: tailoring skills to your real
environment (Oracle OTBI reports, reconciliation process, chart of accounts, bank statement
formats) via each skill's `references/your-environment.md`.
