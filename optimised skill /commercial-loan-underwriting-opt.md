---
name: commercial-loan-underwriting
description: >
  Commercial loan underwriting expertise including financial statement analysis, cash flow modeling, collateral evaluation, and credit structuring.
metadata:
  vertical: bfsi-banking
  function: credit
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "OCC, FDIC, Basel III"
---

## Role
Evaluate commercial credit requests using the 5 Cs framework to produce defensible, regulatory-compliant underwriting recommendations across C&I, CRE, construction, ABL, and leveraged lending.

## Decision Framework

### Repayment Source Hierarchy
| Priority | Source | Rule |
|----------|---------|------|
| 1 — Primary | Operating cash flow | Underwriting centers on this; must be demonstrated, not projected |
| 2 — Secondary | Collateral liquidation | Protects against loss severity; does not transform weak credit into acceptable one |
| 3 — Tertiary | Guarantor support | Requires independent global cash flow and personal financial statement analysis |

### Three-Metric CRE Test (all three must pass simultaneously)

| Metric | Formula | Standard | Community Bank Target |
|--------|---------|---------|----------------------|
| DSCR | NOI ÷ Annual Debt Service | Min 1.25× | 1.40×–1.50× |
| LTV | Loan ÷ Appraised Value | ≤80% commercial; ≤85% multifamily; ≤65% raw land | Per 12 CFR 34 Subpart D Appendix A |
| Debt Yield | NOI ÷ Loan Amount | Min 8%–10% | Leverage-neutral; unaffected by rate/amortization |

### C&I Credit Analysis

| Metric | Acceptable Range | Formula |
|--------|----------------|---------|
| FCCR | ≥1.20× | (EBITDA − Unfinanced CapEx − Cash Taxes − Distributions) ÷ (Total Debt Service + Capital Leases) |
| Leverage (Debt/EBITDA) | 2.0×–4.0× typical; >6.0× = leveraged lending |  |
| Current Ratio | >1.5 preferred | Current Assets ÷ Current Liabilities |
| Trend Analysis | 3-year minimum | Revenue trajectory, margin stability, working capital |

## Quantitative Scoring Matrix

| Metric | Strong | Acceptable | Marginal | Unacceptable |
|--------|--------|-----------|----------|-------------|
| DSCR (CRE) | ≥1.50× | 1.25×–1.49× | 1.10×–1.24× | <1.10× |
| FCCR (C&I) | ≥1.50× | 1.20×–1.49× | 1.00×–1.19× | <1.00× |
| Leverage (Debt/EBITDA) | <2.0× | 2.0×–3.5× | 3.5×–5.0× | >5.0× |
| LTV (Commercial) | <65% | 65%–75% | 75%–80% | >80% |
| Debt Yield | >12% | 9%–12% | 7%–9% | <7% |
| Current Ratio | >2.0 | 1.5–2.0 | 1.0–1.5 | <1.0 |

## Risk Rating Definitions (OCC Comptroller's Handbook)

| Grade | Definition |
|-------|-----------|
| Pass | No defined weaknesses; multiple sub-grades within Pass for internal differentiation |
| Special Mention | Potential weaknesses deserving close attention; if uncorrected, may result in deterioration |
| Substandard | Inadequately protected by current paying capacity or collateral; well-defined weakness exists |
| Doubtful | Full collection highly questionable and improbable based on existing conditions |
| Loss | Uncollectible; of such little value that continuance as a bankable asset not warranted |

## Regulatory Requirements

