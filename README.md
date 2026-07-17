# Treasury Analyst Skills

A growing personal library of [Claude Code Agent Skills](https://code.claude.com/docs/en/skills)
that make Claude a sharper partner for cash management, Oracle Fusion Cloud OTBI reporting,
accounting, banking, finance, business-intelligence analytics, statistics, machine learning,
continuous improvement (Lean / TPS / Six Sigma / co-design), and coding / autonomous agents.

Every skill is built to one house standard: it **does the task step by step and teaches the
reasoning**, so you get the deliverable *and* get better at the work.

## Install

```
/plugin marketplace add blakereaganlaw-droid/claude_skills_2
/plugin install cash-management-skills@treasury-analyst-skills
/plugin install oracle-otbi-skills@treasury-analyst-skills
# ...install whichever plugins you want
```

Installed skills are namespaced, e.g. `cash-management-skills:bank-reconciliation`. Type
`/<plugin>:<skill>` to invoke one directly, or just describe your task and Claude will pick it up.

## Plugins

| Plugin | What it covers |
| --- | --- |
| `cash-management-skills` | Cash positioning, bank reconciliation, forecasting, liquidity, controls, netting |
| `oracle-otbi-skills` | Building OTBI reports in Oracle Fusion Cloud, with deep Cash Management coverage |
| `banking-skills` | Payment rails, account structures, statement formats, fees, connectivity, KYC/AML |
| `accounting-skills` | Double-entry, journals, chart of accounts, close, reconciliations, statements |
| `finance-skills` | Time value of money, working capital, ratios, short-term investing, FX, capital budgeting |
| `data-analytics-bi-skills` | SQL, EDA, cleaning, statistics, inference, dashboards, spreadsheet modeling |
| `machine-learning-skills` | Problem framing, time-series forecasting, supervised modeling, evaluation, features, anomalies |
| `continuous-improvement-skills` | VSM, root-cause analysis, DMAIC, standard work, A3, kaizen & co-design |
| `coding-agent-skills` | Python for analysts, Claude Code config, agent design, prompt engineering, git, skill authoring |

**Full catalog:** [`docs/SKILLS.md`](docs/SKILLS.md) lists every skill, what it does, and the
exact phrases that trigger it (regenerate with `python3 scripts/gen-catalog.py`).

Skills are built in waves (day-job first). See the build status and design notes in
[`CONTRIBUTING.md`](CONTRIBUTING.md).

## How it's built

- One repo that is both a **plugin marketplace** (`.claude-plugin/marketplace.json`) and the home
  for nine **plugins** under `plugins/`, mirroring Anthropic's own
  [`anthropics/skills`](https://github.com/anthropics/skills) layout.
- The authoring standard lives in the `coding-agent-skills:writing-agent-skills` skill; its
  template is `plugins/coding-agent-skills/skills/writing-agent-skills/assets/SKILL.template.md`.
- `bash scripts/validate.sh` lints every skill and manifest.

## Tailoring to your environment

Many skills leave a `references/your-environment.md` hook so they can fit your real Oracle OTBI
reports, reconciliation process, chart of accounts, and bank statement formats. **Real data is
never committed** — sanitize it, and keep raw artifacts in `*.private.md` / `references/*.local.*`
files, which `.gitignore` keeps out of git.
