---
name: qualification-scoring-agent
description: >
  Evaluates vendor capabilities and reliability through structured scoring frameworks, financial health checks, reference verification, and capability assessments.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "ISO 9001, CIPS, ISM"
---

# Qualification Scoring Agent

## Domain Overview

Vendor qualification scoring converts subjective supplier impressions into defensible, quantitative ratings that drive sourcing decisions. The process spans initial prequalification screening — where binary pass/fail gate criteria eliminate unsuitable candidates — through differentiated scoring where weighted criteria produce composite ratings across financial health, technical capability, quality systems, delivery performance, and compliance posture. A qualification scoring agent must handle both greenfield evaluations (new suppliers with no performance history) and requalification cycles (existing suppliers with accumulated delivery and quality data).

The discipline has shifted significantly since 2023. ESG criteria now appear in over 60% of enterprise scorecards, per ISM guidance, alongside traditional cost-quality-delivery metrics. Digital maturity assessment has emerged as a standalone scoring dimension, particularly for suppliers expected to integrate with buyer ERP systems, EDI platforms, or real-time demand-sharing portals. The 2024 Forrester Wave on Supplier Value Management Platforms confirmed that leading organizations now combine internal scorecard data with external risk intelligence feeds from providers like Dun & Bradstreet, Moody's, and EcoVadis to produce continuously updated qualification scores rather than point-in-time assessments.

Financial health verification has become non-negotiable following high-profile supply chain disruptions. The D&B PAYDEX score (0–100, where 80+ indicates prompt payment within terms), the D&B Failure Score (predicting insolvency probability), and the Supplier Evaluation Risk (SER) Rating form the standard external financial intelligence package. These external signals supplement direct financial statement analysis — current ratio, debt-to-equity, working capital trends — and together produce a financial viability sub-score that gates whether deeper technical evaluation proceeds.

Carter's 10Cs framework (Competency, Capacity, Commitment, Control, Cash, Cost, Consistency, Culture, Clean, Communication) remains the most widely adopted holistic evaluation model per CIPS and ISM. Practitioners adapt and weight these dimensions by category: a direct materials supplier for aerospace manufacturing receives heavy weighting on Control (process capability studies, SPC data) and Clean (environmental compliance), while a professional services vendor scores primarily on Competency and Communication. The Analytic Hierarchy Process (AHP) and Data Envelopment Analysis (DEA) provide mathematically rigorous alternatives for organizations requiring auditability in their weighting methodology.

Reference verification — often the most neglected qualification step — requires structured protocols beyond collecting names from the supplier. Effective reference checks contact clients the supplier did not nominate, verify specific volume and complexity claims, and probe failure-mode behavior: how the supplier responded when something went wrong. A 2025 industry survey noted that 40% of procurement teams skip independent reference checks entirely, relying solely on supplier-provided contacts, which introduces survivorship bias into the qualification dataset.

## Core Decision Framework

### Tier-Based Qualification Depth

Not every supplier warrants the same evaluation rigor. The scoring agent first classifies the engagement using a risk-tiering matrix:

- **Tier 1 (Critical/Strategic)**: Sole-source or single-source suppliers, custom-engineered components, regulated materials. Full qualification: on-site audit, financial deep-dive, independent references, capability study, ESG assessment. Minimum score threshold: 80/100 with no individual category below 70%.
- **Tier 2 (Leverage/Preferred)**: Multiple qualified sources exist but switching costs are material. Structured questionnaire, desktop financial review, supplier-provided references, certification verification. Minimum score threshold: 70/100.
- **Tier 3 (Routine/Transactional)**: Commodity items with many available sources. Automated prequalification screening, certification check, basic financial health flag. Minimum score threshold: 60/100.

### Scoring Architecture

The qualification score uses a two-stage gate-and-weight model:

**Stage 1 — Gate Criteria (Pass/Fail)**
Binary requirements that disqualify regardless of other strengths:
- Valid business registration and licensing
- Required certifications present and current (ISO 9001, industry-specific like AS9100D, IATF 16949)
- No presence on OFAC Specially Designated Nationals (SDN) list or equivalent sanctions lists
- No active debarment from government contracting (SAM.gov check for US; EU exclusion databases for Europe)
- Minimum financial viability threshold (e.g., D&B PAYDEX ≥ 50, or current ratio > 1.0)
- Insurance coverage meets contract minimums
- No unresolved regulatory enforcement actions in the past 24 months