| Regulation / Guidance | Citation | Key Requirement |
|----------------------|----------|----------------|
| Real Estate Lending Standards | 12 CFR 34 Subpart D (OCC); 12 CFR 365 (FDIC) | Written RE lending policies with LTV limits, underwriting standards, exception tracking |
| Supervisory LTV Limits | Appendix A to 12 CFR 34 Subpart D | 65% raw land; 75% land development; 80% commercial/multifamily construction; 80% improved commercial; 85% multifamily residential |
| CRE Concentration Guidance | OCC Bulletin 2006-46 (71 FR 74580) | Construction/land dev ≥100% of capital triggers enhanced review; total CRE ≥300% of capital + 50% growth in 36 months triggers heightened scrutiny |
| Credit Risk Review Systems | OCC Bulletin 2020-50 | Independent credit risk review function required for rating validation |
| Refinance Risk | OCC Bulletin 2024-29 | Guidance on managing CRE loan maturities in higher rate environment |
| Rating Credit Risk | OCC Comptroller's Handbook Apr 2001 | Pass/Special Mention/Substandard/Doubtful/Loss; dual rating (borrower + facility) recommended |
| Safety & Soundness | 12 CFR 30 Appendix A (OCC); 12 CFR 364 Appendix A (FDIC) | Credit underwriting standards: documentation, analysis, collateral |
| CECL | FASB ASC 326 | Lifetime expected credit loss at origination; affects initial risk rating and provisioning |
| Appraisal Requirements | 12 CFR 34 Subpart C (OCC); 12 CFR 323 (FDIC) | FIRREA-compliant appraisals for RE transactions >$500,000 |
| Legal Lending Limits | 12 USC 84; 12 CFR 32 | Max 15% of unimpaired capital (unsecured); 25% with qualifying collateral |
| Insider Lending | Regulation O (12 CFR 215) | Prior board approval; terms no more favorable than comparable non-insider transactions |
| Flood Insurance | 42 USC 4012a; 12 CFR 22 | Mandatory for properties in Special Flood Hazard Areas |
| BSA/AML | 31 CFR 1020; 12 CFR 21 | CDD/KYC; beneficial ownership identification |
| OCC/FDIC Leveraged Lending Rescission | Dec 2025 | 2013 guidance rescinded; principles-based supervision; Federal Reserve still maintains 2013 definition for state member banks |

## Process

### Phase 1: Application Intake & Eligibility Screening
- Collect borrower/guarantor financials: 3 years tax returns, interim statements, PFS
- Verify legal entity structure, ownership chain, related-party relationships
- Confirm loan purpose aligns with lending policy and risk appetite
- Screen: BSA/AML, OFAC, Regulation O (12 CFR 215)

### Phase 2: Financial Spreading & Analysis
- Spread statements into standardized format (RMA or internal template)
- Calculate: DSCR, FCCR, leverage, liquidity, profitability margins
- Trend analysis across minimum 3-year period
- Reconcile tax returns to financial statements; investigate material discrepancies
- Global cash flow: consolidate all borrower entities and guarantors

### Phase 3: Collateral Evaluation
- Order FIRREA-compliant appraisal for transactions >$500,000 per 12 CFR 34 Subpart C
- Verify appraiser independence per OCC Bulletin 2010-42 and Interagency Appraisal Guidelines
- Calculate LTV against supervisory and internal policy limits
- Assess: location, condition, marketability, environmental risk (Phase I/II ESA)
- Non-RE collateral: liquidation (not going-concern) value; apply advance rates

### Phase 4: Risk Rating Assignment
- Assign dual risk rating: borrower risk + facility risk
- Map to regulatory classification per OCC Comptroller's Handbook
- Document rating rationale in narrative — a rating without narrative fails examiner scrutiny
- Validate against OCC grade definitions and migration patterns

### Phase 5: Credit Memorandum & Structuring
- Draft credit memo: borrower overview, risk score, terms, pricing, covenants, key financials, industry context, policy exceptions, recommendation
- Structure: amortization, maturity, rate type, guaranty requirements, collateral package
- Financial covenants: minimum DSCR, maximum leverage, minimum net worth
- Reporting covenants: annual audited financials, quarterly interims, tax returns, rent rolls (CRE), borrowing base certs (ABL)
- Document all policy exceptions with compensating factors

### Phase 6: Approval & Booking
- Route to appropriate authority by loan size and risk grade
- Credit committee or board approval for loans exceeding delegated authority
- Verify legal lending limit compliance (12 USC 84)
- Proper documentation: UCC filings, title insurance, flood determination

## Glossary

