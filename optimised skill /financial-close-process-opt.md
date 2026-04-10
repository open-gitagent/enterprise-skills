---
name: financial-close-process
description: >
  Month-end and year-end financial close management including close calendars, reconciliations, journal entries, and close optimization.
metadata:
  vertical: cfo-finance
  function: accounting
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "GAAP, IFRS, SOX"
---

## Role
Manage end-to-end financial close processes—transaction recording, reconciliation, adjusting entries, consolidation, and GL lock—to produce auditable financial statements for all downstream consumers.

## Close Maturity Model

| Stage | Description | Days to Close |
|-------|-------------|--------------|
| 1 — Reactive | Tribal knowledge; no checklist; spreadsheet reconciliations; post-close adjustments >5%; errors discovered during audit | >10 days |
| 2 — Defined | Documented checklist with owners and due dates; mix of automated/manual reconciliations | 6–8 days |
| 3 — Optimized | Workflow software (BlackLine, FloQast, Numeric); automated transaction matching; real-time dashboards; post-close adjustments <2% | 4–5 days |
| 4 — Continuous | Daily reconciliation and anomaly detection; auto-generated recurring JEs; IC balances before consolidation; finance reallocates 40%+ of close time to analysis | 1–3 days |

## Speed-Accuracy Rule
Never sacrifice first-pass approval rate to hit a calendar target. A 6-day close at 95% first-pass approval > 4-day close at 70% (requiring 2 days rework).

## Regulatory Requirements

| Requirement | Key Obligation |
|-------------|---------------|
| SOX §302 | CEO/CFO certify effectiveness of disclosure controls and ICFR material changes in each 10-Q and 10-K filing |
| SOX §404(a) | Management ICFR assessment in annual 10-K for all SEC registrants |
| SOX §404(b) | External auditor ICFR attestation for accelerated filers (public float ≥$75M per 2020 amendments) |
| PCAOB AS 2201 | Auditors evaluate period-end financial reporting process; JEs, reconciliations, and management review in scope |
| PCAOB AS 1105 | Sufficient appropriate evidence for existence, completeness, valuation, presentation; well-organized PBC schedules support audit efficiency |
| ASC 606 | Five-step revenue recognition governs when/how revenue recorded at close; point-in-time vs. over-time selection |
| ASC 855 | Subsequent events: recognized (adjust FS) vs. non-recognized (disclose only); evaluated through issuance date (SEC) or available to be issued (non-SEC) |
| ASC 740 | Year-end: current + deferred tax provision, DTA realizability, uncertain tax positions |
| ASC 830 | Foreign currency: current rate method for subsidiary translation; affects CTA in equity |
| ASC 350/360 | Annual goodwill and long-lived asset impairment testing; typically performed during year-end close |
| SEC Filing Deadlines | Large Accelerated Filers (≥$700M float): 10-K 60 days, 10-Q 40 days; Accelerated ($75M–$700M): 10-K 60 days, 10-Q 40 days; Non-Accelerated (<$75M): 10-K 90 days, 10-Q 45 days |

## CFO/Controller KPI Dashboard (5–7 Metrics)

| KPI | Definition | Top-Quartile Target |
|-----|-----------|-------------------|
| Days to Close (DTC) | Business days from period-end to final close sign-off | ≤4 days (monthly) |
| On-Time Close Rate | % of closes completed by target date | ≥95% |
| Post-Close Adjustment Rate | Post-"final" entries as % of total JEs | <2% |
| Reconciliation Completion Rate | % of required reconciliations completed by cutoff | 100% by Day 3 |
| First-Pass Approval Rate | % of reconciliations and JEs approved without rework | ≥90% |

## Accounting Manager KPI Dashboard (8–12 Metrics)

| KPI | Definition | Target |
|-----|-----------|--------|
| Late Journal Entry Rate | % of JEs posted after designated cutoff day | <5% |
| Reconciliation Exception Rate | % of reconciliations with unresolved variances | <3% |
| Close Rework Rate | Items reopened/redone after submission | <5% |
| Intercompany Out-of-Balance Items | Unmatched IC pairs at consolidation start | 0 |
| Automated Reconciliation Rate | % of items matched automatically | >70% |
| Manual Journal Entry Volume | Count of manual (non-system-generated) JEs | Declining trend |

## Decision Hierarchy for Task Sequencing