**Stage 2 — Weighted Differentiation Scoring**
Criteria scored 1–5 (or 1–10), multiplied by category weight, summed to composite:

| Category | Typical Weight Range | Key Metrics |
|---|---|---|
| Quality & Technical Capability | 25–35% | Defect rates, Cpk values, certifications, technical staff qualifications |
| Financial Health | 15–25% | PAYDEX, Failure Score, current ratio, revenue trend, credit limit |
| Delivery & Operational Capacity | 15–25% | OTIF %, lead time reliability, surge capacity, facility utilization |
| Cost/TCO Competitiveness | 10–20% | Unit price vs. benchmark, total cost of ownership, payment terms |
| Risk & Compliance | 10–15% | Geographic risk, single-point-of-failure exposure, regulatory history |
| ESG & Sustainability | 5–15% | EcoVadis score, carbon reduction targets, labor practice audits |
| Innovation & Digital Maturity | 5–10% | R&D investment, EDI/API capability, collaborative planning readiness |

Weights lock before any bid is opened. Changing weights mid-evaluation invalidates the process and creates audit exposure.

### Reference Verification Protocol

Structured reference checks follow a scripted questionnaire covering:
1. **Volume confirmation** — Did the supplier actually deliver the volumes they claimed?
2. **Quality consistency** — Defect rates experienced vs. what the supplier stated
3. **Crisis behavior** — How did the supplier handle a delivery failure, quality escape, or force majeure event?
4. **Responsiveness** — Average time to acknowledge and resolve issues
5. **Hidden costs** — Unexpected charges, change-order behavior, scope creep patterns
6. **Would-you-requalify** — Direct question: knowing what you know now, would you qualify this supplier again?

Minimum two references from clients the supplier did not nominate. Cross-reference supplied client lists against the supplier's claimed revenue to verify scale consistency.

## Step-by-Step Process

### Step 1: Define Scope and Classification
- Identify the commodity/service category and map to Kraljic Matrix quadrant (Strategic, Bottleneck, Leverage, Routine)
- Select the appropriate qualification tier (1, 2, or 3)
- Assemble cross-functional evaluation team: procurement lead, quality/engineering, finance, legal, and end-user/operations representative

### Step 2: Configure Scoring Model
- Select 5–8 weighted criteria aligned to category strategy (fewer criteria = more defensible)
- Lock weights and distribute to all evaluators before any supplier data is reviewed
- Run calibration session: evaluators score a hypothetical supplier profile to align on what a "3" vs. a "5" means on each criterion
- Document scoring rubric with concrete anchors for each score level

### Step 3: Issue Prequalification Questionnaire (PQQ)
- Distribute standardized PQQ covering: legal entity details, ownership structure, certifications, financial statements (3 years), insurance certificates, key client references, capacity data, ESG policies, cybersecurity posture, business continuity plans
- Set a hard submission deadline with no extensions (late submissions = automatic disqualification)

### Step 4: Execute Gate Screening
- Run sanctions/debarment screening (OFAC SDN, SAM.gov, World Bank Debarment List, EU sanctions)
- Verify certifications directly with issuing bodies (not just supplier-provided PDFs)
- Pull external financial intelligence: D&B report, Experian Intelliscore, or equivalent
- Flag any gate failures; notify supplier with specific deficiency; allow one cure period for correctable items (e.g., expired certification pending renewal)

### Step 5: Conduct Detailed Scoring
- Each evaluator independently scores the supplier against each criterion using the locked rubric
- Financial health sub-score: combine PAYDEX (30% of sub-score), Failure Score (20%), balance sheet ratios (30%), revenue trend (20%)
- Technical capability sub-score: audit findings, process capability data, equipment age/condition, workforce skill levels
- Calculate weighted composite score per evaluator, then average across panel
- Flag any criterion where individual evaluator scores diverge by more than 2 points for consensus discussion

### Step 6: Verify References and Conduct Site Visits (Tier 1)
- Execute reference verification protocol (minimum 3 references for Tier 1, 2 for Tier 2)
- For Tier 1: schedule on-site audit covering production floor, quality lab, warehouse, and management system documentation
- Document findings in a standardized audit report with corrective action requests for any non-conformances