| Term | Definition |
|------|-----------|
| DSCR | Net Operating Income ÷ Annual Debt Service; primary CRE repayment metric; 1.25× minimum; 1.0× = breakeven |
| Global Cash Flow | Consolidation of all entities and individuals in borrowing relationship; prevents double-counting K-1 income |
| Debt Yield | NOI ÷ Loan Amount; leverage-neutral metric unaffected by interest rate or amortization |
| LTV | Loan ÷ Appraised Value; supervisory limits per Interagency Guidelines |
| Special Mention | OCC warning grade: potential weaknesses, not yet classified |
| Substandard | Regulatory classification: inadequately protected by paying capacity or collateral; well-defined weakness exists |
| FCCR | (EBITDA − Unfinanced CapEx − Cash Taxes − Distributions) ÷ (Total Debt Service + Capital Leases) |
| Concentration Risk | Portfolio exposure to common risk factor; OCC Bulletin 2006-46 defines CRE thresholds at 100%/300% of capital |
| Credit Memorandum | Formal analytical document presenting assessment, risk rating, deal structure, and recommendation |
| SNC | Shared National Credit; syndicated loan ≥$100M shared by ≥3 regulated institutions; annual interagency review |
| Leveraged Lending | Generally Debt/EBITDA >4.0×–6.0× (institution-defined post-2025 rescission); Federal Reserve still applies 2013 definition |
| Risk Rating Migration | Movement of credits between risk grades over time; tracked via transition matrices for CECL |
| Covenant Lite | Loan lacking financial maintenance covenants; repeatedly flagged in SNC reviews |
| Debt Service Reserve | Cash/LOC covering 6–12 months of debt service; required for construction loans and weaker credits |
| Owner-Occupied CRE | >50% space used by borrower's own business; excluded from CRE concentration calculations per OCC Bulletin 2006-46 |
| Advance Rate | % of collateral value lent against; typical: 80%–85% eligible A/R, 50%–65% inventory, 75%–80% equipment at OLV |
| Cap Rate | NOI ÷ Property Value; 100bp increase at 6% cap rate reduces value ~14% |
| Policy Exception | Approved deviation from lending policy; must document compensating factors and track aggregate exception rate |
| Nonaccrual | Interest recognition ceases when full repayment doubtful or 90+ days past due |
| UCA Cash Flow | Standardized C&I cash flow from net income adjusted for non-cash items, working capital, CapEx, debt service |

## Checklist

- [ ] Global cash flow completed — all entities and guarantors consolidated; K-1 income not double-counted
- [ ] DSCR calculated on both in-place income AND stressed basis (200bp rate increase, 10% NOI decline, or policy-specified stress)
- [ ] LTV verified against 12 CFR 34 Subpart D Appendix A supervisory limits; exceptions documented with compensating factors
- [ ] Risk rating supported by written narrative tying financial analysis to specific OCC grade definition
- [ ] Credit memo includes forward-looking industry analysis — not boilerplate recycled from prior memos
- [ ] Appraisal meets FIRREA requirements; appraiser independence verified; age appropriate for current market conditions
- [ ] CRE concentration impact assessed — loan's contribution to 100%/300% thresholds calculated and documented
- [ ] Flood determination obtained; if SFHA, evidence of adequate flood insurance documented before closing
- [ ] Regulation O screening completed; prior board approval obtained where required
- [ ] Covenant package includes measurable financial triggers with clearly defined testing periods and remedy provisions
- [ ] Legal lending limit calculated: total exposure (direct + indirect + contingent) within 12 USC 84 limits
- [ ] For participations: independent credit analysis performed — not reliance on lead bank's memo alone per OCC Bulletin 2020-50
- [ ] Environmental due diligence (Phase I ESA minimum) completed; RECs identified and addressed
- [ ] Tax return-to-financial statement reconciliation completed; material discrepancies investigated
- [ ] CECL implications assessed — initial risk rating and expected loss estimate documented for allowance methodology

## References
OCC Comptroller's Handbook: CRE Lending (Mar 2022), Rating Credit Risk (Apr 2001), Commercial Loans §206; OCC Bulletin 2006-46, OCC Bulletin 2024-29, OCC Bulletin 2020-50, 12 CFR 34 Subpart D, 2024 SNC Program Report, FDIC CRE/C&I Lending Resources, FDIC Consumer Compliance Highlights Mar 2024, OCC/FDIC Leveraged Lending Rescission Dec 2025, FASB ASC 326 (CECL)
