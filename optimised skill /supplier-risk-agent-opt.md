---
name: supplier-risk-agent
description: >
  Monitors vendor risk factors including financial stability tracking, geopolitical risk analysis, supply chain disruption alerts, and ESG risk scoring.
metadata:
  vertical: procurement
  function: risk-&-compliance
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "ISO 31000, COSO, FCPA"
---

## Role
Identify, score, mitigate, and continuously monitor supplier risks across financial, operational, cyber, geopolitical, compliance, and ESG dimensions using structured frameworks and real-time data.

## Risk Scoring Model

| Risk Dimension | Weight | Key Data Sources |
|---|---|---|
| Financial stability | 25% | D&B SER Rating (1-9), PAYDEX (1-100; 80+=prompt), D&B SSI, Altman Z-score, current ratio, debt-to-equity, 8-quarter revenue trend |
| Operational performance | 20% | OTIF %, lead time coefficient of variation, quality PPM (automotive: 5-50 PPM), order fulfillment accuracy |
| Cybersecurity posture | 15% | BitSight / SecurityScorecard rating, SOC 2 Type II currency, NIST SP 800-161 Rev 1 self-attestation, incident history |
| Geopolitical exposure | 15% | Country risk indices, sanctions lists, trade route dependency, regional conflict monitoring |
| Compliance & regulatory | 15% | UFLPA entity list screening, LkSG audit results, ISO certifications, REACH/RoHS status, CMRT |
| ESG & reputational | 10% | EcoVadis score (0-100), modern slavery disclosures, carbon emissions data, media monitoring |

## Risk Tier Thresholds

| Composite Score | Tier | Required Action |
|---|---|---|
| 1–5 | Negligible | Standard monitoring |
| 6–10 | Low | Annual review |
| 11–15 | Medium | Mitigation plan required within 90 days; procurement director review |
| 16–20 | High | Immediate mitigation action; executive escalation |
| 21–25 | Critical | Mandatory escalation; executive review within 48 hr; activate contingency sourcing |

## Per-Category Scoring Scale

| Score | Meaning |
|---|---|
| 1 | Minimal risk, robust controls in place |
| 2 | Low risk, minor gaps identified |
| 3 | Moderate risk, mitigation plan required within 90 days |
| 4 | High risk, immediate mitigation + executive escalation |
| 5 | Critical risk, suspend new orders pending remediation or activate alternate source |

## Kraljic Segmentation & Monitoring Cadence

| Quadrant | Profile | Review Cadence | Key Risk Actions |
|---|---|---|---|
| Strategic | High risk, high impact | Monthly | Dual-source development, executive governance, deep sub-tier mapping |
| Bottleneck | High risk, low impact | Quarterly | Safety stock, qualified alternates, financial health monitoring |
| Leverage | Low risk, high impact | Semiannual | Monitor geographic concentration; don't assume availability = low risk |
| Non-critical | Low risk, low impact | Annual | Basic thresholds at onboarding only; automate procurement |

## D&B Alert Thresholds

| Indicator | Alert Trigger | Meaning |
|---|---|---|
| D&B SER Rating | 8–9 | High failure/creditor-relief probability within 12 months |
| D&B SSI | Any 3+ point increase in one quarter; score 8–10 | 2× more likely to fail than average; investigate immediately |
| D&B PAYDEX | Below 80 | Late payment pattern emerging |
| D&B Failure Score | Bottom quintile | Flag for immediate investigation |

## Mitigation Strategies

| Risk Type | Mitigation |
|---|---|
| Single-source dependency | Dual/multi-source qualification; test orders to validate alternate lead time |
| Financial deterioration | Performance bonds, termination-for-convenience rights, inventory buffers |
| Geopolitical / route disruption | Contingency contracts, alternate sourcing, safety stock for long-lead components |
| Cybersecurity | SOC 2 Type II requirements; NIST SP 800-161 Rev 1 self-attestation; fourth-party posture assessment |
| UFLPA / forced labor compliance | Sub-tier screening; audit rights; fourth-party disclosure requirements in contracts |
| LkSG / CSDDD | Human rights officer designation; indirect supplier investigation protocol on substantiated knowledge |
| ESG | EcoVadis scoring requirements; CMRT submission; modern slavery statement |
| Concentration | HHI spend analysis; no single supplier >40% of any category spend |
| Supply chain disruption | Insurance (uptake 46.7% in 2024 per BCI); scenario planning with measured RTOs |

