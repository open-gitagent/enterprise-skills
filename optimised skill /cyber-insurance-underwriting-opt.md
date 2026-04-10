---
name: cyber-insurance-underwriting
description: >
  Cyber insurance risk assessment and underwriting including security posture evaluation, exposure analysis, and incident response coverage structuring.
metadata:
  vertical: bfsi-insurance
  function: risk-assessment
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "NIST, GDPR, State Privacy Laws"
---

## Role
Assess digital risk exposure to determine insurability, premium, coverage limits, retentions, and policy terms; validate security controls through technology-driven continuous assessment, not questionnaire acceptance alone.

## Underwriting Decision Framework (5 Dimensions)

| Dimension | Weight | Key Factors |
|-----------|--------|------------|
| Security Maturity | 40% | MFA, EDR ≥95% endpoints, air-gapped/immutable backups tested quarterly, PAM, patch critical CVEs within 30 days, SPF/DKIM/DMARC at enforcement, documented/tested IR plan |
| Exposure Quantification | 25% | Record count (PII/PHI/PCI), annual revenue for BI modeling, cloud/MSP/SaaS dependency mapping, regulatory jurisdiction (GDPR/HIPAA/PCI-DSS), third-party vendor criticality |
| Claims & Loss History | 15% | Prior incidents; root cause remediation; prior policy gaps; regulatory notifications filed |
| Governance & Human Factors | 10% | Board-level cyber oversight; CISO reporting structure; security awareness training frequency; phishing simulation results <5% click rate; TPRM maturity |
| Aggregation & Portfolio Impact | 10% | Contribution to technology concentration (AWS/Azure/GCP, Microsoft 365, SAP, MSP); accumulation limits per cloud provider/MSP/software platform |

## Security Control Evaluation Table

| Control | Weight | Scoring |
|---------|--------|---------|
| MFA Deployment Scope | Critical | Binary pass/fail — must cover all admin, remote, email, cloud |
| EDR Coverage | Critical | <95% endpoints = sublimiting trigger |
| Backup Architecture | Critical | Air-gapped + immutable + quarterly tested = pass; any gap = conditional |
| Patch Cadence | High | Critical CVEs ≤14 days; high ≤30 days; medium ≤90 days |
| IR Plan Maturity | High | Documented + tabletop tested within 12 months = full credit |
| PAM Implementation | High | Least-privilege enforced; admin accounts inventoried; sessions recorded |
| Email Authentication | Medium | SPF + DKIM + DMARC at reject enforcement = full credit |
| Security Awareness Training | Medium | Quarterly phishing simulations; <5% click rate |
| Third-Party Risk Management | Medium | Vendor assessment program with critical vendor SLA monitoring |
| Board/Executive Cyber Governance | Medium | Dedicated committee or regular board reporting = full credit |
| External Scan Score | Medium | SecurityScorecard/BitSight ≥750 = favorable; <650 = adverse |
| Encryption | Medium | Full coverage of PII/PHI datastores and external communications |

## Loss Trend Data (Current Market)

| Metric | Figure | Source |
|--------|--------|--------|
| Ransomware share of incurred losses | 91% | Resilience H1 2025 |
| Average ransomware attack cost increase YoY | +17% | Resilience 2025 |
| BEC/FTF claim frequency share | 31% of claims | Coalition 2024 |
| Avg FTF recovery | $278K | Coalition 2024 |
| Double extortion % of large claims | 40% | Allianz 2025 |
| Average data breach cost | $4.88M | IBM 2024 |
| Breach detection lag (avg days) | 194 days | IBM 2024 |
| Global cyber market size (2024 U.S.) | $9.14B DPW; 4.3M policies | NAIC 2024 |
| Rate decline from mid-2022 peak | ~22% | Howden |
| Healthcare average claim loss | $1.3M | Resilience H1 2025 |
| Manufacturing ransomware share | 23.1% of claims | Resilience 2025 |
| Supply chain losses (manufacturing) | 46% of sector losses in 2024 | Resilience |

## Regulatory Requirements

