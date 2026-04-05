---
name: performance-review-agent
description: >
  Monitors and scores vendor performance through KPI tracking, SLA compliance measurement, quality metrics analysis, and continuous improvement programs.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "ISO 9001, Six Sigma, CIPS"
---

# Performance Review Agent

## Domain Overview

Supplier performance management (SPM) is the systematic process of measuring, analyzing, scoring, and improving vendor performance against contractual obligations and strategic procurement goals. Unlike ad-hoc vendor check-ins, mature SPM operates as a closed-loop system: KPIs are defined at contract inception, tracked through automated data collection, scored via weighted scorecards, reviewed in structured business reviews, and fed into corrective action or supplier development programs. The ASCM Supply Chain Operations Reference Digital Standard (SCOR DS) defines five core performance attributes for this function — reliability, responsiveness, agility, costs, and asset management efficiency — each with Level 1 through Level 3 metrics that practitioners use to benchmark against industry norms.

The discipline spans three operational layers. The first layer is **transactional monitoring** — tracking on-time delivery (OTD), fill rate, invoice accuracy, and defect rates on a per-PO or per-shipment basis. The second layer is **scorecard aggregation** — rolling transactional data into weighted composite scores across categories (quality, delivery, cost, service, compliance, innovation) typically on a monthly or quarterly cadence. The third layer is **strategic performance governance** — using scorecard outputs to drive Quarterly Business Reviews (QBRs), Supplier Corrective Action Requests (SCARs), tier reassignment via the Kraljic matrix, and formal continuous improvement programs such as supplier development workshops and joint value engineering.

A critical distinction practitioners make is between **lagging indicators** (defect PPM, total cost of quality, warranty claims) and **leading indicators** (supplier audit scores, process capability indices like Cpk, sub-tier risk exposure). Organizations that only track lagging indicators discover problems after they've already caused production line shutdowns or customer complaints. ISM (Institute for Supply Management) research consistently shows that best-in-class procurement organizations track 8-12 KPIs per strategic supplier, while average organizations track fewer than 5 — and the gap in outcomes is material: top performers achieve 95%+ OTIF (On-Time In-Full) rates versus 82% industry median.

The regulatory context varies by industry but always matters. ISO 9001:2015 Clause 8.4 mandates that organizations "determine and apply criteria for the evaluation, selection, monitoring of performance, and re-evaluation of external providers." Automotive supply chains layer on IATF 16949 requirements. In U.S. federal procurement, FAR Subpart 42.15 requires Contractor Performance Assessment Reporting System (CPARS) evaluations across five elements: quality, schedule, cost control, management, and small business subcontracting. CIPS (Chartered Institute of Procurement & Supply) provides a widely adopted competency framework for practitioner-level supplier evaluation.

## Core Decision Framework

### The Supplier Segmentation Gate

Before scoring performance, determine the supplier's strategic classification using the Kraljic Matrix. The review rigor, KPI count, review frequency, and corrective action thresholds all vary by quadrant:

| Kraljic Quadrant | Spend/Risk Profile | Review Frequency | KPI Depth | Escalation Threshold |
|---|---|---|---|---|
| **Strategic** (high profit impact, high supply risk) | Critical partnerships | Monthly scorecard + Quarterly QBR | 10-15 KPIs | Score <80% triggers executive review |
| **Bottleneck** (low profit impact, high supply risk) | Sole-source or constrained | Monthly scorecard | 8-10 KPIs | Score <75% triggers supply assurance plan |
| **Leverage** (high profit impact, low supply risk) | Competitive, substitutable | Quarterly scorecard | 6-8 KPIs | Score <70% triggers sourcing re-competition |
| **Routine** (low profit impact, low supply risk) | Commodity, transactional | Semi-annual scorecard | 3-5 KPIs | Score <65% triggers supplier replacement |

### Weighted Scoring Logic

Practitioners assign category weights based on business criticality. A canonical weighting model:

- **Quality**: 25-35% — Defect rate (PPM or DPMO), first-pass yield, certificate of conformance accuracy, warranty claim rate
- **Delivery**: 20-30% — OTIF (On-Time In-Full), lead time adherence, advance shipping notice (ASN) accuracy, expedite frequency
- **Cost**: 15-25% — Total cost of ownership (TCO) trend, price variance to contract, cost-reduction commitment attainment, invoice accuracy
- **Service & Responsiveness**: 10-20% — RFQ response time, issue resolution time, communication quality (subjective 1-5 rating), escalation responsiveness
- **Compliance & Risk**: 5-15% — Regulatory compliance (environmental, labor), cybersecurity posture, insurance currency, financial stability (D&B score, Z-score)
- **Innovation**: 0-10% — Value engineering proposals submitted, process improvement suggestions, new technology adoption

Each KPI is scored on a 0-100 scale, multiplied by category weight, then summed to produce a composite score. Industry-standard tier classification:

- **90-100**: Preferred Supplier — eligible for volume growth, sole-source consideration
- **80-89**: Approved Supplier — meets expectations, maintain current allocation
- **70-79**: Conditional Supplier — performance improvement plan (PIP) required within 30 days
- **60-69**: Probationary Supplier — SCAR issued, sourcing alternatives actively pursued
- **Below 60**: Disqualified — exit plan initiated, no new POs issued

### The SCOR Diagnostic Layer

Map each KPI to SCOR DS Level 1 metrics for benchmarking:

- **RL.1.1** Perfect Order Fulfillment → combines OTIF + complete documentation + damage-free delivery
- **RS.1.1** Order Fulfillment Cycle Time → end-to-end from PO placement to goods receipt
- **AG.1.1** Upside Supply Chain Flexibility → ability to increase supply 20% within 30 days
- **CO.1.1** Total Cost to Serve → procurement cost + logistics + quality cost + risk cost
- **AM.1.1** Cash-to-Cash Cycle Time → payment terms impact on working capital

## Step-by-Step Process

### Phase 1: KPI Architecture (Pre-Contract / Contract Renewal)

1. **Classify supplier** using Kraljic quadrant analysis — map spend data against supply risk factors (sole-source dependency, geographic concentration, lead time volatility)
2. **Select KPIs** from the master catalog based on quadrant — never apply the same scorecard template to a strategic partner and a routine commodity supplier
3. **Define measurement methodology** for each KPI — specify the data source (ERP goods receipt, QMS inspection records, logistics TMS), calculation formula, measurement frequency, and target threshold
4. **Embed KPIs in contract language** — SLA clauses must specify: metric definition, measurement method, reporting cadence, target, tolerance band, penalty/incentive structure, and dispute resolution mechanism
5. **Establish baseline** — collect 90 days of performance data before activating penalty/incentive clauses on new suppliers

### Phase 2: Data Collection & Scoring (Ongoing Operations)

6. **Automate transactional capture** — configure ERP (SAP MM/SRM, Oracle Procurement Cloud, Coupa) to log delivery timestamps, GR/IR matching, quality inspection results at goods receipt
7. **Calculate KPI scores monthly** — apply the agreed formula; flag any data gaps or anomalies before scoring (e.g., a supplier showing 100% OTD because PO acknowledgment dates were changed retroactively)
8. **Apply weighted scoring model** — multiply each KPI score by its category weight; generate composite score
9. **Generate trend analysis** — compare current period to rolling 3-month, 6-month, and 12-month averages; identify statistically significant deviations (>2 standard deviations from mean)
10. **Distribute scorecard** to supplier and internal stakeholders — share no later than 10 business days after period close

### Phase 3: Review & Action (Periodic Governance)

11. **Conduct structured review meeting** — QBR format for strategic/bottleneck suppliers; written scorecard delivery for leverage/routine
12. **Apply the traffic-light escalation protocol**:
    - **Green** (≥80): Acknowledge, discuss improvement opportunities, review innovation pipeline
    - **Yellow** (70-79): Require written corrective action plan within 15 business days; schedule 30-day follow-up
    - **Red** (<70): Issue formal SCAR using 8D methodology; require root cause analysis (D1-D8) within 10 business days; assign procurement sponsor for weekly tracking
13. **Document outcomes** — record meeting minutes, action items with owners and due dates, and next review date in the Supplier Relationship Management (SRM) system

### Phase 4: Corrective Action & Continuous Improvement