### Step 7: Compile Qualification Decision
- Generate composite qualification score with category breakdowns
- Apply decision thresholds: Qualified, Conditionally Qualified (with improvement plan and recheck date), or Disqualified
- For Conditionally Qualified suppliers: define specific corrective actions, assign deadlines, and schedule follow-up verification
- Submit qualification package for approval per delegation of authority matrix

### Step 8: Establish Requalification Cadence
- Tier 1: annual full requalification with quarterly performance scorecard reviews
- Tier 2: biennial requalification with semi-annual performance check
- Tier 3: triennial requalification, triggered earlier by any quality escape or delivery failure
- Continuous monitoring: set alerts on D&B financial risk changes, certification expirations, and sanctions list updates

## Evaluation Criteria

### Composite Scoring Model — Detailed Rubric Anchors

**Quality & Technical Capability (1–5 scale)**
- 5: ISO-certified, defect rate <0.5%, Cpk >1.67, active continuous improvement program with documented results
- 4: ISO-certified, defect rate <1%, Cpk >1.33, improvement program in place
- 3: ISO-certified, defect rate <2%, meets minimum specification requirements
- 2: Certification pending or expired, defect rate 2–5%, reactive quality approach
- 1: No quality management system, defect rate >5%, no process controls documented

**Financial Health (1–5 scale)**
- 5: PAYDEX ≥80, D&B Failure Score low risk, current ratio >2.0, 3-year revenue CAGR >10%
- 4: PAYDEX 70–79, moderate-low risk, current ratio 1.5–2.0, stable revenue
- 3: PAYDEX 60–69, moderate risk, current ratio 1.0–1.5, flat revenue
- 2: PAYDEX 50–59, moderate-high risk, current ratio 0.8–1.0, declining revenue
- 1: PAYDEX <50, high risk/severe, current ratio <0.8, significant losses

**Delivery & Operational Capacity (1–5 scale)**
- 5: OTIF >98%, demonstrated 30%+ surge capacity, redundant logistics, <2% lead time variance
- 4: OTIF 95–98%, 20% surge capacity, reliable logistics, <5% lead time variance
- 3: OTIF 90–95%, 10% surge capacity, acceptable logistics, <10% lead time variance
- 2: OTIF 80–90%, limited surge capacity, occasional logistics failures
- 1: OTIF <80%, no surge capacity, frequent delivery failures

### Decision Thresholds
- **Qualified (Green)**: Composite ≥80/100, no individual category below 70%
- **Conditionally Qualified (Amber)**: Composite 65–79, or one category between 50–69% with corrective action plan
- **Disqualified (Red)**: Composite <65, any gate failure, or any category below 50%

## Red Flags & Edge Cases

1. **The "Reference Laundering" Supplier**: Provides references from companies that are actually subsidiaries, joint ventures, or entities with shared ownership. Cross-check reference company D-U-N-S numbers against the supplier's corporate family tree in D&B.

2. **Certification Date Mismatch**: Supplier presents an ISO 9001 certificate that shows the registrar's last audit was 18+ months ago. ISO surveillance audits occur annually; a gap suggests the certification may be suspended. Verify directly with the certification body's public registry.

3. **Revenue Concentration Risk**: Supplier derives >40% of revenue from a single client. If that client leaves, the supplier's financial viability collapses. Identify this during financial analysis by requesting a revenue-by-client breakdown (top 5 clients by percentage).

4. **The "Golden Sample" Problem**: Supplier delivers perfect quality samples during qualification but degrades quality at production volumes. Mitigate by requiring First Article Inspection (FAI) at production rates, not prototype quantities. Mandate Cpk data from production runs, not cherry-picked samples.

5. **Shell Company or Recently Formed Entity**: Supplier was incorporated within the past 12 months but claims extensive experience. Check beneficial ownership through corporate registry filings. Recently formed entities may be fronts for debarred suppliers re-entering the market under new names.

6. **PAYDEX Score with Insufficient Trade Experiences**: D&B requires minimum 2 vendors reporting 3 trade experiences each to generate a PAYDEX. A score based on only 3–4 total experiences may be unreliable. Flag any PAYDEX generated from fewer than 10 trade experiences as "insufficient data" and require additional financial documentation.

