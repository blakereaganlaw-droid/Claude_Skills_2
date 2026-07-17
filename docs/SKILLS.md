# Treasury Analyst Skills — trigger & capability catalog

Auto-generated from every skill's `SKILL.md` frontmatter by `scripts/gen-catalog.py`. **66 skills across 11 plugins.**

## How to trigger a skill

There are two ways every skill fires:

1. **Automatically** — just describe your task in plain language. Claude matches your request against each skill's description and **trigger phrases** (listed below) and loads the right one on its own. You don't need to name it.

2. **Manually** — type the slash command `/{plugin}:{skill}` (e.g. `/cash-management-skills:bank-reconciliation`) to invoke a specific skill on demand.

Ask **"what skills are available?"** any time to list them.

## Install

```
/plugin marketplace add blakereaganlaw-droid/claude_skills_2
/plugin install <plugin>@treasury-analyst-skills      # e.g. cash-management-skills@treasury-analyst-skills
```
Install only the plugins you want; each is independent. Skills are namespaced `<plugin>:<skill>` so they never collide.

## Plugins

- [`cash-management-skills`](#cash-management-skills) (6) — Treasury cash operations: cash positioning, bank reconciliation, forecasting, liquidity, controls, and intercompany netting.
- [`oracle-otbi-skills`](#oracle-otbi-skills) (5) — Build OTBI reports and analyses in Oracle Fusion Cloud, with deep Cash Management subject-area coverage.
- [`oracle-fusion-finance-skills`](#oracle-fusion-finance-skills) (6) — Functional Oracle Fusion Cloud Financials: GL and journals, FBDI data loading, AP invoice-to-pay, AR and collections, the Cash Management module, and period close.
- [`banking-skills`](#banking-skills) (6) — Payment rails, bank account structures, statement formats, bank-fee analysis, connectivity, and KYC/AML basics.
- [`accounting-skills`](#accounting-skills) (6) — Double-entry accounting, journal entries, chart of accounts, month-end close, reconciliations, and financial statements.
- [`finance-skills`](#finance-skills) (6) — Corporate and treasury finance: time value of money, working capital, ratios, short-term investing, FX risk, and capital budgeting.
- [`data-analytics-bi-skills`](#data-analytics-bi-skills) (7) — SQL, exploratory analysis, data cleaning, statistics, inference, dashboard design, and spreadsheet modeling for business intelligence.
- [`data-tools-skills`](#data-tools-skills) (6) — Practical data plumbing: Excel automation with Python, CSV/flat-file wrangling, DuckDB local analytics, PDF data extraction, REST API data pulls, and data-file hygiene.
- [`machine-learning-skills`](#machine-learning-skills) (6) — Framing ML problems, time-series forecasting, supervised modeling, evaluation, feature engineering, and anomaly detection.
- [`continuous-improvement-skills`](#continuous-improvement-skills) (6) — Lean, Toyota Production System, Six Sigma, and co-design: value-stream mapping, root-cause analysis, DMAIC, standard work, A3, and kaizen.
- [`coding-agent-skills`](#coding-agent-skills) (6) — Python for analysts, Claude Code harness config, autonomous agent design, prompt engineering, git/code review, and authoring Agent Skills.

## `cash-management-skills`

Treasury cash operations: cash positioning, bank reconciliation, forecasting, liquidity, controls, and intercompany netting.

Install: `/plugin install cash-management-skills@treasury-analyst-skills`

### `cash-management-skills:bank-reconciliation`

**Invoke:** `/cash-management-skills:bank-reconciliation` — or just describe the task.

**What it does:** Reconciles a bank statement to the ledger or system cash balance, matches transactions, classifies outstanding and in-transit items, and investigates breaks until the difference resolves to zero. Use when reconciling a bank account, chasing an unreconciled difference, reviewing someone's reconciliation, or setting up matching/tolerance rules.

**Triggers:** `bank reconciliation`, `recon`, `reconcile the bank`, `unreconciled`, `outstanding items`, `deposits in transit`, `outstanding checks`, `statement vs book`, `reconciling difference`, `break`

### `cash-management-skills:cash-forecasting`

**Invoke:** `/cash-management-skills:cash-forecasting` — or just describe the task.

**What it does:** Builds direct-method short- and medium-term cash forecasts — projecting receipts and disbursements from operational drivers (AR collections, AP runs, payroll, debt service, tax) — and measures forecast-vs-actual variance to improve accuracy. Use when projecting liquidity, building a rolling 13-week or monthly cash forecast, choosing the direct vs. indirect method, or reviewing forecast accuracy.

**Triggers:** `cash forecast`, `liquidity forecast`, `direct method`, `indirect method`, `rolling forecast`, `13-week forecast`, `forecast variance`, `forecast accuracy`, `receipts and disbursements`, `project cash flow`

### `cash-management-skills:cash-management-controls`

**Invoke:** `/cash-management-skills:cash-management-controls` — or just describe the task.

**What it does:** Designs and reviews controls over cash processes — segregation of duties, payment authorization and dual approval, positive pay and ACH filters, reconciliation as a detective control, bank mandate management, and business-email-compromise prevention — mapped to the control objectives of authorization, completeness, accuracy, and safeguarding. Use when designing or auditing cash controls, building a segregation-of-duties matrix, or responding to a payment-fraud risk.

**Triggers:** `cash controls`, `segregation of duties`, `SOD`, `dual approval`, `payment authorization`, `positive pay`, `ACH filter`, `payment fraud`, `BEC`, `business email compromise`, `audit trail`, `bank mandate`

### `cash-management-skills:cash-positioning`

**Invoke:** `/cash-management-skills:cash-positioning` — or just describe the task.

**What it does:** Builds and reads a daily cash position — opening, available, and projected closing balances across bank accounts, currencies, and entities — from actual cash flows (bank statement balances, AP payments, AR receipts, payroll) to drive funding, sweep, and investing decisions. Use when determining how much cash is available today, sizing a sweep, funding a disbursement account before a payment run, or building a cash position worksheet.

**Triggers:** `cash position`, `daily cash`, `available balance`, `cash worksheet`, `opening balance`, `closing balance`, `position the cash`, `sweep decision`, `how much cash today`, `funding decision`

### `cash-management-skills:intercompany-cash-netting`

**Invoke:** `/cash-management-skills:intercompany-cash-netting` — or just describe the task.

**What it does:** Designs and runs intercompany netting cycles and in-house-bank settlements to cut cross-entity payments, float, and FX conversions, and evaluates pooling structures (notional, physical/ZBA, POBO/COBO). Use when consolidating intercompany cash, running a bilateral or multilateral netting cycle, or assessing an in-house bank or cash-pooling structure.

**Triggers:** `netting`, `intercompany netting`, `netting cycle`, `bilateral netting`, `multilateral netting`, `in-house bank`, `cash pooling`, `notional pooling`, `physical pooling`, `POBO`, `COBO`, `settlement cycle`

### `cash-management-skills:liquidity-management`

**Invoke:** `/cash-management-skills:liquidity-management` — or just describe the task.

**What it does:** Assesses liquidity buffers and sets target/minimum balances, structures concentration and zero-balance sweeps, and decides how to deploy surplus cash or cover a deficit across accounts and entities. Use when setting target balances, designing sweeps or a concentration structure, sizing a liquidity buffer, or deciding what to do with surplus or short cash.

**Triggers:** `liquidity`, `target balance`, `minimum balance`, `concentration account`, `ZBA`, `cash sweep`, `liquidity buffer`, `surplus cash`, `idle cash`, `cover a shortfall`, `committed facility`

## `oracle-otbi-skills`

Build OTBI reports and analyses in Oracle Fusion Cloud, with deep Cash Management subject-area coverage.

Install: `/plugin install oracle-otbi-skills@treasury-analyst-skills`

### `oracle-otbi-skills:otbi-analysis-filters`

**Invoke:** `/oracle-otbi-skills:otbi-analysis-filters` — or just describe the task.

**What it does:** Scopes and parameterizes an OTBI analysis: builds filters and "is prompted" filters, column/named/dashboard prompts, presentation and repository variables, and column-formula CASE logic for aging or classification buckets. Use when adding filters to a report, making it interactive or prompt-driven, passing runtime parameters, or writing a CASE column for aging buckets and derived measures.

**Triggers:** `add a filter`, `is prompted`, `dashboard prompt`, `column prompt`, `named prompt`, `presentation variable`, `runtime parameter`, `prompt-driven report`, `aging buckets`, `CASE formula`, `bucket a column`, `as-of date prompt`

### `oracle-otbi-skills:otbi-cash-management-reports`

**Invoke:** `/oracle-otbi-skills:otbi-cash-management-reports` — or just describe the task.

**What it does:** Builds the common Oracle Cash Management OTBI reports — bank statement balances, cash-position snapshot, unreconciled/exception and aging analyses, reconciliation status summary, bank-charge and charge-tax breakdowns, and external cash transaction audits — each mapped to its correct Cash Management subject area, with the security duty role required and the reconciliation-status-is-an- attribute caveat. Use when reporting on Oracle Fusion Cash Management data in OTBI.

**Triggers:** `cash management report`, `bank statement balances report`, `cash position OTBI`, `unreconciled report`, `reconciliation status report`, `bank charges report`, `external cash transactions`, `OTBI cash report`, `unreconciled aging`

### `oracle-otbi-skills:otbi-report-building`

**Invoke:** `/oracle-otbi-skills:otbi-report-building` — or just describe the task.

**What it does:** Builds or edits an Oracle Transactional Business Intelligence (OTBI) analysis end to end in Oracle Fusion Cloud: pick one subject area, add columns and column formulas on the Criteria tab, set filters, assemble Results views into a compound layout, save under /Shared Folders/Custom, and surface it on a dashboard with a shared prompt. Use when creating, editing, or troubleshooting any OTBI report or analysis.

**Triggers:** `build an OTBI report`, `create an analysis`, `OTBI analysis`, `Reports and Analytics`, `Browse Catalog`, `criteria tab`, `compound layout`, `add a column formula`, `put an analysis on a dashboard`, `edit an OTBI report`

### `oracle-otbi-skills:otbi-report-scheduling-sharing`

**Invoke:** `/oracle-otbi-skills:otbi-report-scheduling-sharing` — or just describe the task.

**What it does:** Shares and distributes OTBI content through dashboards and catalog folder permissions, and flags OTBI's key limitation — no native scheduling, bursting, or pixel-perfect output — so scheduled, burst, or precisely formatted delivery is routed to BI Publisher instead. Use when sharing, scheduling, distributing, emailing, or setting permissions on an OTBI report or dashboard, or when deciding between OTBI and BI Publisher for delivery.

**Triggers:** `share an OTBI report`, `schedule a report`, `burst a report`, `email a report on a schedule`, `distribute a dashboard`, `catalog permissions`, `pixel-perfect report`, `BI Publisher vs OTBI`, `OTBI can't schedule`

### `oracle-otbi-skills:otbi-subject-area-selection`

**Invoke:** `/oracle-otbi-skills:otbi-subject-area-selection` — or just describe the task.

**What it does:** Chooses the right OTBI subject area and columns for a reporting question, explains fact vs. dimension folders and the one-subject-area-per-analysis limit, and gives cross-pillar workarounds (BI Publisher SQL, side-by-side dashboard analyses on a shared prompt, or FDI/OAC). Covers the four Oracle Cash Management subject areas and when to use each. Use when unsure which subject area or columns to query, or when a report seems to need two subject areas or two Fusion pillars.

**Triggers:** `which subject area`, `pick a subject area`, `what subject area for`, `cross-subject-area`, `join two subject areas`, `Cash Management subject area`, `single subject area limit`, `column not available`, `fact vs dimension folder`

## `oracle-fusion-finance-skills`

Functional Oracle Fusion Cloud Financials: GL and journals, FBDI data loading, AP invoice-to-pay, AR and collections, the Cash Management module, and period close.

Install: `/plugin install oracle-fusion-finance-skills@treasury-analyst-skills`

### `oracle-fusion-finance-skills:fusion-ap-invoice-to-pay`

**Invoke:** `/oracle-fusion-finance-skills:fusion-ap-invoice-to-pay` — or just describe the task.

**What it does:** Runs the Oracle Fusion Payables invoice-to-pay cycle — invoice entry and validation, PO matching (2/3/4-way), holds and their releases, approval workflow, accounting, and paying through Payment Process Requests (PPRs) that build payment files. Use when entering or fixing an AP invoice in Fusion, releasing holds, investigating why an invoice isn't paid, or running and troubleshooting a payment batch.

**Triggers:** `fusion AP`, `payables invoice`, `invoice hold`, `release hold`, `invoice validation`, `PO matching`, `three-way match`, `payment process request`, `PPR`, `payment batch`, `invoice not paid`, `pay run fusion`, `payables approval`

### `oracle-fusion-finance-skills:fusion-ar-and-collections`

**Invoke:** `/oracle-fusion-finance-skills:fusion-ar-and-collections` — or just describe the task.

**What it does:** Runs Oracle Fusion Receivables — creating and importing AR transactions (invoices, credit memos), applying receipts manually and through lockbox/automatch, keeping unapplied and on-account cash honest, and working aging and the Advanced Collections dunning/strategy cycle. Use when booking or fixing an AR transaction in Fusion, applying or troubleshooting receipts, reconciling unapplied cash, or setting up aging and collections follow-up.

**Triggers:** `fusion AR`, `receivables invoice`, `apply receipt`, `unapplied receipt`, `on-account`, `lockbox`, `autoapply`, `credit memo fusion`, `AR aging`, `collections fusion`, `dunning`, `receipt application`, `customer balance`

### `oracle-fusion-finance-skills:fusion-cash-management-module`

**Invoke:** `/oracle-fusion-finance-skills:fusion-cash-management-module` — or just describe the task.

**What it does:** Operates the Oracle Fusion Cash Management module — bank, branch, and account setup; loading and troubleshooting electronic bank statements (BAI2, camt.053); tuning automatic reconciliation matching rules and rule sets; handling external cash transactions; and reading the module's reconciliation statuses. Use when setting up bank accounts in Fusion, loading bank statements, configuring or debugging auto-reconciliation, or clearing unreconciled statement lines in the Fusion CE module.

**Triggers:** `fusion cash management`, `bank statement load`, `camt.053 fusion`, `BAI2 import`, `auto reconciliation fusion`, `matching rules`, `reconcile in fusion`, `external cash transaction`, `bank account setup fusion`, `unreconciled statement lines`

### `oracle-fusion-finance-skills:fusion-fbdi-data-loading`

**Invoke:** `/oracle-fusion-finance-skills:fusion-fbdi-data-loading` — or just describe the task.

**What it does:** Loads data into Oracle Fusion Cloud with File-Based Data Import (FBDI) — picks the right import template, fills it without breaking its hidden formatting rules, generates and uploads the zip, runs the interface loader and the module import job, and works the error-correction loop until every row lands. Covers GL journal import (GL_INTERFACE) in depth. Use when bulk-loading journals, invoices, or other records into Fusion, or when an FBDI load errors out.

**Triggers:** `FBDI`, `file-based data import`, `journal import`, `GL_INTERFACE`, `import journals`, `load data into fusion`, `FBDI template`, `interface loader`, `ESS import job`, `correct import errors`, `bulk load fusion`

### `oracle-fusion-finance-skills:fusion-gl-and-journals`

**Invoke:** `/oracle-fusion-finance-skills:fusion-gl-and-journals` — or just describe the task.

**What it does:** Works General Ledger in Oracle Fusion Cloud — reads the ledger and chart-of-accounts structure (segments, value sets, hierarchies, cross-validation rules), creates manual and spreadsheet (ADFdi) journals, routes them through approval, posts them, and troubleshoots unposted or rejected journals. Use when entering or fixing a journal in Fusion GL, explaining a ledger/COA setup, or diagnosing why a journal won't post.

**Triggers:** `fusion journal`, `GL journal entry`, `create journal in fusion`, `ADFdi journal`, `spreadsheet journal`, `journal approval`, `post journal`, `journal won't post`, `cross-validation rule`, `chart of accounts segments`, `fusion ledger`

### `oracle-fusion-finance-skills:fusion-period-close`

**Invoke:** `/oracle-fusion-finance-skills:fusion-period-close` — or just describe the task.

**What it does:** Drives period close in Oracle Fusion Cloud — the subledger-to-GL close sequence (AP, AR, FA, projects, then GL), period statuses per module, exception sweeps (unaccounted transactions, stuck interface rows), subledger-to-GL reconciliation, and the Close Monitor/close calendar. Use when closing a period in Fusion, deciding the close order, chasing why a period won't close, or reconciling a subledger to its GL control account at close.

**Triggers:** `period close fusion`, `close the period`, `period status`, `can't close period`, `close AP period`, `sweep unaccounted`, `subledger close`, `close monitor`, `period end fusion`, `exceptions preventing close`

## `banking-skills`

Payment rails, bank account structures, statement formats, bank-fee analysis, connectivity, and KYC/AML basics.

Install: `/plugin install banking-skills@treasury-analyst-skills`

### `banking-skills:bank-account-structure`

**Invoke:** `/banking-skills:bank-account-structure` — or just describe the task.

**What it does:** Designs bank account hierarchies and automated sweep structures — concentration/header accounts, zero-balance (ZBA) and target-balance sub-accounts, and physical vs notional cash pooling — and rationalizes account counts to cut idle cash, fees, and risk. Use when structuring, opening, or rationalizing bank accounts, or designing sweeps or cash pooling.

**Triggers:** `bank account structure`, `account hierarchy`, `ZBA`, `zero balance account`, `concentration account`, `target balance`, `sweeps`, `cash pooling`, `notional pooling`, `account rationalization`, `BAM`, `bank account management`

### `banking-skills:bank-connectivity`

**Invoke:** `/banking-skills:bank-connectivity` — or just describe the task.

**What it does:** Reasons about the channels that connect an ERP or TMS to banks — host-to-host SFTP, SWIFT (Alliance, service bureau, SCORE), bank APIs / open banking, and single-bank portals — weighing cost, effort, resilience, and standardization, and covering file security (PGP, SSH keys). Use when integrating with a bank, choosing a connectivity channel, or securing bank file transfer.

**Triggers:** `host-to-host`, `H2H`, `SFTP`, `SWIFT connectivity`, `service bureau`, `SCORE`, `Alliance Lite`, `bank API`, `open banking`, `ERP to bank`, `TMS to bank`, `bank portal`, `PGP`, `connectivity channel`

### `banking-skills:bank-fee-analysis`

**Invoke:** `/banking-skills:bank-fee-analysis` — or just describe the task.

**What it does:** Analyzes bank fees from account-analysis statements — decoding AFP Service Codes, EDI 822 and ISO 20022 camt.086 billing files, and the earnings-credit-rate (ECR) offset against compensating balances — to review, benchmark, and reduce bank charges. Use when reviewing bank fees, reading an account analysis statement, or preparing a fee negotiation.

**Triggers:** `bank fees`, `account analysis`, `account analysis statement`, `AFP service codes`, `EDI 822`, `camt.086`, `bank services billing`, `earnings credit rate`, `ECR`, `compensating balance`, `fee reduction`, `bank billing`

### `banking-skills:bank-statement-parsing`

**Invoke:** `/banking-skills:bank-statement-parsing` — or just describe the task.

**What it does:** Normalizes bank statement files — BAI2, SWIFT MT940/MT942, ISO 20022 CAMT.053/CAMT.052, and CSV — into one reconciliation-ready schema (date, amount, direction, reference, description, balance), handling each format's balance and transaction codes and sign conventions. Use when ingesting, mapping, or troubleshooting a bank statement file before positioning or reconciliation.

**Triggers:** `BAI2`, `MT940`, `MT942`, `CAMT.053`, `CAMT.052`, `bank file`, `statement import`, `parse statement`, `transaction code`, `balance code`, `normalize statement`, `prior-day vs intraday`

### `banking-skills:kyc-aml-basics`

**Invoke:** `/banking-skills:kyc-aml-basics` — or just describe the task.

**What it does:** Explains and applies KYC / CDD / EDD, beneficial-ownership (UBO) identification, sanctions and OFAC/SDN screening, AML red flags, transaction monitoring, and SARs when onboarding or transacting with a counterparty — educational fundamentals, not legal advice. Use when onboarding a counterparty, screening a payment, or understanding an AML/KYC control.

**Triggers:** `KYC`, `CDD`, `EDD`, `AML`, `know your customer`, `customer due diligence`, `beneficial ownership`, `UBO`, `sanctions screening`, `OFAC`, `SDN`, `PEP`, `red flags`, `SAR`, `transaction monitoring`, `correspondent banking risk`

### `banking-skills:payment-rails`

**Invoke:** `/banking-skills:payment-rails` — or just describe the task.

**What it does:** Compares and selects payment methods — ACH (including Same Day ACH), Fedwire, CHIPS, RTP, FedNow, SWIFT cross-border, and checks — by cost, speed, settlement finality, reversibility, amount limits, and cutoff times, and explains how a given rail works. Use when deciding how to move money, funding a payment, or explaining the difference between rails.

**Triggers:** `ACH`, `wire`, `Fedwire`, `CHIPS`, `RTP`, `FedNow`, `SWIFT`, `MT103`, `pacs.008`, `payment rail`, `same-day ACH`, `payment method`, `how to send money`, `wire vs ACH`, `real-time payment`, `cross-border payment`

## `accounting-skills`

Double-entry accounting, journal entries, chart of accounts, month-end close, reconciliations, and financial statements.

Install: `/plugin install accounting-skills@treasury-analyst-skills`

### `accounting-skills:account-reconciliations`

**Invoke:** `/accounting-skills:account-reconciliations` — or just describe the task.

**What it does:** Performs balance-sheet account reconciliations (not bank recs) — prepaids, accruals, fixed assets, intercompany, and other GL accounts — proving each balance against independent support with a supporting schedule, classified and aged reconciling items, roll-forwards, and risk-ranking. Use when reconciling a GL balance-sheet account, building a supporting schedule, or reviewing a reconciliation.

**Triggers:** `account reconciliation`, `balance sheet reconciliation`, `GL rec`, `reconciling items`, `supporting schedule`, `roll-forward`, `risk-ranking accounts`, `prepaid schedule`, `accrual reconciliation`

### `accounting-skills:chart-of-accounts-design`

**Invoke:** `/accounting-skills:chart-of-accounts-design` — or just describe the task.

**What it does:** Designs, extends, and interprets a chart of accounts and its segments — entity/company, cost center, natural account, and others — with parent/child hierarchies and rollups for reporting. Use when designing or restructuring a COA, adding or mapping accounts, defining segments, or making sense of an existing account structure.

**Triggers:** `chart of accounts`, `COA`, `account segments`, `accounting flexfield`, `natural account`, `cost center`, `account hierarchy`, `rollup`, `account mapping`, `new account request`

### `accounting-skills:double-entry-fundamentals`

**Invoke:** `/accounting-skills:double-entry-fundamentals` — or just describe the task.

**What it does:** Applies the accounting equation, debit/credit rules, normal balances, T-accounts, and the accounting cycle to record a transaction correctly and prove the books balance. Use when unsure how to book a transaction, which side is the debit and which the credit, what an account's normal balance is, or how the accounting cycle flows from journal to ledger to trial balance to statements.

**Triggers:** `double entry`, `debit`, `credit`, `accounting equation`, `normal balance`, `T-account`, `trial balance`, `accounting cycle`, `assets liabilities equity`

### `accounting-skills:financial-statements`

**Invoke:** `/accounting-skills:financial-statements` — or just describe the task.

**What it does:** Reads and builds the three core financial statements — balance sheet, income statement, and cash flow statement (direct and indirect) — and uses how they articulate to tie them out. Use when analyzing, preparing, or tying out the statements, converting accrual results to cash, or building a cash flow statement by the indirect method starting from net income.

**Triggers:** `financial statements`, `balance sheet`, `income statement`, `P&L`, `cash flow statement`, `statement of cash flows`, `indirect method`, `accrual vs cash`, `articulation`, `tie out`

### `accounting-skills:journal-entries`

**Invoke:** `/accounting-skills:journal-entries` — or just describe the task.

**What it does:** Drafts and reviews journal entries — standard, accrual, deferral, reversing, reclassifying, and adjusting — keeping debits equal to credits and every line on its correct normal balance, with a clear memo and support. Use when creating, booking, or reviewing a journal entry, recording an accrual or deferral, or setting up a reversing entry.

**Triggers:** `journal entry`, `JE`, `book an entry`, `accrual`, `deferral`, `reversing entry`, `reclass`, `reclassifying entry`, `adjusting entry`, `debit and credit`, `top-side entry`

### `accounting-skills:month-end-close`

**Invoke:** `/accounting-skills:month-end-close` — or just describe the task.

**What it does:** Runs a structured month-end close — cutoff, accruals, subledger-to-GL tie-outs, reconciliations, intercompany, and flux/variance review — tracked on a close checklist with owners and a close calendar. Use when closing the books, building a close calendar or checklist, sequencing close tasks, or reviewing close status.

**Triggers:** `month-end close`, `period close`, `period end`, `close checklist`, `close calendar`, `cutoff`, `flux analysis`, `variance review`, `soft close`, `hard close`

## `finance-skills`

Corporate and treasury finance: time value of money, working capital, ratios, short-term investing, FX risk, and capital budgeting.

Install: `/plugin install finance-skills@treasury-analyst-skills`

### `finance-skills:capital-budgeting`

**Invoke:** `/finance-skills:capital-budgeting` — or just describe the task.

**What it does:** Evaluates capital projects with NPV, IRR, payback, discounted payback, and the profitability index, built on incremental after-tax free cash flows, and explains which rule governs when they conflict and why NPV is primary. Use when evaluating an investment or capital project, a buy-versus-build or equipment-replacement decision, or when ranking competing or mutually exclusive projects under a budget.

**Triggers:** `capital budgeting`, `project evaluation`, `NPV`, `IRR`, `payback period`, `discounted payback`, `profitability index`, `incremental cash flow`, `hurdle rate`, `mutually exclusive projects`, `capital rationing`

### `finance-skills:financial-ratios`

**Invoke:** `/finance-skills:financial-ratios` — or just describe the task.

**What it does:** Computes and interprets liquidity, leverage, profitability, and efficiency ratios — current and quick ratios, debt-to-equity, interest coverage, gross/operating/net margins, ROA, ROE, asset and inventory turnover — and decomposes ROE with DuPont, always read against a benchmark or trend. Use when analyzing a company's ratios or financial health, or when explaining what is driving its return on equity.

**Triggers:** `financial ratios`, `current ratio`, `quick ratio`, `debt to equity`, `interest coverage`, `ROE`, `ROA`, `gross margin`, `operating margin`, `net margin`, `DuPont`, `asset turnover`, `inventory turnover`, `receivables turnover`, `financial health`

### `finance-skills:fx-risk-basics`

**Invoke:** `/finance-skills:fx-risk-basics` — or just describe the task.

**What it does:** Identifies transaction, translation, and economic foreign-exchange exposure and applies basic hedges — forward contracts, natural or operational hedging, and netting exposures before hedging externally. Use when handling multi-currency exposure, deciding whether or how to hedge a foreign-currency cash flow, distinguishing the three types of FX risk, or reading spot/forward quotes.

**Triggers:** `FX risk`, `foreign exchange risk`, `currency exposure`, `hedging`, `forward contract`, `transaction exposure`, `translation exposure`, `economic exposure`, `natural hedge`, `hedge ratio`, `currency netting`

### `finance-skills:short-term-investments`

**Invoke:** `/finance-skills:short-term-investments` — or just describe the task.

**What it does:** Evaluates money-market instruments — T-bills, commercial paper, CDs, repos, and money-market funds — and builds an approach for investing surplus operating cash under a safety-then-liquidity-then- yield priority, including yield-basis conversions, an investment policy statement, and maturity laddering. Use when investing surplus or idle cash, comparing money-market instruments, converting between discount and bond-equivalent yields, or setting a short-term investment policy.

**Triggers:** `short-term investment`, `money market`, `T-bills`, `commercial paper`, `CDs`, `repo`, `money market fund`, `investment policy statement`, `laddering`, `surplus cash`, `discount yield`, `bond-equivalent yield`

### `finance-skills:time-value-of-money`

**Invoke:** `/finance-skills:time-value-of-money` — or just describe the task.

**What it does:** Applies present value, future value, discounting, and compounding to value cash flows over time, and computes annuities, perpetuities, NPV, and IRR — including IRR's known pitfalls (multiple or no solution, scale, and reinvestment assumptions). Use when valuing future cash flows, computing PV, FV, NPV, or IRR, choosing a discount rate, or comparing amounts that fall on different dates.

**Triggers:** `time value of money`, `present value`, `future value`, `discounting`, `compounding`, `NPV`, `IRR`, `annuity`, `perpetuity`, `discount rate`, `effective annual rate`, `EAR`, `opportunity cost of capital`

### `finance-skills:working-capital-management`

**Invoke:** `/finance-skills:working-capital-management` — or just describe the task.

**What it does:** Analyzes days sales outstanding (DSO), days payable outstanding (DPO), days inventory outstanding (DIO), and the cash conversion cycle (CCC = DSO + DIO − DPO) to release cash tied up in operations, and weighs the levers and trade-offs for shortening it. Use when analyzing or improving working capital, the operating cycle, or the cash conversion cycle, or when quantifying cash freed by faster collections, leaner inventory, or longer payment terms.

**Triggers:** `working capital`, `cash conversion cycle`, `CCC`, `DSO`, `DPO`, `DIO`, `days sales outstanding`, `days payable outstanding`, `days inventory outstanding`, `receivables`, `payables`, `inventory days`, `operating cycle`

## `data-analytics-bi-skills`

SQL, exploratory analysis, data cleaning, statistics, inference, dashboard design, and spreadsheet modeling for business intelligence.

Install: `/plugin install data-analytics-bi-skills@treasury-analyst-skills`

### `data-analytics-bi-skills:dashboard-design`

**Invoke:** `/data-analytics-bi-skills:dashboard-design` — or just describe the task.

**What it does:** Designs decision-driving BI dashboards and reports — defining robust KPIs (numerator, denominator, target, direction), choosing the right chart for the question being asked, and laying out for the audience and the decision. Use when building a report, dashboard, or scorecard, defining a KPI or metric, choosing a chart type, or cutting clutter from an existing view.

**Triggers:** `dashboard`, `KPI`, `metric`, `scorecard`, `chart choice`, `which chart`, `visualization`, `report layout`, `drill-down`, `report design`, `vanity metric`, `chart type`

### `data-analytics-bi-skills:data-cleaning`

**Invoke:** `/data-analytics-bi-skills:data-cleaning` — or just describe the task.

**What it does:** Cleans and reshapes messy data into an analysis-ready, tidy form — handling missing values, type and format coercion, deduplication, category standardization, and join hygiene — with validation at each step and a reproducible, non-destructive workflow. Use when preparing, wrangling, or fixing data before analysis or reporting.

**Triggers:** `data cleaning`, `data wrangling`, `data prep`, `data preparation`, `missing values`, `impute`, `deduplicate`, `remove duplicates`, `standardize`, `normalize categories`, `tidy data`, `reshape`, `pivot`, `join hygiene`, `fan-out`, `data quality fix`

### `data-analytics-bi-skills:descriptive-statistics`

**Invoke:** `/data-analytics-bi-skills:descriptive-statistics` — or just describe the task.

**What it does:** Summarizes a variable or dataset with the right measures of central tendency, dispersion, shape, and percentiles — and switches to robust measures (median, IQR, MAD) when outliers or skew would make the mean and standard deviation mislead. Use when describing or summarizing data, computing a "typical" value or a spread, or choosing which summary statistic to report before drawing conclusions.

**Triggers:** `descriptive statistics`, `summary statistics`, `mean`, `median`, `mode`, `average`, `standard deviation`, `variance`, `range`, `percentile`, `quartile`, `IQR`, `coefficient of variation`, `skewness`, `kurtosis`, `distribution shape`, `central tendency`, `spread`

### `data-analytics-bi-skills:exploratory-data-analysis`

**Invoke:** `/data-analytics-bi-skills:exploratory-data-analysis` — or just describe the task.

**What it does:** Profiles a dataset before any modeling or reporting — its shape, column types, grain, distributions, missingness, outliers, and relationships — so you understand and can trust the data before drawing conclusions from it. Use when first inspecting a new dataset, sizing up data quality, or deciding what needs fixing before analysis.

**Triggers:** `EDA`, `exploratory data analysis`, `data profiling`, `profile the data`, `first look at data`, `distribution`, `summary statistics`, `central tendency`, `spread`, `outliers`, `correlation`, `cross-tab`, `missing data`, `data quality check`, `get to know the data`

### `data-analytics-bi-skills:spreadsheet-modeling`

**Invoke:** `/data-analytics-bi-skills:spreadsheet-modeling` — or just describe the task.

**What it does:** Builds and audits transparent, reliable spreadsheet models (Excel/Google Sheets) — a clean input/calculation/output separation, consistent one-formula-per-row logic, named ranges, check cells and control totals, no constants hardcoded inside formulas, and sensitivity/what-if analysis. Use when building a financial or operational spreadsheet model, or reviewing/auditing one for errors.

**Triggers:** `Excel model`, `spreadsheet model`, `financial model`, `named ranges`, `check cell`, `control total`, `model audit`, `sensitivity analysis`, `what-if`, `data table`, `hardcoded formula`, `model review`

### `data-analytics-bi-skills:sql-for-analysts`

**Invoke:** `/data-analytics-bi-skills:sql-for-analysts` — or just describe the task.

**What it does:** Writes, reviews, and optimizes analytical SQL — joins, GROUP BY aggregation, window functions, CTEs, subqueries, and date/time handling — with a working sense of performance (grain, sargability, indexing). Use when turning a business question into a query for a report or analysis, adding window logic like running totals or rankings, or reviewing a query for correctness and speed.

**Triggers:** `SQL`, `query`, `write a query`, `join`, `GROUP BY`, `aggregate`, `window function`, `OVER`, `PARTITION BY`, `running total`, `moving average`, `rank`, `lag`, `lead`, `CTE`, `subquery`, `QUALIFY`, `slow query`, `optimize query`, `group by grain`

### `data-analytics-bi-skills:statistical-inference`

**Invoke:** `/data-analytics-bi-skills:statistical-inference` — or just describe the task.

**What it does:** Reasons from a sample to a population with confidence intervals and hypothesis tests (t-test, chi-square, ANOVA) — choosing the right test, checking its assumptions, and interpreting p-values, effect size, and Type I/II errors correctly rather than treating "significant" as a verdict. Use when testing a claim, comparing groups, running an A/B test, or quantifying the uncertainty of an estimate from a sample.

**Triggers:** `hypothesis test`, `p-value`, `statistical significance`, `confidence interval`, `t-test`, `chi-square`, `ANOVA`, `effect size`, `sampling`, `sampling distribution`, `type I error`, `type II error`, `statistical power`, `A/B test`, `significance level`, `null hypothesis`

## `data-tools-skills`

Practical data plumbing: Excel automation with Python, CSV/flat-file wrangling, DuckDB local analytics, PDF data extraction, REST API data pulls, and data-file hygiene.

Install: `/plugin install data-tools-skills@treasury-analyst-skills`

### `data-tools-skills:csv-and-flat-file-wrangling`

**Invoke:** `/data-tools-skills:csv-and-flat-file-wrangling` — or just describe the task.

**What it does:** Ingests real-world CSV and flat-file exports safely — detecting encodings and delimiters, surviving bank/ERP export quirks (BOMs, footers, quoted commas, leading-zero IDs, mixed date formats), validating the parsed schema, and merging files without silent row loss. Use when loading a CSV that parses wrong, combining exports from different systems, or hardening a recurring file feed.

**Triggers:** `csv parsing`, `delimiter`, `encoding error`, `utf-8 vs latin-1`, `BOM`, `pipe delimited`, `fixed width file`, `load csv pandas`, `merge csv files`, `bank export csv`, `leading zeros lost`, `csv broken columns`

### `data-tools-skills:data-file-hygiene`

**Invoke:** `/data-tools-skills:data-file-hygiene` — or just describe the task.

**What it does:** Keeps analysis files trustworthy and safe to share — naming and foldering conventions that sort correctly and explain themselves, raw/processed/output separation, lightweight versioning of data and scripts, and sanitizing sensitive data (account numbers, customer names, balances) before anything leaves your machine or enters git. Use when organizing a data project, naming recurring extract files, deciding what may be committed or emailed, or scrubbing a dataset for sharing.

**Triggers:** `file naming convention`, `organize data files`, `folder structure analysis`, `version data files`, `sanitize data`, `anonymize spreadsheet`, `remove sensitive data`, `what can I commit`, `data retention files`, `raw vs processed`

### `data-tools-skills:duckdb-local-analytics`

**Invoke:** `/data-tools-skills:duckdb-local-analytics` — or just describe the task.

**What it does:** Runs real SQL directly over local CSV, Parquet, and Excel files with DuckDB — no database server — for joins across files, aggregations on data too big for Excel, and repeatable analysis scripts, from the CLI or Python, persisting results back to files or a .duckdb database. Use when joining or aggregating local files with SQL, when a dataset chokes Excel/pandas memory, or when replacing a fragile chain of spreadsheet lookups with one query.

**Triggers:** `duckdb`, `query csv with sql`, `join csv files`, `sql on parquet`, `local sql`, `read_csv_auto`, `analyze large csv`, `sql without a database`, `parquet analytics`, `out of memory pandas`

### `data-tools-skills:excel-automation-python`

**Invoke:** `/data-tools-skills:excel-automation-python` — or just describe the task.

**What it does:** Reads, writes, and formats real Excel workbooks with Python — pandas for data in/out, openpyxl for formulas, multiple sheets, number formats, column widths, and styling — so recurring spreadsheet deliverables become a script instead of hand work. Use when automating an Excel report, converting data to a formatted .xlsx, reading a messy workbook into a DataFrame, or deciding between pandas and openpyxl.

**Triggers:** `excel automation`, `openpyxl`, `write xlsx`, `read excel python`, `pandas to_excel`, `format excel with python`, `excel report script`, `xlsxwriter`, `automate spreadsheet`, `excel formulas python`

### `data-tools-skills:pdf-data-extraction`

**Invoke:** `/data-tools-skills:pdf-data-extraction` — or just describe the task.

**What it does:** Extracts tables and text from PDFs into usable data — choosing between pdfplumber and camelot by PDF type, detecting scanned-vs-native pages, handling multi-page tables, bank-statement and invoice layouts, and validating extracted numbers against the document's own totals. Use when pulling transactions from a PDF bank statement, tabling data out of a PDF report or invoice, or when a PDF extraction comes out scrambled.

**Triggers:** `extract pdf table`, `pdf to excel`, `pdfplumber`, `camelot`, `parse bank statement pdf`, `pdf invoice data`, `scanned pdf`, `OCR pdf`, `pdf text extraction`, `table extraction python`

### `data-tools-skills:rest-api-data-pulls`

**Invoke:** `/data-tools-skills:rest-api-data-pulls` — or just describe the task.

**What it does:** Pulls data from REST APIs into files and DataFrames reliably — authentication patterns, query and field selection, pagination until exhaustion, retries with backoff for rate limits and transient failures, and flattening nested JSON — using Oracle Fusion Cloud REST APIs as the worked example. Use when extracting data from a REST API (Fusion or any SaaS), when a pull returns partial data, or when hardening a recurring API extract.

**Triggers:** `rest api pull`, `call api python`, `fusion rest api`, `pagination`, `api rate limit`, `429 retry`, `requests python`, `extract data from api`, `api to csv`, `json to dataframe`, `oauth token api`

## `machine-learning-skills`

Framing ML problems, time-series forecasting, supervised modeling, evaluation, feature engineering, and anomaly detection.

Install: `/plugin install machine-learning-skills@treasury-analyst-skills`

### `machine-learning-skills:anomaly-detection`

**Invoke:** `/machine-learning-skills:anomaly-detection` — or just describe the task.

**What it does:** Detects anomalies and outliers in transactions or time series using statistical and unsupervised methods — z-score and robust z (median/MAD), IQR, time-series residual anomalies, and multivariate models (isolation forest, local outlier factor, clustering) — with thresholds tuned to the precision/recall trade-off under scarce labels, and attention to alert fatigue. Use when flagging unusual activity such as reconciliation breaks, fee spikes, duplicate or out-of-pattern payments, or possible fraud.

**Triggers:** `anomaly detection`, `anomaly`, `outlier`, `outlier detection`, `unusual transaction`, `fraud detection`, `isolation forest`, `local outlier factor`, `LOF`, `z-score`, `novelty detection`, `unusual activity`

### `machine-learning-skills:feature-engineering`

**Invoke:** `/machine-learning-skills:feature-engineering` — or just describe the task.

**What it does:** Engineers, encodes, scales, and selects model features with transforms fit only on training data so nothing leaks from the future or the test set. Covers encoding categoricals (one-hot, target, frequency, ordinal), scaling and normalization, datetime and lag/rolling features, aggregations and interactions, missing-value handling as information, fit-on-train-only pipelines, and basic feature selection. Use when improving model inputs or preparing features for a model.

**Triggers:** `feature engineering`, `features`, `encoding`, `one-hot`, `target encoding`, `frequency encoding`, `scaling`, `normalization`, `standardize`, `datetime features`, `lag features`, `rolling features`, `feature selection`, `interactions`, `missing values`

### `machine-learning-skills:ml-project-framing`

**Invoke:** `/machine-learning-skills:ml-project-framing` — or just describe the task.

**What it does:** Turns a business problem into a well-posed machine-learning task: names the decision, defines the target and the unit of prediction, lists only features available at prediction time, picks an evaluation metric tied to the decision, sets a baseline to beat, and runs leakage and feasibility checks before any model is built. Use when starting an ML project, scoping a prediction, or sanity-checking whether ML even fits the problem.

**Triggers:** `ML problem`, `machine learning problem`, `framing`, `frame the problem`, `target variable`, `prediction task`, `unit of prediction`, `baseline model`, `is this an ML problem`, `does ML fit`, `feasibility`, `well-posed`

### `machine-learning-skills:model-evaluation`

**Invoke:** `/machine-learning-skills:model-evaluation` — or just describe the task.

**What it does:** Chooses the right metric and validation scheme for a model, guards against data leakage and overfitting, and compares every result against a baseline. Covers train/validation/test discipline, k-fold and time-series cross-validation, regression metrics (RMSE/MAE/R²) versus classification metrics (precision/recall/F1, ROC AUC vs PR AUC, calibration), confusion-matrix and threshold choice tied to error costs, and the common sources of leakage. Use when validating any model or picking a metric or decision threshold.

**Triggers:** `model evaluation`, `evaluate a model`, `cross-validation`, `k-fold`, `overfitting`, `underfitting`, `ROC AUC`, `precision recall`, `PR AUC`, `RMSE`, `R2`, `data leakage`, `train test split`, `confusion matrix`, `threshold`, `calibration`

### `machine-learning-skills:supervised-modeling`

**Invoke:** `/machine-learning-skills:supervised-modeling` — or just describe the task.

**What it does:** Builds and interprets supervised regression and classification models — starting with an interpretable linear or logistic baseline, then tree ensembles (random forest, gradient boosting / XGBoost / LightGBM) — with sensible defaults, regularization, class-imbalance handling, a leakage-safe fit/predict pipeline, and honest interpretation of coefficients and feature importance. Use when predicting a numeric or categorical outcome from features.

**Triggers:** `regression`, `classification`, `logistic regression`, `linear regression`, `random forest`, `gradient boosting`, `XGBoost`, `LightGBM`, `predict a category`, `predict a number`, `classifier`, `feature importance`, `coefficients`

### `machine-learning-skills:time-series-forecasting`

**Invoke:** `/machine-learning-skills:time-series-forecasting` — or just describe the task.

**What it does:** Builds and evaluates time-series forecasts with proper temporal validation — decomposition and stationarity checks, naive and seasonal-naive baselines first, classical models (ETS/Holt-Winters, ARIMA/SARIMA), and ML approaches with lagged and exogenous features — using time-ordered splits and rolling-origin backtesting, and metrics chosen for the series. Use when forecasting a series over time such as cash flow, account balances, transaction volumes, or collections.

**Triggers:** `time series`, `forecast`, `forecasting`, `ARIMA`, `SARIMA`, `ETS`, `Holt-Winters`, `exponential smoothing`, `seasonality`, `backtesting`, `rolling forecast`, `rolling origin`, `predict future values`, `trend and seasonality`

## `continuous-improvement-skills`

Lean, Toyota Production System, Six Sigma, and co-design: value-stream mapping, root-cause analysis, DMAIC, standard work, A3, and kaizen.

Install: `/plugin install continuous-improvement-skills@treasury-analyst-skills`

### `continuous-improvement-skills:a3-thinking`

**Invoke:** `/continuous-improvement-skills:a3-thinking` — or just describe the task.

**What it does:** Structures a problem, its analysis, and countermeasures on a single A3 page using the PDCA cycle, as a thinking and alignment tool rather than a form to fill. Use when proposing an improvement, telling a problem-solving story on one page, building consensus around a change, or running a PDCA cycle.

**Triggers:** `A3`, `A3 report`, `PDCA`, `plan do check act`, `problem solving`, `countermeasure`, `one-page proposal`

### `continuous-improvement-skills:dmaic-problem-solving`

**Invoke:** `/continuous-improvement-skills:dmaic-problem-solving` — or just describe the task.

**What it does:** Runs a Six Sigma DMAIC cycle — Define, Measure, Analyze, Improve, Control — to structure a data-driven improvement project that measures and confirms cause before changing anything. Use when structuring an improvement project, reducing defects or variation with rigor, or translating voice of the customer into CTQs and a charter.

**Triggers:** `DMAIC`, `six sigma`, `define measure analyze improve control`, `process improvement project`, `reduce defects`, `reduce variation`, `CTQ`

### `continuous-improvement-skills:kaizen-and-codesign`

**Invoke:** `/continuous-improvement-skills:kaizen-and-codesign` — or just describe the task.

**What it does:** Plans and facilitates kaizen events and co-design sessions so the people who do the work — and their downstream customers — design the improvement themselves, at the gemba, with rapid PDCA and captured standard work. Use when running an improvement workshop, a kaizen event, or a participatory/co-design session, or facilitating continuous improvement.

**Triggers:** `kaizen`, `kaizen event`, `co-design`, `participatory design`, `improvement workshop`, `gemba`, `facilitation`, `continuous improvement event`

### `continuous-improvement-skills:root-cause-analysis`

**Invoke:** `/continuous-improvement-skills:root-cause-analysis` — or just describe the task.

**What it does:** Finds the true cause of a recurring problem with 5 Whys, a fishbone/Ishikawa diagram across the 6M categories, and Pareto analysis, separating immediate containment from the root cause and verifying the cause before any countermeasure. Use when diagnosing a recurring problem, chasing a defect's cause, or a fix that never sticks.

**Triggers:** `root cause`, `5 whys`, `fishbone`, `Ishikawa`, `cause and effect`, `Pareto`, `RCA`, `why did this happen`, `recurring problem`

### `continuous-improvement-skills:standard-work`

**Invoke:** `/continuous-improvement-skills:standard-work` — or just describe the task.

**What it does:** Documents the current best-known method for a repeatable task as standard work (an SOP) — capturing sequence, timing, and the key points and reasons — with takt/cycle context and visual management, so the process is stable enough to improve. Use when documenting, standardizing, or stabilizing a process, or writing an SOP or work instruction.

**Triggers:** `standard work`, `standardized work`, `SOP`, `standard operating procedure`, `work instruction`, `standardize`, `visual management`

### `continuous-improvement-skills:value-stream-mapping`

**Invoke:** `/continuous-improvement-skills:value-stream-mapping` — or just describe the task.

**What it does:** Maps a process end to end in current and future state, quantifying cycle time, lead time, and value-added vs non-value-added time to expose waste and improve flow; scopes the effort first with SIPOC. Use when analyzing a whole process, mapping a value stream, drawing a current- or future-state map, measuring lead vs cycle time, or scoping a process with SIPOC.

**Triggers:** `value stream mapping`, `VSM`, `current state`, `future state`, `process map`, `SIPOC`, `lead time`, `cycle time`, `waste`, `flow`

## `coding-agent-skills`

Python for analysts, Claude Code harness config, autonomous agent design, prompt engineering, git/code review, and authoring Agent Skills.

Install: `/plugin install coding-agent-skills@treasury-analyst-skills`

### `coding-agent-skills:agent-harness-config`

**Invoke:** `/coding-agent-skills:agent-harness-config` — or just describe the task.

**What it does:** Configures the Claude Code harness — settings.json layers and precedence, tool permission rules (allow/ask/deny), automated hooks (SessionStart, PreToolUse, PostToolUse, Stop, and more), MCP servers, and environment variables. Use when setting up a repo for Claude Code, reducing permission prompts, automating a behavior that should run every time X happens, or wiring up an MCP server.

**Triggers:** `settings.json`, `permissions`, `allow this command`, `hooks`, `run automatically`, `whenever X do Y`, `MCP server`, `.mcp.json`, `configure Claude Code`, `harness config`

### `coding-agent-skills:agentic-workflow-design`

**Invoke:** `/coding-agent-skills:agentic-workflow-design` — or just describe the task.

**What it does:** Designs reliable autonomous and multi-step agent workflows — deciding agent vs deterministic script, decomposing a task into steps and subtasks, defining tools and their contracts, adding verification, guardrails, and checkpoints, handling failure and human-in-the-loop review, and evaluating the workflow against real cases. Use when building an agent, an automation pipeline, or a multi-step LLM workflow.

**Triggers:** `agent`, `autonomous agent`, `agentic workflow`, `tool use`, `orchestration`, `multi-step`, `pipeline`, `human in the loop`, `guardrails`

### `coding-agent-skills:git-and-code-review`

**Invoke:** `/coding-agent-skills:git-and-code-review` — or just describe the task.

**What it does:** Uses version control well and reviews changes constructively — branch-per-change, atomic commits with clear messages, the pull request flow, merge vs rebase (concept and when to use each), resolving merge conflicts calmly, and reading a diff for correctness and readability with useful feedback. Use when using git, opening or reviewing a pull request, resolving a merge conflict, or deciding how to structure a set of changes.

**Triggers:** `git`, `branch`, `commit`, `pull request`, `PR`, `merge conflict`, `code review`, `rebase`, `version control`

### `coding-agent-skills:prompt-engineering`

**Invoke:** `/coding-agent-skills:prompt-engineering` — or just describe the task.

**What it does:** Writes effective, provider-agnostic prompts and instructions for LLM agents — stating the task and success criteria, giving the right context and only that, few-shot examples, an explicit output format, decomposing complex asks, and iterating against real test cases. Use when crafting a prompt, instruction, or system message, or debugging a flaky prompt that gives inconsistent or wrong results.

**Triggers:** `prompt`, `prompt engineering`, `system prompt`, `instructions`, `few-shot`, `output format`, `prompt not working`, `improve a prompt`

### `coding-agent-skills:python-for-analysts`

**Invoke:** `/coding-agent-skills:python-for-analysts` — or just describe the task.

**What it does:** Writes clean, reproducible Python for data work and automation — virtual environments and pinned dependencies, script vs notebook structure, pandas essentials (load, select, filter, groupby, merge, write), small functions, and basic error handling and logging. Use when scripting an analysis, automating a repetitive task, cleaning up messy analysis code, or setting up a Python project so it runs the same way twice.

**Triggers:** `python`, `pandas`, `script`, `automate`, `virtualenv`, `notebook`, `dataframe`, `read csv`, `python for analysis`

### `coding-agent-skills:writing-agent-skills`

**Invoke:** `/coding-agent-skills:writing-agent-skills` — or just describe the task.

**What it does:** Authors and reviews Agent Skills (SKILL.md files) to this library's "do + teach" house standard and the open Agent Skills spec — correct frontmatter, discoverable descriptions, progressive disclosure, and privacy-safe tailoring. Use when creating a new skill, editing an existing one, reviewing a skill for quality, or setting up a new plugin in this repo.

**Triggers:** `write a skill`, `new skill`, `SKILL.md`, `authoring standard`, `skill description`, `add a skill`, `review a skill`, `do and teach`