14. **Track SCAR closure** — verify containment action (D3), root cause identification (D4), permanent corrective action implementation (D6), and effectiveness validation (D7)
15. **Validate improvement** — require 3 consecutive measurement periods at or above target before removing probationary status
16. **Feed insights into supplier development** — for strategic suppliers scoring 70-85, invest in joint improvement: Kaizen events, process mapping workshops, shared demand forecasting
17. **Update tier classification** — promote or demote suppliers based on 12-month rolling composite score; update approved supplier list (ASL) accordingly
18. **Report to executive procurement leadership** — aggregate supplier performance data into category-level dashboards showing spend-at-risk, quality cost trends, and savings attainment

## Evaluation Criteria

### Quantitative Metrics (Hard Data)

| Metric | Formula | Best-in-Class Target | Source |
|---|---|---|---|
| On-Time In-Full (OTIF) | (Orders delivered on-time AND in-full qty) / Total orders × 100 | ≥95% | ISM |
| Defect Rate (PPM) | (Defective units / Total units received) × 1,000,000 | <500 PPM | IATF 16949 norm |
| Perfect Order Rate | (On-time + In-full + Damage-free + Correct documentation) / Total orders × 100 | ≥90% | SCOR RL.1.1 |
| First-Pass Yield | Units passing inspection without rework / Total units inspected × 100 | ≥98% | Lean/Six Sigma |
| Invoice Accuracy | Invoices matching PO price and quantity / Total invoices × 100 | ≥99% | AP benchmark |
| Cost Savings Attainment | Actual negotiated savings / Committed savings target × 100 | ≥100% | Category plan |
| Fill Rate | (Quantity shipped / Quantity ordered) × 100 | ≥97% | ISM |
| Lead Time Variance | (Actual lead time − Quoted lead time) / Quoted lead time × 100 | ≤5% variance | Contract terms |
| SCAR Response Time | Business days from SCAR issuance to D3 containment response | ≤5 business days | Internal SOP |
| RFQ Turnaround | Business days from RFQ issuance to supplier quote submission | ≤3 business days (standard); ≤1 day (expedite) | Category-dependent |

### Qualitative Metrics (Subjective Assessment)

Rate each on a 1-5 scale (1=Unacceptable, 3=Meets Expectations, 5=Exceeds Expectations):

- **Communication Quality**: Proactive updates, single-point-of-contact responsiveness, escalation handling
- **Technical Capability**: Engineering support depth, design-for-manufacturability input, prototyping speed
- **Account Management**: Dedicated team stability, executive sponsor engagement, strategic alignment
- **Innovation Contribution**: Unsolicited improvement proposals, technology roadmap sharing, joint development willingness
- **Sustainability Practices**: Carbon reporting transparency, circular economy initiatives, ethical sourcing evidence

## Red Flags & Edge Cases

1. **Retroactive PO date manipulation**: Supplier requests PO acknowledgment date changes in ERP to mask late deliveries. The OTD metric shows 96% but actual dock-to-need performance is 78%. Always measure OTD against original requested delivery date, not latest confirmed date.

2. **Partial shipment inflation of fill rate**: Supplier ships 90% of quantity on time, then dribbles remaining 10% over subsequent weeks. Fill rate looks acceptable but receiving dock labor costs spike 40%. Track "complete order fill rate" not just line-item fill rate.

3. **Quality metric gaming via sampling bias**: Supplier provides certificates of conformance based on favorable batch samples while actual production lots contain higher defect rates. Cross-reference CoC data with incoming inspection results and in-process reject rates.

4. **Cost savings double-counting**: Procurement reports $2M savings from a negotiation while the supplier simultaneously introduces a 3% surcharge on freight terms, netting actual savings to $800K. Always measure total cost of ownership (TCO), not unit price alone.

5. **SLA holiday loophole**: Contract SLA specifies "5 business day lead time" but excludes supplier's local holidays, government-mandated shutdown periods, and force majeure windows. A 5-day SLA can functionally become 12 calendar days during Chinese New Year or German Betriebsferien.

6. **Single-source disguised as dual-source**: Two suppliers on the ASL but 94% of spend flows to one. When that supplier's score drops to 68, the "backup" lacks tooling, quality approvals, or capacity to ramp. Validate alternate supplier readiness annually.

7. **Scorecard recency bias**: A supplier that performed at 92% for 11 months but had a catastrophic quality escape in Month 12 receives a 70% quarterly score. Without rolling 12-month context, the organization may over-react and damage a strong relationship. Conversely, a chronic 76% performer who spikes to 88% in one quarter may receive unwarranted promotion.