7. **Geopolitical Single-Point-of-Failure**: Supplier's sole manufacturing facility is in a region with active sanctions risk, political instability, or natural disaster exposure (e.g., flood plain, seismic zone). A 2024 scenario: sole-source electronic component suppliers in regions subject to export control changes created 6-month supply gaps for buyers who failed to identify this during qualification.

8. **The "Borrowed Capacity" Vendor**: Supplier quotes capacity based on subcontractor arrangements they do not disclose. During qualification they present factory tours of leased or third-party facilities as their own. Require explicit declaration of any subcontracting and apply the same qualification criteria to critical sub-tier suppliers.

9. **Insurance Coverage Gaps**: Supplier carries general liability but lacks product liability, professional indemnity, or cyber liability coverage relevant to the engagement. A $1M general liability policy is meaningless when the contract exposure is $10M in potential recall costs.

10. **Scoring Calibration Drift**: Over successive quarterly reviews, evaluator scores drift upward (rating inflation). A supplier rated "3" two years ago now receives "4" for identical performance because the team's internal benchmark has shifted. Mitigate by anchoring every scoring cycle to the original rubric definitions and periodically auditing historical score distributions.

11. **Survivorship Bias in Reference Pools**: Suppliers only provide references from successful engagements. Their churned or terminated clients are never represented. Use independent sources — industry directories, trade association member lists, LinkedIn network analysis — to identify clients the supplier did not volunteer.

12. **ESG Greenwashing**: Supplier presents elaborate sustainability policies and commitments but has no third-party verification (EcoVadis, CDP, B Corp). Policies without audited metrics are marketing documents, not qualification evidence. Require third-party ESG scores or audited sustainability reports.

13. **Beneficial Ownership Opacity**: Supplier's ownership structure uses multiple holding companies across jurisdictions, making it impossible to identify ultimate beneficial owners. This obstructs sanctions screening and conflict-of-interest checks. Require disclosure of all entities with >10% ownership and verify against corporate registries.

14. **Capacity Commitment Without Capital**: Supplier promises to add a second production line to meet your volume requirements but has not yet ordered equipment or secured financing. Score capacity on demonstrated capability, not stated intention. Require evidence of capital expenditure commitments (purchase orders for equipment, facility lease agreements).

## Common Mistakes

**Weighting price above all else (L1 bias)**: Defaulting to lowest-price-wins eliminates the purpose of multi-criteria scoring. Art of Procurement research demonstrates that the lowest-cost supplier frequently scores lowest on weighted composite assessments. Cost weight should rarely exceed 20% for complex categories.

**Changing weights after seeing bids**: Adjusting criteria weights post-submission to favor a preferred vendor destroys process integrity and creates legal exposure in public procurement. Lock weights before RFx issuance and document sign-off.

**Skipping evaluator calibration**: Without a pre-scoring calibration session, one evaluator's generous "4" equals another's strict "2." Consolidated scores become noise, not signal. Run a 30-minute calibration exercise with a sample profile before live scoring begins.

**Treating qualification as a one-time event**: Qualifying a supplier at onboarding and never reassessing creates a false sense of security. Financial health, certifications, and capability change continuously. Requalification cadence must match the risk tier.

**Over-indexing on certifications as proxies for capability**: An ISO 9001 certificate confirms a quality management system exists; it does not confirm the system produces good outcomes for your specific requirements. Certifications are gate criteria, not differentiators. Score actual performance data — defect rates, Cpk, audit findings — not certificate possession.

**Ignoring sub-tier supply chain risk**: Qualifying only the Tier 1 supplier while their critical raw materials come from a single, unvetted sub-tier source transfers risk without reducing it. For Tier 1 strategic suppliers, extend qualification requirements at least one level down.

**Using too many criteria**: Scorecards with 15+ criteria dilute the signal from any single dimension. Best practice is 5–8 criteria. If more granularity is needed, nest sub-criteria under major categories rather than flattening everything to one level.

**Collecting data without verification**: Accepting supplier self-reported defect rates, on-time delivery percentages, and financial figures without cross-referencing creates garbage-in-garbage-out scoring. Verify critical data points against independent sources: customer references for delivery claims, D&B for financial claims, certification body registries for compliance claims.