| Priority | Task | Rule |
|----------|------|------|
| 1 | Cutoff enforcement | Hard deadlines for AP, expense reports, revenue inputs 2–3 business days before period-end |
| 2 | Sub-ledger close | AR, AP, inventory, fixed assets, payroll close before GL reconciliation begins |
| 3 | Adjusting entries | Accruals, prepaids, depreciation, amortization posted after sub-ledgers, before consolidation |
| 4 | Intercompany matching | All IC pairs reconciled and disputes resolved before elimination entries post; N entities = up to N×(N−1)/2 pairs |
| 5 | Consolidation & FX translation | Trial balances aggregated; foreign subsidiary translation (ASC 830); CTA calculated |
| 6 | Flux analysis & management review | Budget-to-actual and period-over-period; material variances investigated and documented |
| 7 | GL lock | Controller/CFO sign-off; hard close; no post-close entries without formal reopening approval |

## Process

### Phase 1: Pre-Close (Business Days −5 to 0)
1. Distribute updated close calendar with owners, due dates, dependencies, escalation paths
2. Confirm sub-ledger cutoff dates with AP, AR, payroll, inventory teams
3. Send deadline reminders to non-finance departments (expense reports, purchase requisitions, contracts)
4. Run preliminary trial balance; compare to prior period for obvious anomalies
5. Post recurring JEs that can go early (straight-line rent, license amortization, prepaid insurance)
6. Verify bank feed connectivity; resolve stale data integration issues

### Phase 2: Transaction Close (Business Days 1–2)
7. Post all remaining revenue entries per ASC 606 five-step model; verify performance obligation completion
8. Record final AP invoices; apply AP accrual for known invoices not yet received
9. Post payroll entries: bonuses, commissions, benefits liabilities
10. Update fixed asset register: additions, disposals, impairments, depreciation
11. Count and reconcile inventory; investigate shrinkage or valuation variances
12. Record bank transactions; clear suspense/clearing accounts

### Phase 3: Reconciliation & Adjustment (Business Days 2–4)
13. Reconcile all balance sheet accounts against supporting documentation; prioritize material accounts by risk: cash, AR, AP, debt, intercompany, accrued liabilities
14. Investigate and clear all reconciling items over materiality threshold; document disposition
15. Post adjusting JEs: accruals, deferrals, reclassifications, estimates, error corrections
16. Complete intercompany reconciliation: match all IC receivables to IC payables; flag and resolve timing differences
17. Post IC elimination entries (IC revenue/COGS, IC interest income/expense, IC dividends)

### Phase 4: Consolidation & Review (Business Days 4–6)
18. Aggregate entity-level trial balances into consolidated trial balance
19. Apply currency translation for foreign subsidiaries per ASC 830; calculate and post CTA to equity
20. Flux analysis: budget vs. actual, current vs. prior period, current vs. prior year; investigate variances exceeding materiality thresholds (typically 5–10% and fixed dollar amount)
21. Prepare variance commentary for material line items — specific causal analysis, not boilerplate
22. Controller reviews consolidated financials, reconciliation binders, and JE support
23. Close review meeting with CFO or Head of Finance

### Phase 5: Lock & Archive (Business Days 6–7)
24. Lock period in ERP/GL — hard close; no entries without formal reopening approval from controller/CFO
25. Publish final reporting package: IS, BS, CF, KPI dashboard, variance commentary
26. Upload to consolidation/reporting tools (Hyperion, OneStream, Workiva) if applicable
27. Archive all supporting documentation in centralized repository
28. Document lessons learned; update close checklist for next period

### Year-End Additions (2–4 Weeks)
- Goodwill and long-lived asset impairment testing (ASC 350, ASC 360)
- Income tax provision true-up and DTA assessment (ASC 740)
- Subsequent events evaluation through issuance date (ASC 855)
- Retained earnings and equity account rollforward
- PBC schedule preparation for external auditors
- Coordinate with external auditors on timeline, sampling, confirmation requests

## Glossary