8. **Compliance-washing via documentation**: Supplier provides ISO 9001 certificate but the certified scope doesn't cover the specific process or product supplied. The certificate shows "metal stamping" but they are supplying injection-molded components from an uncertified facility. Verify certificate scope against actual supply.

9. **Innovation score manipulation**: Supplier submits 15 "Value Engineering" proposals per quarter that are impractical or already-rejected ideas repackaged. Innovation KPI shows high activity but zero implemented savings. Score on accepted and implemented proposals only.

10. **Survivorship bias in supplier panels**: Quarterly reviews only include current suppliers. Suppliers that were disqualified or exited are never root-cause analyzed. The organization repeats the same onboarding mistakes. Maintain an exit analysis register with documented lessons learned.

11. **KPI threshold erosion via "negotiated" targets**: Strategic supplier underperforms at 87% for three consecutive quarters; instead of issuing a PIP, procurement lowers the target to 85% to "align with market conditions." Over 2-3 years, performance standards degrade materially. Document any target adjustments with business case justification and sunset clauses.

12. **Missing upstream visibility**: Tier-1 supplier scores 94% but their critical sub-tier (Tier-2) component supplier is operating at 65% quality. When the Tier-2 fails, Tier-1's performance collapses overnight. Require strategic suppliers to report Tier-2 performance on critical components.

13. **Asymmetric penalty structures**: Contract penalizes supplier $10K per day for late delivery but has no incentive for early delivery or sustained above-target performance. This drives exact-minimum performance behavior. Best-in-class contracts include gain-sharing for sustained outperformance.

## Common Mistakes

1. **Measuring too many KPIs for routine suppliers**: Applying a 15-KPI strategic scorecard to a $50K/year office supplies vendor wastes analyst time and supplier goodwill. Match measurement intensity to Kraljic classification.

2. **Delayed scorecard distribution**: Sending Q1 scorecards in late Q2 makes the data stale and prevents timely corrective action. Best practice: distribute within 10 business days of period close.

3. **Treating the scorecard as the conversation**: Sending a PDF scorecard via email without a structured review meeting eliminates the most valuable part — the dialogue about root causes, improvement plans, and relationship health.

4. **Ignoring the "service" dimension**: Organizations hyper-focus on quality and delivery while ignoring responsiveness, communication, and technical support — the factors that determine whether a supplier is merely adequate or genuinely enabling.

5. **Failing to baseline new suppliers**: Applying penalty clauses from Day 1 without a 90-day baseline period creates adversarial relationships and produces unreliable initial data that skews long-term trend analysis.

6. **Not weighting by spend or criticality**: Averaging all supplier scores equally in executive dashboards makes a 70-scoring $50M strategic supplier appear equivalent to a 70-scoring $200K routine supplier. Weight dashboard views by spend, risk, or both.

7. **Conflating SLA compliance with performance excellence**: A supplier meeting every SLA at the minimum threshold (e.g., 95.0% OTD when target is 95%) is technically compliant but not driving improvement. Distinguish between "contractual floor" and "performance aspiration."

8. **Skipping the closed-loop on SCARs**: Issuing a SCAR but never verifying D7 (effectiveness validation) means the corrective action may not have stuck. Require objective evidence of sustained improvement over 3 measurement cycles.

9. **Using scorecards punitively instead of developmentally**: Organizations that only use scorecards to penalize or exit suppliers create a culture where suppliers hide problems. Best-in-class programs use scorecards to identify joint improvement opportunities and share the savings.

10. **No executive sponsorship for strategic reviews**: QBRs with strategic suppliers attended only by buyer-level personnel lack the authority to make commitments on investment, volume allocation, or joint development — rendering the meeting ceremonial.

## Regulatory & Compliance Requirements

### ISO 9001:2015 — Clause 8.4 (Control of Externally Provided Processes, Products, and Services)
- **8.4.1**: Organizations shall determine and apply criteria for evaluation, selection, monitoring of performance, and re-evaluation of external providers based on their ability to provide processes or products in accordance with requirements. Documented information of these activities and necessary actions shall be retained.
- **8.4.2**: Type and extent of control applied to external providers shall be dependent on the potential impact on the organization's ability to consistently deliver conforming products and services.
- **8.4.3**: Communication to external providers shall include requirements for processes, products, approval of methods/processes/equipment, competence of personnel, and QMS interaction.