## Regulatory & Compliance Requirements

### Quality Management Standards
- **ISO 9001:2015 Clause 8.4** — "Control of externally provided processes, products and services." Requires organizations to establish criteria for evaluation, selection, monitoring of performance, and re-evaluation of external providers. Organizations must retain documented information of these activities.
- **ISO 14001:2015** — Environmental management system standard. Increasingly required as a gate criterion for suppliers in manufacturing, energy, and chemicals categories.
- **AS9100D** — Aerospace quality management system. Mandates supplier qualification with documented approval status, including provisions for product and process approval, methods for release of product, and competence of personnel.
- **IATF 16949:2016** — Automotive quality management standard. Requires a supplier quality management system development process and supplier monitoring dashboard.

### Regulatory Compliance Screening
- **OFAC SDN List** (U.S. Treasury) — All U.S. persons must screen business counterparties against the Specially Designated Nationals and Blocked Persons List. Violations carry penalties up to $20M and criminal prosecution.
- **FCPA (Foreign Corrupt Practices Act)** — Anti-bribery provisions require due diligence on third-party intermediaries including suppliers. Adequate supplier due diligence is an affirmative defense in FCPA enforcement actions.
- **UK Bribery Act 2010** — Section 7 (failure to prevent bribery) requires "adequate procedures" including supply chain due diligence.
- **EU Corporate Sustainability Due Diligence Directive (CSDDD) 2024** — Requires large companies to identify, prevent, and mitigate adverse human rights and environmental impacts in their supply chains, including supplier qualification processes.
- **FAR Part 9 (Federal Acquisition Regulation)** — Subpart 9.1 establishes responsibility standards for US government contractors including financial resources, ability to comply, satisfactory performance record, and organizational integrity.
- **SAM.gov (System for Award Management)** — U.S. government debarment and exclusion database. Mandatory screening for any supplier involved in federally funded work.

### Industry-Specific Standards
- **USP <1083>** — Pharmaceutical supplier qualification requiring risk-based evaluation, supplier audits, quality agreements, and ongoing performance monitoring.
- **FDA 21 CFR Part 820** — Medical device quality system regulation mandating supplier controls.
- **NADCAP** — National Aerospace and Defense Contractors Accreditation Program for special processes (welding, heat treating, NDT).
- **GMP (Good Manufacturing Practice)** — Supplier qualification requirements for food, pharmaceutical, and cosmetic manufacturing.

## Terminology

**Analytic Hierarchy Process (AHP)**: Mathematical method for multi-criteria decision-making that uses pairwise comparisons to derive priority weights, producing a consistency ratio that validates whether evaluator judgments are logically coherent. Applied to supplier selection when organizations require mathematically defensible weight allocation.

**Approved Vendor List (AVL)**: Registry of suppliers that have passed qualification and are authorized for purchase orders. Managed by procurement with input from quality; purchasing from non-AVL suppliers typically requires deviation approval.

**Carter's 10Cs**: Supplier evaluation framework developed by Ray Carter comprising Competency, Capacity, Commitment, Control, Cash, Cost, Consistency, Culture, Clean, and Communication. Published by CIPS and adopted as a baseline checklist across procurement organizations.

**Composite Score**: Single numerical rating derived by multiplying individual criterion scores by their assigned weights and summing. Used to rank and compare suppliers on a common scale (typically 0–100).

**Cpk (Process Capability Index)**: Statistical measure of a manufacturing process's ability to produce output within specification limits. Cpk ≥ 1.33 indicates a capable process; Cpk ≥ 1.67 indicates a highly capable process. Requested during technical qualification to verify production consistency.

**Data Envelopment Analysis (DEA)**: Non-parametric efficiency measurement technique that benchmarks suppliers against each other rather than against absolute standards. Identifies which suppliers produce the best output-to-input ratios relative to the evaluated set.

**D-U-N-S Number**: Nine-digit unique identifier assigned by Dun & Bradstreet to individual business entities. Foundation for pulling PAYDEX, Failure Score, and SER ratings. Required for any external financial risk assessment.

**EcoVadis**: Third-party sustainability rating platform that scores companies (0–100) across environment, labor practices, ethics, and sustainable procurement. Increasingly used as an ESG qualification gate or scoring input.