## Process

1. **Define Scope & Risk Appetite** — establish supplier categories, geographies, and tiers in scope; document risk tolerance thresholds (e.g., no single supplier >40% category spend; no critical-path component from single country); align with ERM framework and board risk appetite statements
2. **Build & Validate Supplier Inventory** — consolidate from ERP, P2P, and contract systems into single master record; assign D-U-N-S numbers; identify gaps (typically 15-30% of active suppliers missing); map parent-subsidiary relationships to detect hidden concentration
3. **Segment: Kraljic + Criticality Overlay** — apply Kraljic Matrix at category level; overlay criticality: Does a viable alternate exist? Revenue-at-risk if supplier fails? Requalification time? Criticality is not determined by spend alone
4. **Conduct Risk Identification** — catalog risks across all 6 dimensions; use: supplier self-assessment questionnaires, D&B/EcoVadis/BitSight third-party data feeds, on-site audits, OSINT monitoring; for Tier 2+: deploy Everstream Discover / Resilinc EventWatchAI or contractually require Tier 1 to disclose sub-tier relationships
5. **Score & Prioritize** — apply weighted scoring model; ensure inter-rater reliability by calibrating against historical data; generate composite scores; plot heat map; flag any supplier with D&B SSI 8-10 or Failure Score in bottom quintile immediately
6. **Develop Mitigation Strategies** — match mitigation to risk type and severity per table above; activate dual-sourcing, contractual safeguards, safety stock, supplier development, or insurance as appropriate
7. **Implement Continuous Monitoring** — configure real-time alerts for: financial deterioration (credit score drops, late payment patterns), sanctions list / UFLPA entity list additions, natural disaster proximity, cyber incident disclosures, management changes; monitor per Kraljic cadence (Strategic monthly, Bottleneck quarterly, Leverage semiannually, Non-critical annually)
8. **Report, Escalate & Reassess** — produce monthly executive dashboard (portfolio heat map, top-10 risk movers, concentration analysis by geography/supplier, mitigation status); escalate per risk tier table (Medium → procurement director; Critical → C-suite within 48 hr); conduct formal reassessment after material events (M&A, geopolitical shifts, large price swings, design changes); annual scenario planning: minimum 3 disruption scenarios (geopolitical, climate, cyber) with measured RTOs

## Glossary

| Term | Definition |
|---|---|
| BAFA | German Federal Office for Economic Affairs and Export Control; LkSG enforcement authority; conducted 486 audits in 2023; penalties up to 2% of global annual turnover |
| C-SCRM | Cybersecurity Supply Chain Risk Management; governed by NIST SP 800-161 Rev 1; integrates with NIST SP 800-53r5 SR control family (SR-1 through SR-12) |
| C-TPAT | Customs-Trade Partnership Against Terrorism; voluntary program for reduced inspections and expedited customs clearance |
| CMRT | Conflict Minerals Reporting Template (Responsible Minerals Initiative); discloses 3TG (tin, tantalum, tungsten, gold) sourcing per Dodd-Frank §1502 |
| Concentration risk | Exposure from disproportionate supply dependency on single supplier, geography, or route; measured using Herfindahl-Hirschman Index (HHI) |
| D&B PAYDEX | Monetarily-weighted payment history score (1-100); 80+ = prompt payment |
| D&B SER Rating | Supplier Evaluation Risk Rating (1-9 scale); predicts cessation of operations or creditor relief within 12 months |
| D&B SSI | Supplier Stability Indicator; probability of significant financial stress within 90 days; developed on D&B Data Cloud with segmented regional scorecards |
| Dual sourcing | Qualifying two approved suppliers for the same component to reduce single-source dependency; distinct from multi-sourcing (3+) |
| EcoVadis Score | Third-party sustainability rating (0-100) across environment, labor & human rights, ethics, sustainable procurement |
| EventWatchAI | Resilinc AI disruption monitoring; scans millions of data sources to identify and classify supply chain risk events in real time |
| Force majeure clause | Contract provision excusing performance during extraordinary events; must explicitly enumerate triggering events, notification timelines, mitigation obligations, and termination rights |
| Heat map | Visual 5×5 grid plotting risk likelihood vs. impact severity; used to prioritize and communicate portfolio risk to executives |
| Inherent risk | Risk level before any controls or mitigation measures are applied; assessment starting baseline |
| Kraljic Matrix | 2×2 framework: supply risk vs. profit impact → Strategic / Leverage / Bottleneck / Non-critical |
| N-th party risk | Risk from any entity in the extended supply network (beyond Tier 4) whose failure could cascade into operational impact |
| OTIF | On-Time In-Full; % of orders delivered by promised date with correct quantity and specification |
| PPM | Parts Per Million; defect rate; automotive standard 5-50 PPM depending on component criticality |
| Residual risk | Risk exposure remaining after mitigation controls applied; gap between inherent risk and countermeasure effectiveness |
| Right-to-audit clause | Contractual provision granting buyer the right to inspect supplier facilities, records, and processes |
| Sub-tier visibility | Ability to map and monitor beyond Tier 1; >50% of disruptions originate at Tier 2 or below; only 2% of companies have visibility beyond Tier 2 |
| UFLPA Entity List | CBP-maintained list of Xinjiang entities associated with forced labor; 144 entities as of 2025; rebuttable presumption of prohibited U.S. entry |
| Value-at-Risk (VaR) | Adapted from financial risk management; estimates maximum potential financial loss from supply chain disruptions within a given confidence interval and time horizon |