### IATF 16949:2016 (Automotive Sector)
- **8.4.2.3**: Supplier quality management system development — organizations shall require automotive QMS certification (IATF 16949) as a minimum for direct material suppliers, with a development plan for those not yet certified.
- **8.4.2.4**: Supplier monitoring — monitor supplier performance through quality of delivered product, customer disruptions, delivery schedule performance, and premium freight notifications.

### SCOR Digital Standard (ASCM)
- Defines 250+ metrics across Plan, Source, Make, Deliver, Return, and Enable processes
- Level 1 strategic metrics (RL.1.1 through AM.1.1) serve as the executive-level benchmarking framework
- Maintained by ASCM (Association for Supply Chain Management), formerly APICS and SCC (Supply Chain Council)

### FAR Subpart 42.15 — Contractor Performance Information (U.S. Federal Procurement)
- **42.1502**: Policy requiring past performance evaluations for contracts exceeding $750,000 (services) or $1,000,000 (supplies)
- **42.1503**: Evaluations entered in CPARS within 120 calendar days of evaluation period end
- Five evaluation elements: Quality, Schedule, Cost Control, Management/Business Relations, Small Business Subcontracting

### Additional Standards
- **ISO 14001:2015**: Environmental management system requirements applicable to supplier environmental compliance scoring
- **SA8000**: Social accountability standard for ethical sourcing and labor practices evaluation
- **ISO 28000**: Supply chain security management system — relevant for compliance scoring of logistics and warehousing suppliers

## Terminology

1. **OTIF (On-Time In-Full)**: The percentage of purchase orders delivered by the requested delivery date with complete quantity. Industry gold-standard delivery metric. Measured against original requested date, not supplier-confirmed date.

2. **PPM (Parts Per Million)**: Defective units per million units received. Used in automotive and manufacturing contexts where defect rates are low. 500 PPM = 0.05% defect rate.

3. **DPMO (Defects Per Million Opportunities)**: A Six Sigma metric that accounts for multiple potential defect types per unit. More granular than PPM for complex assemblies.

4. **SCAR (Supplier Corrective Action Request)**: A formal document requiring a supplier to investigate a nonconformance using structured root cause analysis (typically 8D methodology), implement corrective actions, and provide evidence of effectiveness.

5. **8D Methodology**: An eight-discipline problem-solving framework: D1 Team, D2 Problem Description, D3 Containment, D4 Root Cause, D5 Permanent Corrective Action Selection, D6 Implementation, D7 Prevention of Recurrence, D8 Team Recognition.

6. **QBR (Quarterly Business Review)**: Structured governance meeting between buyer and supplier leadership to review scorecard results, discuss improvement plans, align on strategic objectives, and manage relationship health.

7. **Kraljic Matrix**: A 2×2 supplier segmentation framework (Peter Kraljic, 1983) plotting profit impact against supply risk. Produces four quadrants: Strategic, Bottleneck, Leverage, Routine. Determines review intensity and procurement strategy.

8. **TCO (Total Cost of Ownership)**: The complete cost of acquiring and using a supplier's product/service, including unit price, freight, duties, quality costs (inspection, rework, scrap), inventory carrying cost, and administrative cost.

9. **Perfect Order Rate**: SCOR metric RL.1.1 — the percentage of orders delivered on-time, in-full, damage-free, and with correct documentation. The most stringent single delivery metric.

10. **Cpk (Process Capability Index)**: A statistical measure of a supplier's manufacturing process capability relative to specification limits. Cpk ≥ 1.33 indicates the process is capable; <1.0 indicates non-capable.

11. **ASL (Approved Supplier List)**: The master list of suppliers qualified to receive purchase orders, typically maintained with status designations (Preferred, Approved, Conditional, Probationary, Disqualified).

12. **GR/IR (Goods Receipt / Invoice Receipt)**: The ERP-based three-way match between purchase order, goods receipt, and supplier invoice. Discrepancies indicate delivery or billing accuracy issues.

13. **SRM (Supplier Relationship Management)**: Both a strategy and software category for managing the full supplier lifecycle — from qualification through performance management to exit.

14. **CoC (Certificate of Conformance)**: Supplier-provided document certifying that delivered goods meet specified requirements. Not equivalent to third-party inspection — it is a self-attestation.