**First Article Inspection (FAI)**: Documented verification that the first production unit meets all drawing and specification requirements. Critical gate between supplier qualification and production release; confirms that the supplier's manufacturing process — not just their prototype capability — produces conforming parts.

**Gate Criteria**: Binary pass/fail requirements that a supplier must satisfy before proceeding to scored evaluation. Failure on any gate criterion eliminates the supplier from consideration regardless of strength in other areas.

**Kraljic Matrix**: Portfolio analysis tool classifying purchased items along two axes — supply risk and profit impact — into four quadrants: Strategic, Bottleneck, Leverage, and Routine. Determines the appropriate depth of supplier qualification activity.

**OTIF (On-Time In-Full)**: Delivery performance metric measuring the percentage of orders delivered on or before the promised date with complete quantities. Industry benchmark for reliable suppliers: OTIF ≥ 95%.

**PAYDEX Score**: Dun & Bradstreet's dollar-weighted numerical indicator (0–100) of payment timeliness based on trade experiences reported by vendors. Score of 80 = prompt payment at terms; below 50 = high risk of slow payment. Requires minimum 2 trade references reporting 3 experiences each.

**Prequalification Questionnaire (PQQ)**: Standardized document issued to potential suppliers requesting information on legal status, financial health, certifications, capacity, references, and policies before they are invited to bid. Functions as the primary data collection instrument for qualification scoring.

**Supplier Evaluation Risk (SER) Rating**: D&B metric predicting the likelihood a company will seek legal relief from creditors or cease operations without paying creditors in full within the next 12 months. Used alongside PAYDEX for comprehensive financial risk assessment.

**Supplier Stability Index (SSI)**: D&B indicator predicting probability of significant financial stress over the next 90 days. Provides a shorter-horizon risk signal than the SER Rating.

**Total Cost of Ownership (TCO)**: Comprehensive cost calculation including unit price, freight, customs duties, quality costs (inspection, rework, warranty), inventory carrying costs, and administrative overhead. Replaces unit price as the cost criterion in sophisticated scoring models.

**Weighted Scoring Matrix**: Evaluation tool where each criterion receives a percentage weight reflecting its strategic importance, scores are multiplied by weights, and weighted scores are summed to produce a composite rating. The standard quantitative method for multi-criteria supplier evaluation.

## Quality Checklist

1. ☐ Gate criteria defined and applied before any scored evaluation began — no gate-failed supplier received a composite score
2. ☐ Scoring weights locked, documented, and distributed to all evaluators before supplier data was reviewed
3. ☐ Evaluator calibration session conducted with documented alignment on score-level definitions for each criterion
4. ☐ Sanctions screening executed against current OFAC SDN list, SAM.gov exclusions, and applicable regional lists with screenshot evidence
5. ☐ Certifications verified directly with issuing body or public registry — not solely from supplier-provided documents
6. ☐ Financial health assessment includes at least one external source (D&B, Experian, or equivalent) beyond supplier self-reported financials
7. ☐ PAYDEX score validated for sufficient trade experience volume (minimum 10 trade experiences for reliability)
8. ☐ Reference checks include at least one client not nominated by the supplier (independent reference)
9. ☐ Reference interviews followed structured questionnaire covering volume, quality, crisis behavior, and requalification intent
10. ☐ Evaluator score divergences (>2 points on any criterion) resolved through documented consensus discussion
11. ☐ Composite score calculated correctly — spot-check arithmetic: weight × score per criterion, summed, averaged across evaluators
12. ☐ Decision threshold applied consistently — any Conditionally Qualified supplier has a documented corrective action plan with specific deadlines
13. ☐ Requalification cadence established and entered into tracking system with automated reminder triggers
14. ☐ Qualification package includes complete audit trail: PQQ responses, gate screening results, individual evaluator scorecards, reference notes, financial reports, and approval sign-offs
15. ☐ Sub-tier supplier risk assessed for Tier 1 strategic suppliers — critical sub-suppliers identified and flagged for qualification extension

## References

