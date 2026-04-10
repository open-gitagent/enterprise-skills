---
name: tax-compliance
description: >
  Corporate tax compliance management including income tax provision, sales and use tax, transfer pricing, and multi-jurisdictional filing requirements.
metadata:
  vertical: cfo-finance
  function: tax
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "IRC, IRS, State Revenue"
---

## Role
Produce defensible income tax provisions, file accurate multi-jurisdictional returns, implement Pillar Two and CAMT compliance, and maintain SOX 404 tax controls.

## Decision Lenses

| Lens | Focus | Key Rule |
|---|---|---|
| 1 — Provision Accuracy (ASC 740) | Current/deferred provision + UTP reserve | FIN 48 / ASC 740-10-25-6 two-step: more-likely-than-not threshold, then largest amount >50% likely sustained; enacted rates only — not proposed |
| 2 — Filing Compliance | Return accuracy and timeliness | IRC §6651(a): failure-to-file 5%/month max 25%; failure-to-pay 0.5%/month max 25%; IRC §6662 accuracy-related 20% |
| 3 — International (TP/Pillar Two/CbCR) | Transfer pricing, GloBE, country-by-country | OECD three-tier TP: Master File/Local File/CbCR; CbCR threshold $850M USD (Form 8975); Pillar Two 15% ETR floor per jurisdiction via IIR/UTPR/QDMTT |
| 4 — Controls & Governance (SOX 404) | ICFR effectiveness | SOX §404(a) management assessment; §404(b) auditor attestation (accelerated filers); PCAOB AS 2201 |

## Regulatory Framework

| Regulation | Citation | Key Requirement |
|---|---|---|
| Income Tax Accounting | FASB ASC 740 (Topic 740) | Recognize/measure all current/deferred tax assets, liabilities, uncertain positions |
| Uncertain Tax Positions | ASC 740-10-25 (FIN 48) | Two-step recognition/measurement |
| Enhanced Tax Disclosures | ASU 2023-09 | Prescriptive rate reconciliation; 8 mandatory categories; 5% quantitative threshold; effective PBEs annual periods after 12/15/2024 |
| Corporate Alternative Minimum Tax | IRC §§55, 56A, 59 | 15% min tax on AFSI; ≥$1B avg AFSI; controlled-group basis |
| Transfer Pricing | IRC §482; Treas. Reg. §1.482 | Arm's length standard |
| Transfer Pricing Penalties | IRC §6662(e)(h) | 20% substantial valuation misstatement; 40% gross valuation misstatement |
| Country-by-Country Reporting | IRC §6038; Treas. Reg. §1.6038-4 | Form 8975; U.S. MNE groups ≥$850M annual revenue |
| Int'l Information Returns | IRC §6038, §6038A | $10,000/return/year penalty; Forms 5471/5472/8865/8858 |
| OECD Pillar Two | GloBE Model Rules | 15% min ETR per jurisdiction; €750M revenue threshold |
| SOX Internal Controls | SOX §404; PCAOB AS 2201 | Management + auditor attestation of ICFR |
| SOX Certification | SOX §302 | CEO/CFO personal certification |
| Filing Penalties | IRC §6651(a) | FTF: 5%/month max 25%; FTP: 0.5%/month max 25% |
| Accuracy-Related Penalty | IRC §6662 | 20% of underpayment |
| Estimated Tax | IRC §6655 | Underpayment penalty; large corporation rules eliminate prior-year safe harbor after Q1 |
| BEPS TP Documentation | OECD BEPS Action 13 | Master File/Local File/CbCR three-tiered structure |

## Evaluation Metrics

| Metric | Green | Yellow | Red |
|---|---|---|---|
| Cash ETR (5-yr avg) | >20% | 15-20% | <15% (Pillar Two/CAMT scrutiny) |
| Return-to-Provision | <2% of total provision | 2-5% | >5% (provision deficiency) |
| UTB reserve YoY growth | Stable/declining | +5-15% | >+15% without new positions |
| Filing timeliness | 100% on-time | 1-2 late | 3+ late or missed extensions |
| TP documentation | Contemporaneous all material | >80% documented | <80% or master/local file gaps |
| SOX 404 tax controls | No deficiencies | Significant deficiencies | Material weakness |
| Provision close cycle | ≤5 biz days after quarter close | 6-10 days | >10 days |
| Penalty exposure | $0 | <$100K cumulative | >$100K or recurrence |
| Pillar Two data readiness | Complete GloBE model operational | Partial gaps, manual workarounds | No systematic collection |
| ASU 2023-09 readiness | Template tested with sample data | Template drafted, data gaps | No preparation |

## Process

**Phase 1 — Tax Position Inventory & Risk Assessment (Ongoing)**
1. Maintain inventory of all tax positions across all jurisdictions (federal, state, local, foreign)
2. Apply ASC 740-10-25-6 two-step to each material position: >50% more-likely-than-not, then measure at largest amount >50% likely sustained
3. Assess TP positions against arm's length documentation; identify gaps
4. Map CAMT exposure: test $1B avg AFSI on controlled-group basis; compute tentative minimum tax vs. regular tax + BEAT
5. Evaluate Pillar Two: confirm €750M threshold; identify low-tax jurisdictions (<15% ETR); assess safe harbors (de minimis, simplified ETR, routine profits tests)

**Phase 2 — Quarterly Provision Process**
6. Compute AETR per ASC 740-270; apply to YTD ordinary income
7. Identify discrete items (stock compensation, enacted law changes, RTP adjustments)
8. Calculate DTA/DTL movements; test valuation allowance with positive and negative evidence
9. Update UTP reserves; evaluate new information (cases, audit activity, legislation)
10. Prepare rate reconciliation per ASU 2023-09: 8 mandatory categories; items exceeding 5% threshold disclosed individually by nature and jurisdiction