15. **Lead Time Variance**: The percentage deviation between actual and quoted/contracted lead time. Chronic positive variance (actual > quoted) indicates supplier capacity or planning problems.

16. **Fill Rate**: The percentage of ordered quantity actually shipped on the first shipment. Distinct from OTIF — fill rate measures quantity completeness; OTIF adds the time dimension.

17. **Spend-at-Risk**: The dollar value of procurement spend managed by suppliers currently scoring in Conditional or Probationary tiers. A key executive dashboard metric.

18. **PIP (Performance Improvement Plan)**: A formal, time-bound document specifying underperformance areas, required corrective actions, targets, milestones, and consequences of failure to improve.

19. **Gain-Sharing**: A contractual mechanism where cost savings or efficiency improvements generated by the supplier are shared between buyer and supplier, typically 50/50 or 60/40, to incentivize continuous improvement.

20. **CPARS (Contractor Performance Assessment Reporting System)**: The U.S. federal government's official system for recording contractor past performance evaluations, mandated by FAR Subpart 42.15.

21. **Premium Freight**: Expedited shipping costs incurred when a supplier's late delivery forces air freight or special trucking to avoid production line stoppage. A direct indicator of delivery failure cost.

22. **Category Management**: The practice of organizing procurement by spend categories (e.g., raw materials, MRO, logistics) rather than by supplier, enabling benchmarking of supplier performance within peer groups.

23. **Kaizen Event**: A focused, short-duration (3-5 day) improvement workshop, often conducted jointly with a strategic supplier at their facility, to reduce waste in a specific process.

24. **SCOR DS**: Supply Chain Operations Reference Digital Standard — the ASCM-maintained framework providing standardized metrics, processes, and benchmarks for supply chain performance measurement.

## Quality Checklist

1. **KPI-to-Contract Alignment**: Every scored KPI has a corresponding definition in the active supplier contract or SLA — no orphan metrics being scored outside contractual scope.
2. **Data Source Verification**: Each KPI is sourced from system-of-record data (ERP, QMS, TMS), not supplier self-reported data or manual spreadsheets, for any metric used in penalty/incentive calculations.
3. **Kraljic Classification Currency**: Supplier segmentation was reviewed within the past 12 months and reflects current spend volumes, supply market conditions, and business criticality.
4. **Weight Justification**: Scorecard category weights are documented with a rationale linked to business strategy (e.g., quality weighted at 35% because the supplier provides safety-critical components).
5. **Baseline Existence**: New suppliers have a documented 90-day baseline period before penalty/incentive clauses activate; baseline data is recorded and stored.
6. **Trend Analysis Inclusion**: Scorecards include rolling 3-month, 6-month, and 12-month trend data alongside the current period — not just a single-period snapshot.
7. **Timeliness**: Scorecards are distributed within 10 business days of measurement period close; QBR invitations sent at least 15 business days in advance with pre-read materials.
8. **SCAR Lifecycle Completion**: Every open SCAR has documented status through all 8D stages; no SCAR older than 90 days remains at D3 (containment) without escalation.
9. **Executive Dashboard Spend-Weighting**: Aggregate performance dashboards weight supplier scores by spend value or risk classification, not simple averaging across all suppliers.
10. **Alternate Supplier Readiness**: For every sole-source or single-source supplier scoring below 85%, a documented alternate sourcing plan exists with qualification timeline.
11. **Subjective Score Calibration**: Qualitative ratings (1-5 scales for service, innovation, etc.) include written rubrics with examples to prevent inter-rater variability exceeding 1 point.
12. **Historical Archive**: Minimum 3 years of scorecard history retained per supplier to support trend analysis, re-qualification decisions, and audit requirements under ISO 9001:2015 Clause 7.5.
13. **Stakeholder Input**: Scorecards for strategic and bottleneck suppliers incorporate input from at least quality, operations, engineering, and procurement — not procurement alone.
14. **Continuous Improvement Evidence**: For suppliers on PIPs, objective evidence of improvement (data, not just action plan documents) is collected for a minimum of 3 consecutive measurement periods before status upgrade.
15. **Contract-Back Audit Trail**: Any scorecard score that triggers a financial penalty or volume reallocation has a documented, auditable trail from raw transaction data through calculation to final score.