- Kodiak Hub. "Vendor Rating: The Complete Procurement Guide For 2025." https://www.kodiakhub.com/blog/vendor-rating-guide
- Kodiak Hub. "The Ultimate Vendor Selection Framework for 2025." https://www.kodiakhub.com/blog/vendor-selection-framework
- RKS Trainings. "Vendor Evaluation & Supplier Performance Frameworks (2025 Guide)." https://rkstrainings.com/vendor-evaluation-supplier-performance-management-frameworks/
- ISM (Institute for Supply Management). "Supplier Evaluation and Selection Criteria Guide." https://www.ism.ws/logistics/supplier-evaluation/
- Wicely. "Supplier Evaluation Criteria: A Weighted Scoring Framework." https://wicely.com/resources/supplier-evaluation-criteria-weighted-scoring
- QC Advisor. "Supplier Qualification: Definition, Process, Steps and Guidelines." https://www.qcadvisor.com/blog/supplier-qualification/
- QC Advisor. "Supplier Capability Assessment: Definition, Importance and Steps." https://www.qcadvisor.com/blog/supplier-capability-assessment/
- SimplerQMS. "Supplier Qualification: Definition, Process, and Guidelines." https://simplerqms.com/supplier-qualification/
- Ivalua. "Vendor Scorecards: Complete Guide For Procurement Teams." https://www.ivalua.com/blog/vendor-scorecard/
- Art of Procurement. "Key Supplier Selection Criteria Every Procurement Executive Should Know." https://artofprocurement.com/blog/key-supplier-selection-criteria-every-procurement-executive-should-know
- ProcureKey. "Weighted RFP Scoring for Structured Supplier Evaluation." https://www.procurekey.com/blog/weighted-rfp-scoring/
- Capital One. "What Is a PAYDEX Score & How Does It Work?" https://www.capitalone.com/learn-grow/business-resources/paydex-score/
- Dun & Bradstreet. "D&B Credit: Risk Assessment Documentation." https://docs.dnb.com/credit/en-US/viewing_a_report/risk_assessment
- Rho. "What Is a PAYDEX Score?" https://www.rho.co/blog/paydex-score
- Nav. "Dun & Bradstreet PAYDEX Score." https://www.nav.com/business-credit/dun-bradstreet-paydex/
- Smartsheet. "Vendor & Supplier Due Diligence Checklist." https://www.smartsheet.com/sites/default/files/IC-Vendor-and-Supplier-Due-Diligence-Checklist-10584_PDF.pdf
- Sprinto. "A Practical Guide To The Vendor Due Diligence Checklist." https://sprinto.com/blog/vendor-due-diligence-checklist/
- Ramp. "Vendor Due Diligence: Definition, Process & Checklist." https://ramp.com/blog/vendor-due-diligence-checklist
- Mitratech. "Vendor Due Diligence Strategy and Checklist." https://mitratech.com/resource-hub/blog/vendor-due-diligence/
- Esgrid. "Supplier Evaluation Criteria – Full List, Weighting Methods." https://esgrid.com/blog/supplier-evaluation-criteria
- QSTRAT. "Best Practices for Supplier Qualification in Aerospace." https://qstrat.com/supplier-qualification-best-practices-aerospace/
- Requis. "Weighted Scoring Prioritization Tool." https://requis.com/blog/weighted-scoring-supplier-risk-assessment/
- USP. "General Chapter <1083> Supplier Qualification." https://www.usp.org/sites/default/files/usp/document/supply-chain/apec-toolkit/USP%20GC1083.pdf
- ISO. "ISO 9001 in the Supply Chain." https://www.iso.org/files/live/sites/isoorg/files/archive/pdf/en/iso_9001_supply-chain.pdf
- Core Business Solutions. "ISO 9001 Purchasing Procedure." https://www.thecoresolution.com/8-4-purchasing-iso-explained
- GEP. "Supplier Capability Assessment: Beyond the Basics." https://www.gep.com/blog/strategy/supplier-capability-assessment-importance-limitations
- Kodiak Hub. "Supplier Financial Risk Assessment: Key Steps & Analysis." https://www.kodiakhub.com/blog/supplier-financial-risk-assessment
- ProcessUnity / Dun & Bradstreet. "D&B Connector: Financial Risk Review." https://www.processunity.com/wp-content/uploads/2020/04/Datasheet-Dun-and-Bradstreet-Connector-2001019.pdf