| Requirement | Key Obligation |
|-------------|---------------|
| NAIC Model Law #668 (Insurance Data Security) | Adopted by 28 U.S. jurisdictions (as of Aug 2025); information security programs; 72-hour commissioner notification; annual compliance certification |
| NAIC Cyber Supplement | Annual reporting of DPW/earned, losses paid/incurred, defense costs, policy counts; eff. 2024: primary/excess/endorsement categorization |
| NAIC Model #670/672 | Consumer information and financial/health data privacy |
| NY DFS 23 NYCRR 500 | Pre-dates Model #668; CISO designation; penetration testing; audit trails; annual certification per §500.17(b); applies to all NY licensed entities |
| Lloyd's Market Bulletin Y5381 (Aug 2022) | All standalone cyber policies must exclude state-backed cyberattack losses; attribution mechanism required |
| LMA Model Clauses LMA5667A | Most widely adopted state-backed exclusion; four tiers (LMA5564–LMA5567) varying from total exclusion to narrower state-backed-only with bystanding asset coverage |
| SEC Item 1.05 Form 8-K (Jul 2023) | Public companies disclose material cyber incidents within 4 business days of materiality determination; creates D&O/cyber crossover |
| SEC Reg S-K Item 106 | Annual disclosure of cybersecurity risk management processes, board oversight, management roles |
| NIS2 Directive EU (eff. Oct 2024) | Expanded scope of entities requiring cybersecurity risk management; driving European cyber insurance demand |
| IAIS Cyber Risk Underwriting Guidance | Risk measurement, policy wording clarity, data taxonomy, supervisory reporting |
| OFAC Sanctions | Ransomware payment to sanctioned entities = civil liability; FinCEN SAR filing required; policy must include OFAC compliance provisions |
| Travelers v. International Control Services (2022) | Policy rescinded from inception for misrepresented MFA deployment; validates verify-not-accept underwriting approach |

## Process

### Step 1: Submission Intake & Triage
Receive: completed application, supplemental questionnaires (ransomware, cloud, privacy), 5-year loss runs, security architecture summary, outside-in scan results. Triage by revenue band: SME (<$100M), Mid-Market ($100M–$1B), Large/Complex (>$1B). Route to appropriate team and assign risk appetite tier.

### Step 2: Outside-In Technical Scan
Run automated external vulnerability assessment (SecurityScorecard, BitSight, or carrier-proprietary). Flag: open RDP ports, expired SSL certificates, unpatched critical CVEs visible externally, email authentication failures, dark web credential exposure. Cross-reference against application attestations — material discrepancy → senior underwriting referral.

### Step 3: Application Verification
Mid-Market and above: underwriting call with CISO or IT Director. Validate: MFA scope (every system, not just firewall), backup architecture (immutable, air-gapped, tested), EDR deployment %, PAM implementation, IR plan testing cadence. Large/Complex: request SOC 2 Type II, penetration test results (within 12 months), tabletop exercise documentation.

### Step 4: Exposure Modeling & Pricing
Technical premium via frequency × severity modeling calibrated to industry vertical, revenue, record count, security maturity score. Apply experience rating from loss history. Overlay portfolio-level accumulation loading. Set retention based on applicant's risk tolerance and security maturity — higher maturity earns lower retentions.

### Step 5: Coverage Structuring
Select policy form (claims-made vs. occurrence for BI). Set aggregate and per-occurrence limits. Apply sublimits: ransomware/extortion, regulatory proceedings, PCI fines/assessments, social engineering/FTF, dependent BI, reputational harm. Draft exclusion schedule: war/state-backed attack (per LMA5667A if applicable), infrastructure failure, prior known circumstances, willful non-compliance with stated controls.

### Step 6: Referral & Binding
Escalate submissions exceeding individual authority by limit, industry, or risk score. Document underwriting rationale including all guideline deviations. Bind and transmit to portfolio accumulation monitoring system.

### Step 7: Post-Bind Monitoring
Annual policies: mid-term outside-in scans; monitor for M&A activity, regulatory actions, new breach disclosures. At renewal: full reassessment, incorporate claims activity, adjust terms based on updated security posture.

## Glossary