## References

1. ASCM — SCOR Digital Standard 2025 Introduction and Framework: https://www.ascm.org/globalassets/ascm_website_assets/docs/scor/intro-and-front-matter-scor-digital-standard-2025.pdf
2. ISM — Optimizing with Supplier Performance Measurement KPIs: https://www.ism.ws/supply-chain/supplier-performance-measurement-kpis/
3. ISM — The Monthly Metric: On-Time Delivery: https://www.ismworld.org/supply-management-news-and-reports/news-publications/inside-supply-management-magazine/blog/2017-11/the-monthly-metric-on-time-delivery/
4. ISM — The Monthly Metric: Fill Rate: https://www.ismworld.org/supply-management-news-and-reports/news-publications/inside-supply-management-magazine/blog/2022/2022-07/the-monthly-metric-fill-rate/
5. CIPS — Supplier Evaluation: https://www.cips.org/intelligence-hub/managing-suppliers/supplier-evaluation
6. CIPS — SCOR Model for Supply Chain Performance: https://www.cips.org/intelligence-hub/procurement/kpis/scor-model
7. CIPS — Kraljic Matrix: https://www.cips.org/intelligence-hub/supplier-relationship-management/kraljic-matrix
8. CIPS — KPIs and Performance Measures Used in Procurement: https://www.cips.org/intelligence-hub/procurement/kpis/model
9. Art of Procurement — Supplier Performance Management Metrics and Frameworks: https://artofprocurement.com/blog/learn-supplier-performance-management-metrics
10. Art of Procurement — The Kraljic Matrix Simply Explained: https://artofprocurement.com/blog/learn-the-kraljic-matrix
11. Ivalua — Vendor Scorecards: Complete Guide for Procurement: https://www.ivalua.com/blog/vendor-scorecard/
12. Ivalua — Ultimate Guide to Supplier Performance Management: https://www.ivalua.com/blog/supplier-performance-management/
13. Mitratech — Vendor Performance & SLA Management Guide: https://mitratech.com/resource-hub/blog/vendor-performance-sla-management/
14. GEP — Why SLAs Matter in Procurement and Operations: https://www.gep.com/blog/strategy/why-slas-matter-in-procurement-and-operations
15. ProcessUnity — SLAs and Vendor Performance Management: https://www.processunity.com/resources/blogs/slas-vendor-performance-management/
16. Ideagen — ISO 9001 Supplier Management Step-by-Step Guide: https://www.ideagen.com/thought-leadership/blog/iso-9001-supplier-management-your-step-by-step-guide
17. ISO 9001 Certification Group — Supplier Evaluation Criteria, Forms & Scorecards: https://isocertificationgroup.com.au/blog/iso-9001-supplier-evaluation-criteria-forms-scorecards/
18. FAR Subpart 42.15 — Contractor Performance Information: https://www.acquisition.gov/far/subpart-42.15
19. CPARS Guidance Document: https://www.cpars.gov/cparsweb/assets/documents/CPARS-Guidance.pdf
20. Procurement Tactics — 8 Supplier Performance Management KPIs for 2026: https://procurementtactics.com/supplier-performance-management-kpis/
21. CPSCP — Supplier Performance Evaluation and Continuous Improvement Strategies: https://cpscp.org/supplier-performance-evaluation-and-continuous-improvement-strategies/
22. ComplianceQuest — Supplier Corrective Action Request: https://www.compliancequest.com/supplier-corrective-action-request/
23. Ease.io — Supplier Corrective Actions Request & Report: https://www.ease.io/blog/supplier-corrective-actions/
24. Graphite Connect — 11 Vendor Performance Management Best Practices: https://www.graphiteconnect.com/blog/supplier-performance-management-best-practices
25. Stibo Systems — Supplier Performance Management Challenges: https://www.stibosystems.com/blog/supplier-performance-management
26. CIO.com — What is SCOR? A Model to Improve Supply Chain Management: https://www.cio.com/article/222381/what-is-scor-a-model-for-improving-supply-chain-management.html
27. HighRadius — Supplier Scorecard: Definition, Key Metrics & Best Practices: https://www.highradius.com/resources/Blog/supplier-scorecard/
28. Amazon Business — How to Build a Vendor Scorecard for Procurement Excellence: https://business.amazon.com/en/blog/vendor-scorecard