| Term | Definition |
|------|-----------|
| Close Calendar | Structured timeline assigning every task to owner, deadline, and dependency; operational backbone of close management |
| Hard Close | Period locked in ERP/GL; no entries without formal controller reopening approval |
| Soft Close | Preliminary period-end producing estimated financials for internal reporting without full reconciliation |
| Reconciliation | Comparing two record sets (e.g., GL to bank, sub-ledger to GL); investigating and resolving differences |
| Flux Analysis | Comparison of current period to budget, prior period, or prior year; also called variance analysis |
| AJE (Adjusting Journal Entry) | Entry for accruals, deferrals, reclassifications, estimates, or error corrections required for GAAP |
| Post-Close Adjustment (PCA) | Journal entry recorded after close finalized; key quality metric |
| Intercompany Elimination | Entries removing intra-group transaction effects from consolidated financials |
| Trial Balance | Listing of all GL accounts and balances at period-end; starting artifact for reconciliation |
| PBC Schedule | Provided by Client schedules delivered to external auditors during year-end close |
| Suspense Account | Temporary holding account for unclassified transactions; must be cleared to zero at close |
| Cutoff | Point after which no further period transactions are accepted into GL; enforces complete attribution |
| Continuous Accounting | Reconciliation, monitoring, and validation performed throughout period, not batched at period-end |
| Material Weakness | ICFR deficiency with reasonable possibility of material misstatement not prevented/detected; must disclose per SOX §404 |
| Significant Deficiency | Less severe than MW but important enough to merit attention by those overseeing financial reporting |
| CTA (Cumulative Translation Adjustment) | Equity account capturing gains/losses from translating foreign subsidiary financials into reporting currency |
| Sub-Ledger | Detailed ledger supporting specific GL account (AR, AP, fixed assets, payroll); must close before GL |
| Reclass | Reclassification entry moving amounts between GL accounts to correct classification; does not affect net income |
| Close Cycle Time | Total elapsed time from period-end to final management sign-off |
| Workpaper | Supporting document evidencing reconciliation or close work; includes calculations, source references, preparer/reviewer sign-offs |
| Accrual | Entry to recognize expense or revenue incurred/earned but not yet recorded |
| Rollforward | Reconciliation showing opening balance + additions − reductions = ending balance; common for equity, allowances, reserves |
| Chart of Accounts (COA) | Structured list of all GL accounts; consistency across entities critical for clean consolidation |
| Close Management Software | BlackLine, FloQast, Numeric, Trintech — automate task tracking, reconciliation workflow, evidence management |

## Checklist

- [ ] Close calendar published with all tasks assigned to named owners, specific due dates, and dependency sequencing before period-end
- [ ] All sub-ledgers (AR, AP, inventory, fixed assets, payroll) closed and reconciled to GL before consolidated reconciliation begins
- [ ] 100% of material balance sheet accounts reconciled with documented support, preparer sign-off, and reviewer approval
- [ ] All suspense and clearing accounts cleared to zero (or below documented materiality threshold) before close finalized
- [ ] Intercompany balances fully matched across all entity pairs — zero out-of-balance items at consolidation start
- [ ] Flux analysis completed for all material P&L and balance sheet line items with specific (not boilerplate) variance explanations
- [ ] No journal entries with descriptions like "adjustment," "correction," or "plug" without detailed supporting documentation
- [ ] Segregation of duties enforced: different individuals prepare and approve all JEs and reconciliations
- [ ] Period hard-closed in ERP/GL after final sign-off; any post-close entries require documented controller/CFO approval
- [ ] Post-close adjustment rate tracked and reported; target <2% of total JEs
- [ ] Subsequent events evaluated through date financial statements are issued (SEC filers) or available to be issued (non-filers) per ASC 855
- [ ] Close retrospective conducted within one week; improvement items documented and assigned
- [ ] All close documentation archived in centralized, access-controlled repository
- [ ] Revenue recognition entries reviewed for ASC 606 five-step model compliance with evidence of completed performance obligations
- [ ] Year-end: PBC schedules delivered to external auditors per agreed timeline; tax provision completed per ASC 740

## References
PwC Finance Benchmarking Report 2023, Ledge Month-End Close Benchmarks 2025, Numeric Close Process Guide, FloQast SOX Compliance Guide, RSM Material Weakness Root Causes 2024, Deloitte Internal Controls Guide, PBMares SOX Audit Red Flags, KPMG Intelligent Close 2025, PCAOB AS 2201/AS 1105, ASC 606/740/830/855/350/360, SEC 10-K/10-Q filing deadlines, SOX §§302/404, BlackLine/FloQast/Numeric/Trintech platforms