## Checklist

- [ ] Supplier master data reconciled across ERP, P2P, and contract systems with D-U-N-S number linkage; gap analysis completed for missing/duplicate records
- [ ] Kraljic Matrix segmentation at category level with criticality overlay; validated with cross-functional stakeholders within last 6 months
- [ ] Risk scoring model includes all 6 dimensions (financial, operational, cyber, geopolitical, compliance, ESG) with documented and justified weights
- [ ] D&B SER, SSI, and PAYDEX scores obtained for all strategic and bottleneck suppliers; automated alerts configured for score deterioration
- [ ] UFLPA entity list screening on all suppliers and disclosed sub-tier relationships; refresh cadence documented (minimum quarterly)
- [ ] Sub-tier mapping completed to at least Tier 2 for all critical-path components; Tier 3+ visibility for top 20% risk-scored suppliers
- [ ] Continuous monitoring platform deployed with real-time alerts (financial, geopolitical, cyber, natural disaster events)
- [ ] Escalation matrix documented with named owners, response SLAs, and decision authorities for each risk tier (Medium through Critical)
- [ ] Contractual risk transfer mechanisms verified for all strategic and bottleneck suppliers: audit rights, performance bonds, force majeure specificity, fourth-party disclosure requirements, termination-for-convenience
- [ ] Dual/multi-source qualification active for all sole-source components on critical production paths; alternate supplier lead time validated through test orders
- [ ] LkSG/CSDDD due diligence documentation maintained for indirect supplier investigation triggers; Human Rights Officer designated if in-scope
- [ ] Monthly executive risk dashboard produced: portfolio heat map, top-10 risk movers, concentration analysis by geography and supplier, mitigation plan status
- [ ] Annual scenario planning exercise: minimum 3 disruption scenarios (geopolitical, climate, cyber) with measured recovery time objectives
- [ ] Risk assessment inter-rater reliability calibration performed annually; scoring deviations between assessors documented and resolved

## References
ISO 31000:2018; ISO 28000:2022; ISO 9001:2026 (upcoming revision); NIST SP 800-161 Rev 1 (November 2024); NIST SP 800-53r5 SR control family (SR-1 through SR-12); UFLPA (144 entities, 2025); C-TPAT; German LkSG (1,000+ employees since January 2024); EU CSDDD; EU REACH/RoHS; IATF 16949; FDA 21 CFR Part 820; AS9100; FCPA; COSO; Dodd-Frank §1502; D&B; EcoVadis; Resilinc; Everstream Analytics; Interos; BitSight; SecurityScorecard; BCI Supply Chain Resilience Report 2024; Aon Global Risk Management Survey; BAFA; ISO AEO; Responsible Minerals Initiative