| Term | Definition |
|------|-----------|
| Claims-Made Trigger | Coverage activates when claim first made during policy period regardless of when incident occurred |
| Retroactive Date | Earliest date from which incidents are covered; incidents before this date excluded |
| ERP / Tail | Extended Reporting Period; allows post-expiration claims for incidents during policy period; typically 1–3 years |
| Waiting Period (BI) | Hours after cyber incident before BI coverage attaches; functions as time-based deductible |
| Self-Insured Retention (SIR) | Dollar amount insured must pay before policy responds; insurer has no in-SIR obligation |
| Sublimit | Coverage cap within overall policy limit for specific grants (e.g., ransomware capped at $1M within $5M aggregate) |
| Silent / Non-Affirmative Cyber | Cyber exposure in traditional P/C policies neither explicitly covering nor excluding cyber; Lloyd's mandated elimination from Jan 2020 |
| War Exclusion (Cyber) | Excludes state-backed cyberattacks; requires explicit attribution mechanism post-Lloyd's Y5381 |
| Outside-In Scan | Automated external assessment of internet-facing assets without requiring internal access |
| PML (Probable Maximum Loss) | Estimated maximum portfolio-level loss from single cyber catastrophe at specified return period |
| Accumulation Risk | Correlated losses across policyholders from single event (cloud outage, zero-day, shared software) |
| Double Extortion | Ransomware combining encryption with data exfiltration; separate payment demands for each |
| FTF (Funds Transfer Fraud) | Loss from unauthorized electronic fund transfer via BEC or social engineering |
| Dependent / Contingent BI | Income loss from cyber event at third-party vendor/cloud provider, not insured's own systems |
| Breach Response Costs | First-party expenses: forensics, legal, notification, credit monitoring, PR |
| Regulatory Proceedings Coverage | Defense costs and, where insurable, fines/penalties from regulatory investigations post-incident |
| Betterment Exclusion | Prevents paying to upgrade systems beyond pre-loss state during restoration |
| Policy Rescission | Voiding contract from inception for material misrepresentation; treats policy as never having existed |
| Cyber Cat Bond | Insurance-linked security transferring cyber accumulation risk to capital markets; first issued 2023 |
| DMARC | Domain-based Message Authentication; prevents domain spoofing; "reject" enforcement = underwriting positive |
| Air-Gapped Backup | Backup infrastructure physically/logically isolated from production network; critical underwriting control |
| EDR | Endpoint Detection and Response; <95% coverage = sublimiting trigger |
| PAM | Privileged Access Management; controls and monitors elevated-permission accounts |

## Checklist

- [ ] MFA attestation validated against outside-in scan and confirmed via underwriting call — scope covers all admin, remote, email, cloud
- [ ] EDR deployment ≥95% of all endpoints confirmed; vendor and version documented
- [ ] Backup architecture verified as air-gapped/immutable with quarterly restoration testing evidence
- [ ] Outside-in scan cross-referenced against application responses — no material discrepancies
- [ ] Dark web credential check completed — active credentials found require remediation plan
- [ ] Accumulation analysis: cloud/MSP/SaaS dependencies mapped against portfolio concentration limits
- [ ] War/state-backed exclusion compliant with LMA5667A (if applicable); attribution mechanism specified
- [ ] Dependent BI exposure modeled with vendor-specific RTOs and waiting period alignment confirmed
- [ ] Sublimit adequacy reviewed for ransomware, FTF, regulatory proceedings, PCI fines vs. industry benchmarks
- [ ] OFAC sanctions compliance language included in policy; claims workflow includes sanctions screening
- [ ] Retroactive date appropriateness verified — no unintended coverage gaps from carrier switch
- [ ] SEC 8-K materiality intersection assessed for public company applicants — D&O/cyber cross-program exposure documented
- [ ] Industry-specific regulatory multiplier applied to per-record breach cost (HIPAA/PCI-DSS/GDPR/state AG)
- [ ] IR plan reviewed: documented, board-approved, tabletop tested within 12 months, communication protocols included
- [ ] Pricing reflects current loss trends: ransomware severity +17% YoY (Resilience 2025); BEC severity +23% YoY (Coalition 2024); avg breach cost $4.88M (IBM 2024)

## References
NAIC Cybersecurity Insurance Market Report Oct 2024, NAIC Model Law #668, NY DFS 23 NYCRR 500, Lloyd's Market Bulletin Y5381, LMA5667A, SEC Item 1.05 Form 8-K (Jul 2023)/Reg S-K Item 106, NIS2 Directive (Oct 2024), IAIS Cyber Risk Underwriting Guidance, Munich Re Cyber Trends 2025, Coalition 2025 Cyber Claims Report, Resilience Midyear 2025, Allianz Cyber Risk Trends 2025, IBM Cost of Data Breach 2024, NetDiligence 2025, Travelers v. ICS (2022), Cambridge Centre for Risk Studies/RMS Accumulation, OFAC FinCEN Ransomware Advisories