**Phase 3 — Annual Return Compliance**
11. Reconcile book-to-tax (Schedule M-1/M-3); capture all temporary and permanent differences
12. Compute return-to-provision true-ups; book adjustments
13. File federal, state, and international returns by statutory deadlines (including extensions)
14. File information returns: Form 8975 (CbCR), Forms 5471/5472/8865/8858, state apportionment schedules
15. Calculate and remit estimated tax payments quarterly; verify against IRC §6655 required annual amount

**Phase 4 — Disclosure & Reporting**
16. Prepare ASU 2023-09 disclosures: tabular rate reconciliation, disaggregated taxes paid by federal/state/foreign, jurisdiction-level detail above 5% threshold
17. Disclose UTB rollforward per ASC 740-10-50-15A: beginning balance, current/prior year changes, settlements, statute expirations
18. Disclose NOL and credit carryforward amounts with expiration dates
19. Review APB 23 assertion for permanently reinvested foreign earnings annually

**Phase 5 — Controls Testing & Documentation**
20. Execute SOX 404 tax controls testing: provision review, journal entry approval, reconciliation sign-offs, access controls in tax software
21. Remediate control deficiencies before year-end assessment
22. Document management's ICFR assessment for Form 10-K inclusion

## Glossary

| Term | Definition |
|---|---|
| AETR | Annual Estimated Effective Tax Rate; projected full-year ETR for ASC 740-270 interim-period tax expense |
| AFSI | Adjusted Financial Statement Income; GAAP/IFRS book income with statutory adjustments; CAMT tax base per IRC §56A |
| APB 23 Assertion | Management assertion that undistributed foreign earnings are permanently reinvested; relieves deferred tax liability on outside basis difference |
| CAMT | Corporate Alternative Minimum Tax; 15% on AFSI per IRC §55; applies to ≥$1B avg AFSI controlled groups |
| Cash ETR | Cash taxes paid ÷ pre-tax book income; strips deferred accruals |
| CbCR | Country-by-Country Report; BEPS Action 13; revenue/profit/tax/employees/assets by jurisdiction |
| DTA / DTL | Deferred Tax Asset / Deferred Tax Liability; future tax benefit or obligation from temporary differences |
| ETR | Effective Tax Rate; total income tax expense ÷ pre-tax book income |
| GloBE Income | Pillar Two computational base from financial accounting income with specific adjustments per jurisdiction |
| IIR | Income Inclusion Rule; Pillar Two parent jurisdiction collects top-up tax on low-taxed foreign subsidiary income |
| Intraperiod Tax Allocation | ASC 740-20: allocation of total tax among continuing ops, discontinued ops, OCI, and equity |
| MLTNT | More-Likely-Than-Not; >50% probability threshold for UTP recognition under ASC 740 |
| QDMTT | Qualified Domestic Minimum Top-Up Tax; source country's own 15% floor; first right to top-up tax |
| RTP | Return-to-Provision; adjustment when filed return differs from estimated provision; key quality metric |
| UTB / UTP | Uncertain Tax Benefit / Position; excluded from provision when MLTNT threshold not met |
| UTPR | Undertaxed Profits Rule; Pillar Two backstop allowing other countries to tax when related entities fall below 15% |
| Valuation Allowance | Reserve against DTA when more-likely-than-not that some/all DTA will not be realized; requires positive and negative evidence |

## Checklist

- [ ] Rate reconciliation ties to 21% federal statutory rate; no unexplained residual >1% of tax expense
- [ ] Deferred tax rollforward reconciles: opening balances from prior-year FS tie; all movements (P&L, OCI, equity, acquisitions) separately identified
- [ ] UTB inventory reviewed against current facts within past quarter (SOL status, audit activity, legislation)
- [ ] Valuation allowance analysis: positive and negative evidence listed, weighted, conclusion documented; three-year cumulative loss test addressed
- [ ] TP documentation contemporaneous: Master File, Local File, CbCR substantially drafted before return filing deadline per BEPS Action 13
- [ ] ASU 2023-09 disclosure template populated: 8 mandatory categories mapped; jurisdictions >5% threshold individually identified; taxes paid disaggregated
- [ ] CAMT applicability tested annually on controlled-group basis; Form 4626 complete with Notice 2025-49 adjustments if applicable
- [ ] Pillar Two impact assessed: jurisdiction ETRs computed per GloBE rules; safe harbor eligibility tested; data gaps documented
- [ ] All information returns filed: Forms 5471/5472/8865/8858/8975 tracked on compliance calendar with filing confirmations
- [ ] SOX 404 tax controls tested per COSO: provision review, JE approval, reconciliations, system access; no unremediated material weaknesses
- [ ] Estimated tax payments reconciled against IRC §6655 required annual payment; large corporation rules correctly applied
- [ ] Intercompany transaction pricing benchmarked against arm's length comparables; studies refreshed within 3-year cycle
- [ ] Enacted legislation analyzed for ASC 740 impact in period of enactment (not effective date)
- [ ] Stock compensation discrete items computed in quarter of vesting/exercise; not spread through AETR
- [ ] Audit reserve adequacy reviewed with external counsel; exposure ranges updated quarterly in UTB reserve

## References
FASB ASC 740; ASU 2023-09; IRC §§55/56A/59/482/6038/6038A/6651/6655/6662; SOX §302/§404; PCAOB AS 2201; OECD GloBE Model Rules; BEPS Action 13; Treas. Reg. §1.482/§1.6038-4; IRS Notice 2025-49; IRS Pub 2108-A (TIN Matching); KPMG; Deloitte; EY; PwC; Bloomberg Tax; Thomson Reuters
