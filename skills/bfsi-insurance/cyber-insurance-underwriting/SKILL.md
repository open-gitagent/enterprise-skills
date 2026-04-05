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

# Cyber Insurance Underwriting

## Domain Overview

Cyber insurance underwriting is the disciplined assessment of an organization's digital risk exposure to determine insurability, appropriate premium, coverage limits, retentions, and policy terms. The global cyber insurance market reached approximately $14 billion in 2023 and is projected to grow to $29 billion by 2027 (Munich Re). U.S. direct premiums written reached $9.14 billion in 2024, with more than 4.3 million policies in force. The market has entered a softening phase after the hard market of 2020–2022, with global rates declining approximately 22% from their mid-2022 peak (Howden). Despite rate softening, underwriting discipline remains paramount — ransomware accounted for 91% of incurred losses in Resilience's H1 2025 portfolio, and average ransomware attack costs rose 17% year-over-year even as claim frequency dropped 53%.

The underwriting function has fundamentally transformed from questionnaire-based risk selection to a technology-driven, continuous-assessment model. Carriers now deploy outside-in vulnerability scanning (e.g., SecurityScorecard, BitSight), API-based control verification, and AI-driven risk scoring to validate applicant attestations in real-time. The landmark *Travelers v. International Control Services* (2022) case — where a policy was rescinded from inception due to misrepresented MFA deployment — established that application accuracy is existential for both insurer and insured. Underwriters must now verify, not merely accept, security control attestations.

The regulatory landscape is multi-layered. The NAIC Insurance Data Security Model Law (#668), adopted by 28 U.S. jurisdictions as of August 2025, governs insurer data security obligations. The NAIC's Cybersecurity Insurance Supplement mandates annual reporting of premiums, losses, and claims data, now split into primary/excess/endorsement categories (effective 2024). Lloyd's Market Bulletin Y5381 requires all standalone cyber policies incepted after March 31, 2023, to contain state-backed cyberattack exclusions. The SEC's July 2023 cybersecurity disclosure rules (Item 1.05 Form 8-K) create D&O crossover exposure that directly affects cyber policy structuring. The EU's NIS2 Directive, effective October 2024, is driving cyber insurance demand across European operations.

Accumulation and systemic risk remain the industry's defining challenge. Unlike property catastrophe, where geographic proximity drives correlation, cyber accumulation arises from shared technology dependencies — a single cloud provider outage, zero-day exploit, or supply chain compromise can trigger thousands of simultaneous claims. The first dedicated cyber catastrophe bond was issued in 2023, with additional issuances in 2024, signaling growing institutional approaches to capacity management.

## Core Decision Framework

Experienced cyber underwriters evaluate submissions across five interconnected dimensions, weighted by the applicant's industry, revenue band, and data sensitivity:

**1. Security Maturity Assessment (40% of decision weight)**
Map the applicant's controls against NIST CSF 2.0 functions (Govern, Identify, Protect, Detect, Respond, Recover) or CIS Controls v8. Non-negotiable baseline controls in 2024–2025: MFA on all privileged/remote/email access, EDR on all endpoints, encrypted and air-gapped backups tested quarterly, Privileged Access Management (PAM) enforced, patch management within 30 days for critical CVEs, email authentication (SPF/DKIM/DMARC), and a documented/tested Incident Response plan. Absence of any single baseline control is grounds for declination or sublimiting.

**2. Exposure Quantification (25% of decision weight)**
Calculate first-party and third-party exposure based on: record count (PII/PHI/PCI), annual revenue for business interruption modeling, technology dependency mapping (cloud providers, MSPs, SaaS platforms), regulatory jurisdiction (multi-state, GDPR, HIPAA, PCI-DSS), and third-party vendor criticality. Healthcare applicants carry average claim losses of $1.3 million; manufacturing sees 23.1% of all ransomware claims.

**3. Claims and Loss History (15% of decision weight)**
Evaluate prior incidents, response quality, and remediation completeness. A ransomware event within 24 months where the root cause was not remediated is a hard declination trigger. Prior claims-made policy history gaps create coverage continuity risk. Assess whether the applicant has filed regulatory notifications under applicable breach laws.

**4. Governance and Human Factors (10% of decision weight)**
Board-level cyber oversight, CISO reporting structure, security awareness training frequency and phishing simulation results, third-party risk management program maturity, and regulatory compliance posture. SEC disclosure rules now require public companies to identify specific cyber-responsible officers — underwriters should verify this governance exists.

**5. Aggregation and Portfolio Impact (10% of decision weight)**
Assess the submission's contribution to portfolio-level technology concentration risk. Shared cloud infrastructure (AWS, Azure, GCP), common software vendors (Microsoft 365, SAP), and MSP dependencies create correlated loss scenarios. Underwriters maintain Technology Dependency Maps at the portfolio level and apply accumulation limits per cloud provider, per MSP, and per software platform.

## Step-by-Step Process

**Step 1: Submission Intake and Triage**
Receive broker submission package: completed application, supplemental questionnaires (ransomware, cloud, privacy), loss runs (5 years), current security architecture summary, and outside-in scan results. Triage by revenue band: SME (<$100M), Mid-Market ($100M–$1B), Large/Complex (>$1B). Route to appropriate underwriting team and assign risk appetite tier.

**Step 2: Outside-In Technical Scan**
Run automated external vulnerability assessment using SecurityScorecard, BitSight, or carrier-proprietary tooling. Flag: open RDP ports, expired SSL certificates, unpatched critical CVEs visible externally, email authentication failures, dark web credential exposure. Cross-reference scan findings against application attestations — any material discrepancy triggers a referral to senior underwriting.

**Step 3: Application Verification**
For Mid-Market and above: conduct underwriting call with the applicant's CISO or IT Director. Validate MFA scope (every system, not just firewall), backup architecture (immutable, air-gapped, tested), EDR deployment percentage, PAM implementation, and IR plan testing cadence. For Large/Complex: request SOC 2 Type II report, penetration test results (within 12 months), and tabletop exercise documentation.

**Step 4: Exposure Modeling and Pricing**
Calculate technical premium using frequency × severity modeling calibrated to industry vertical, revenue, record count, and security maturity score. Apply experience rating based on loss history. Overlay portfolio-level accumulation loading. Set retention/deductible based on applicant's risk tolerance and security maturity — higher maturity earns lower retentions. Apply Large Loss Development factors for claims-made tail.

**Step 5: Coverage Structuring**
Select policy form (claims-made vs. occurrence trigger for BI), set aggregate and per-occurrence limits, apply sublimits for: ransomware/extortion, regulatory proceedings, PCI fines and assessments, social engineering/funds transfer fraud, dependent business interruption, reputational harm. Draft exclusion schedule: war/state-backed cyberattack (per Lloyd's Y5381 if applicable), infrastructure failure, prior known circumstances, willful non-compliance with stated controls.

**Step 6: Referral and Binding Authority**
Submissions exceeding individual authority (by limit, industry, or risk score) escalate to referral underwriter or Chief Underwriting Officer. Document underwriting rationale including all deviations from guidelines. Bind coverage, issue policy, and transmit to portfolio accumulation monitoring system.

**Step 7: Post-Bind Monitoring**
For annual policies: conduct mid-term outside-in scans, monitor for material changes in risk profile (M&A activity, regulatory actions, new breach disclosures). At renewal: re-run full assessment, incorporate any claims activity, adjust terms based on updated security posture.

## Evaluation Criteria

| Factor | Weight | Scoring Method |
|--------|--------|----------------|
| MFA Deployment Scope | Critical | Binary pass/fail — must cover all admin, remote, email, and cloud access |
| EDR Coverage | Critical | Percentage of endpoints; <95% triggers sublimiting |
| Backup Architecture | Critical | Air-gapped + immutable + tested quarterly = pass; any gap = conditional |
| Patch Cadence | High | Critical CVEs within 14 days, high within 30 days, medium within 90 days |
| IR Plan Maturity | High | Documented + tested via tabletop within 12 months = full credit |
| PAM Implementation | High | Least-privilege enforced, admin accounts inventoried, session recorded |
| Email Authentication | Medium | SPF + DKIM + DMARC at enforcement = full credit |
| Security Awareness Training | Medium | Quarterly phishing simulations with <5% click rate |
| Third-Party Risk Management | Medium | Vendor assessment program with critical vendor SLA monitoring |
| Board/Executive Cyber Governance | Medium | Dedicated committee or regular board reporting = full credit |
| External Scan Score | Medium | SecurityScorecard/BitSight score ≥ 750 = favorable; < 650 = adverse |
| Encryption at Rest and in Transit | Medium | Full coverage of PII/PHI datastores and all external communications |

## Red Flags & Edge Cases

1. **MFA "Firewall-Only" Attestation**: Applicant marks MFA as "implemented" but deploys it only on the firewall, not on servers, cloud applications, or remote access. This is the exact fact pattern in *Travelers v. ICS* (2022) that resulted in policy rescission from inception. Validate MFA scope explicitly during underwriting calls.

2. **MSP Single-Point-of-Failure**: Applicant outsources all IT management to a single MSP with no direct access to their own backups or security tooling. A ransomware attack on the MSP (e.g., Kaseya VSA, 2021) triggers simultaneous claims across hundreds of the MSP's clients — a portfolio-level accumulation event.

3. **Healthcare Double Extortion Escalation**: Healthcare applicants face extortion demands reaching $4 million (Resilience H1 2025 data). Threat actors specifically target organizations where patient safety creates payment leverage. Standard ransomware sublimits of $1M–$2M are inadequate for large health systems.

4. **Silent Cyber Bleed-Through on Package Policies**: Endorsement-based cyber coverage on commercial property or GL policies may not contain the same exclusionary precision as standalone forms. The NAIC reported endorsement policies comprise ~55% of all cyber policies but only 35% of premium volume — indicating thinner coverage that may create E&O exposure for the carrier when claims arise.

5. **War Exclusion Attribution Ambiguity**: Lloyd's LMA5667A exclusion requires attribution of cyberattacks to state actors. NotPetya (2017) was attributed to Russian military intelligence, but early assessments were uncertain. Underwriters must ensure attribution clauses specify which entity (government, intelligence community) makes the determination and the evidentiary standard applied.

6. **SEC 8-K Materiality Determination Mismatch**: A public company policyholder determines a cyber incident is not "material" under SEC rules but later faces shareholder derivative litigation arguing it was. This triggers D&O coverage, not cyber — unless the cyber policy has a regulatory proceedings insuring agreement. Cross-program correlation (cyber + D&O) for the same event can double carrier exposure.

7. **Supply Chain Dependent BI Without Waiting Period Alignment**: Applicant's policy includes dependent/contingent business interruption coverage but the waiting period (e.g., 12 hours) doesn't align with the applicant's RTO for critical vendor dependencies. A 72-hour vendor outage with a 12-hour waiting period creates 60 hours of covered BI — underwriters must model this exposure accurately.

8. **Credential Exposure on Dark Web Pre-Binding**: Outside-in scan reveals thousands of employee credentials on dark web marketplaces. Applicant may already be compromised (pre-existing condition). Binding coverage without requiring credential reset and enhanced monitoring exposes the carrier to claims from incidents already in progress.

9. **Ransomware Payment Sanctions Compliance**: OFAC sanctions prohibit payments to designated entities. An insured paying ransom to a sanctioned group (e.g., formerly active groups like Evil Corp) creates sanctions violation risk for both insured and carrier. Policy language must include OFAC compliance clauses, and the claims process must include sanctions screening.

10. **CrowdStrike-Type Non-Malicious Outage**: The July 2024 CrowdStrike Falcon update failure caused global IT outages. Policies covering only "malicious" cyber events would exclude this. The NAIC noted that insurers in 2024 increasingly incorporated non-malicious system failure triggers for BI coverage. Underwriters must clearly define whether system failure (non-malicious) is covered or excluded.

11. **Retroactive Date Manipulation at Renewal**: Insured switches carriers at renewal. New carrier offers a retroactive date equal to the new policy inception, eliminating coverage for claims arising from incidents that occurred during the prior policy period but are reported during the new one. This creates a coverage gap the insured may not recognize until claim time.

12. **AI-Generated Social Engineering Deepfakes**: Threat actors using AI-generated voice/video deepfakes to authorize fraudulent wire transfers. Funds Transfer Fraud (FTF) sublimits averaging $250K are often insufficient — Coalition reported average FTF recoveries of $278K in 2024, implying many losses exceed sublimits.

## Common Mistakes

**Accepting Application Attestations at Face Value**: The single most consequential underwriting error. Post-loss investigation frequently reveals gaps between attested and actual control implementation. Carriers that do not independently validate at least MFA, EDR, and backup claims via outside-in scanning or underwriting interviews carry elevated rescission and claims risk.

**Underpricing Dependent Business Interruption**: Contingent BI from vendor/cloud outages is the fastest-growing loss category. Supply chain compromises accounted for 46% of manufacturing sector losses in 2024 (Resilience). Many underwriters price this as a sublimited add-on rather than a primary exposure driver.

**Ignoring Industry-Specific Regulatory Multipliers**: A data breach affecting 500+ medical records triggers HIPAA Breach Notification Rule and potential OCR enforcement. The same record count in retail triggers state AG investigations under varying breach notification laws. Per-record costs vary 3x–5x between sectors, but many rating models apply uniform per-record costs.

**Failing to Stress-Test Accumulation Models**: Cyber catastrophe models remain immature relative to natural catastrophe models. The Cambridge Centre for Risk Studies and RMS note that identifying correlation in cyber portfolios requires domain expertise in technology dependency mapping — not geographic proximity. Underwriters who rely solely on vendor models without supplementing with internal dependency analysis underestimate tail risk.

**Setting Retentions Too Low for Immature Insureds**: Low retentions on accounts with weak security controls incentivize moral hazard and attract adverse selection. The retention should reflect the applicant's "skin in the game" — immature accounts should carry higher retentions to align insurer-insured incentives.

**Neglecting Claims-Made Tail Exposure**: Cyber policies are predominantly claims-made. Failure to properly manage retroactive dates, extended reporting periods, and prior acts coverage creates gaps that surface years after underwriting decisions. The lag between breach occurrence and discovery averages 194 days (IBM Cost of a Data Breach Report 2024).

## Regulatory & Compliance Requirements

### NAIC Framework
- **Model Law #668 (Insurance Data Security Model Law)**: Adopted by 28 jurisdictions (as of August 2025). Requires licensees to maintain information security programs, investigate cybersecurity events, and notify commissioners within 72 hours. Imposes annual certification of compliance on domestic insurers. Carriers writing cyber insurance must themselves comply with #668 in adopted states.
- **NAIC Cyber Supplement**: Mandates annual reporting of direct premiums written/earned, direct losses paid/incurred, defense costs, and policy counts. Effective 2024, reporting shifted from stand-alone/packaged to primary/excess/endorsement categorization. Identity theft supplement discontinued.
- **NAIC Model #670 (Insurance Information and Privacy Protection Act)**: Governs consumer information disclosure practices.
- **NAIC Model #672 (Privacy of Consumer Financial and Health Information)**: Regulates financial/health data privacy for insurance transactions.

### New York DFS
- **23 NYCRR 500**: Pre-dates Model #668 and served as its template. Requires covered entities to maintain cybersecurity programs, designate a CISO, conduct penetration testing, maintain audit trails, and submit annual certifications under Section 500.17(b). Applies to all entities licensed under NY Banking, Insurance, or Financial Services Law.

### Lloyd's / London Market
- **Market Bulletin Y5381 (August 2022)**: All standalone cyber policies must exclude losses from state-backed cyberattacks. Exclusions must address war, state function impairment, and attribution mechanisms.
- **LMA Model Clauses**: LMA5564–LMA5567 (original), LMA5667A (most widely adopted). Four tiers of exclusion stringency, from total cyber operation exclusion (LMA5564) to narrower state-backed-only exclusion with bystanding asset coverage (LMA5567).

### SEC Cybersecurity Disclosure Rules (July 2023)
- **Item 1.05 Form 8-K**: Public companies must disclose material cybersecurity incidents within four business days of materiality determination. Creates D&O/cyber coverage intersection — the same incident can trigger cyber first-party claims and securities class action D&O claims simultaneously.
- **Regulation S-K Items 106**: Annual disclosure of cybersecurity risk management processes, board oversight, and management roles.

### International
- **NIS2 Directive (EU)**: Effective October 2024, expanding scope of entities required to maintain cybersecurity risk management. Driving European cyber insurance demand and influencing underwriting requirements for EU-exposed risks.
- **IAIS Cyber Risk Underwriting Guidance**: Published by the International Association of Insurance Supervisors, addressing risk measurement, policy wording clarity, data taxonomy development, and supervisory reporting on cyber exposure.

### OFAC Sanctions Compliance
- Ransomware payment facilitation to sanctioned entities creates civil liability under OFAC regulations. Treasury's FinCEN issued advisories requiring financial institutions (including insurers) to file SARs on ransomware-related payments. Underwriters must ensure policy language includes OFAC compliance provisions and claims workflows include sanctions screening.

## Terminology

- **Claims-Made Trigger**: Coverage activates when a claim is first made against the insured during the policy period, regardless of when the underlying incident occurred (subject to retroactive date). Dominant trigger mechanism in cyber insurance.
- **Retroactive Date**: The earliest date from which incidents are covered under a claims-made policy. Incidents occurring before this date are excluded regardless of when reported.
- **Extended Reporting Period (ERP / Tail)**: Optional coverage extension allowing claims to be reported after policy expiration for incidents occurring during the policy period. Typically 1–3 years; critical for M&A scenarios.
- **Waiting Period (BI)**: The number of hours after a cyber incident before business interruption coverage attaches. Functions as a time-based deductible. Typical ranges: 8–24 hours.
- **Self-Insured Retention (SIR)**: Dollar amount the insured must pay before the policy responds. Unlike a deductible, the insurer has no obligation to manage or pay within the SIR.
- **Sublimit**: A coverage cap within the overall policy limit applying to specific coverage grants (e.g., ransomware payments capped at $1M within a $5M aggregate).
- **Silent Cyber / Non-Affirmative Cyber**: Cyber exposure embedded in traditional property/casualty policies that neither explicitly covers nor excludes cyber events. Lloyd's mandated elimination of silent cyber starting January 2020.
- **War Exclusion (Cyber)**: Exclusion of losses arising from state-backed cyberattacks or cyber operations conducted as part of armed conflict. Post-Lloyd's Y5381, requires explicit attribution mechanisms.
- **Outside-In Scan**: Automated external assessment of an organization's internet-facing assets to identify vulnerabilities, misconfigurations, and exposed services without requiring internal access.
- **Probable Maximum Loss (PML)**: The estimated maximum portfolio-level loss from a single cyber catastrophe scenario at a specified return period. Central to accumulation management.
- **Accumulation Risk**: The risk that a single cyber event (e.g., cloud provider outage, zero-day exploit) triggers correlated losses across many policyholders simultaneously.
- **Double Extortion**: Ransomware attack strategy combining data encryption with data exfiltration, demanding separate payments for decryption and non-publication. 40% of large cyber claims in H1 2025 involved data theft (Allianz).
- **Funds Transfer Fraud (FTF)**: Loss resulting from unauthorized electronic transfer of funds, typically through BEC or social engineering. Accounted for 31% of cyber claims in 2024 (Coalition).
- **Dependent/Contingent Business Interruption**: Coverage for income loss caused by a cyber event affecting a third-party vendor, cloud provider, or supply chain partner rather than the insured's own systems.
- **Breach Response Costs**: First-party expenses including forensic investigation, legal counsel, notification costs, credit monitoring, and public relations. Triggered upon discovery of a security or privacy event.
- **Regulatory Proceedings Coverage**: Insuring agreement covering defense costs and, where insurable, fines/penalties arising from regulatory investigations following a cyber incident.
- **Betterment Exclusion**: Exclusion preventing the insurer from paying to upgrade systems beyond their pre-loss state during restoration — only restoration to equivalent functionality is covered.
- **Policy Rescission**: Voiding of the insurance contract from inception due to material misrepresentation in the application. Distinguished from claim denial or exclusion — rescission treats the policy as never having existed.
- **Cyber Catastrophe Bond (Cat Bond)**: Insurance-linked security transferring cyber accumulation risk to capital markets. First issued in 2023; growing mechanism for expanding market capacity beyond traditional reinsurance.
- **DMARC (Domain-based Message Authentication)**: Email authentication protocol that builds on SPF and DKIM to prevent domain spoofing. Deployment at "reject" enforcement level is an underwriting positive.
- **Air-Gapped Backup**: Backup infrastructure physically or logically isolated from the production network, preventing ransomware from encrypting backup data. Considered a critical underwriting control.
- **Endpoint Detection and Response (EDR)**: Security solution providing continuous monitoring, threat detection, and automated response on endpoint devices. Deployed EDR with <95% coverage is a sublimiting trigger.
- **Privileged Access Management (PAM)**: Framework controlling and monitoring access for accounts with elevated system permissions. Prevents lateral movement during breaches.

## Quality Checklist

1. ☐ MFA attestation validated against outside-in scan results and confirmed via underwriting call — scope covers all admin, remote, email, and cloud access
2. ☐ EDR deployment percentage confirmed ≥95% of all endpoints, with vendor and version documented
3. ☐ Backup architecture verified as air-gapped/immutable with quarterly restoration testing evidence
4. ☐ Outside-in vulnerability scan completed and cross-referenced against application responses — no material discrepancies
5. ☐ Dark web credential exposure check completed — remediation plan required if active credentials found
6. ☐ Accumulation analysis performed — technology dependencies (cloud, MSP, SaaS) mapped and checked against portfolio concentration limits
7. ☐ War/state-backed cyberattack exclusion compliant with Lloyd's Y5381 (if applicable) or carrier-equivalent, with attribution mechanism specified
8. ☐ Dependent BI exposure modeled with vendor-specific RTOs and waiting period alignment confirmed
9. ☐ Sublimit adequacy reviewed for ransomware, FTF, regulatory proceedings, and PCI fines relative to industry benchmarks
10. ☐ OFAC sanctions compliance language included in policy; claims workflow includes sanctions screening step
11. ☐ Retroactive date appropriateness verified — no unintended coverage gaps from carrier switches
12. ☐ SEC 8-K disclosure intersection assessed for public company applicants — D&O/cyber cross-program exposure documented
13. ☐ Industry-specific regulatory multiplier applied to per-record breach cost assumptions (HIPAA, PCI-DSS, GDPR, state AG)
14. ☐ Incident Response plan reviewed for completeness: documented, board-approved, tested via tabletop within 12 months, includes communication protocols
15. ☐ Pricing reflects current loss trends: ransomware severity +17% YoY (Resilience 2025), BEC severity +23% YoY (Coalition 2024), average breach cost $4.88M (IBM 2024)

## References

1. NAIC, "Report on the Cybersecurity Insurance Market" (October 2024) — https://content.naic.org/sites/default/files/cmte-h-cyber-wg-2024-cyber-ins-report.pdf
2. NAIC, "Insurance Data Security Model Law #668 — Compliance & Enforcement Guide" (2025) — https://content.naic.org/sites/default/files/call_materials/Attachment%20B2-IDSM%20Compliance%20Guide%20v6_Clean%20Copy-combined.pdf
3. NAIC, "Innovation, Cybersecurity, and Technology (H) Committee 2025 Proposed Charges" — https://content.naic.org/sites/default/files/inline-files/_033_H-Cmte-2025-Proposed-Charges-Exposure-Draft_Posted_1.pdf
4. NAIC, "Model Law State Page #668" (Summer 2025) — https://content.naic.org/sites/default/files/model-law-state-page-668.pdf
5. NAIC, "Insurance Topics: Cybersecurity" — https://content.naic.org/insurance-topics/cybersecurity
6. NAIC, "Catastrophe Modeling Primer" (March 2025) — https://content.naic.org/sites/default/files/committees-pending-action-cat-mod-primer.pdf
7. Lloyd's Market Bulletin Y5381, "State-Backed Cyberattack Exclusions" — https://www.cliffordchance.com/insights/resources/blogs/insurance-insights/2023/09/lloyds-cyber-war-exclusion.html
8. WTW, "War Exclusions in Cyber Policies: The Important Details" (June 2023) — https://www.wtwco.com/en-us/insights/2023/06/war-exclusions-in-cyber-policies-the-important-details
9. IAIS, "Cyber Risk Underwriting: Identified Challenges and Supervisory Considerations" — https://www.iais.org/uploads/2022/01/201229-Cyber-Risk-Underwriting_-Identified-Challenges-and-Supervisory-Considerations-for-Sustainable-Market-Development.pdf
10. Munich Re, "Cyber Insurance: Risks and Trends 2025" — https://www.munichre.com/en/insights/cyber/cyber-insurance-risks-and-trends-2025.html
11. Munich Re, "Cyber Insurance: Risks and Trends 2024" — https://www.munichre.com/en/insights/cyber/cyber-insurance-risks-and-trends-2024.html
12. Coalition, "2025 Cyber Claims Report" — https://www.coalitioninc.com/blog/cyber-insurance/2025-cyber-claims-report
13. Resilience, "Midyear 2025 Cyber Risk Report" — https://cyberresilience.com/newsroom/press-release/pr_2025_cyber_risk_report/
14. Allianz Commercial, "Cyber Risk Trends 2025" — https://commercial.allianz.com/news-and-insights/news/cyber-risk-trends-2025.html
15. NetDiligence, "Cyber Claims Study 2025 Report" — https://rsmus.com/content/dam/rsm/insights/services/risk-fraud-cybersecurity/1pdf/net-diligence-cyber-claims-study-2025-report.inline.pdf
16. Lockton, "Travelers v. ICS Underscores Need to Respond Carefully to Cyber Insurance Applications" — https://global.lockton.com/us/en/news-insights/travelers-v-ics-underscores-need-to-respond-carefully-to-cyber-insurance
17. National Law Review, "The Impact of Travelers v. ICS for Cyber Insurance Brokers" — https://natlawreview.com/article/practical-implications-travelers-v-ics-cyber-insurance-brokers-carriers-and
18. Reed Smith, "Insurance Coverage Implications of SEC's Cybersecurity Disclosure Rules" — https://www.reedsmith.com/our-insights/blogs/the-policyholder-perspective/102k347/insurance-coverage-implications-of-secs-cybersecurity-disclosure-rules/
19. Directors & Boards, "D&O Liability and the SEC Cyber Rules" — https://www.directorsandboards.com/board-issues/cyber-risk/do-liability-and-the-sec-cyber-rules/
20. American Academy of Actuaries, "SEC Cybersecurity Disclosure Requirements and Related D&O Implications" — https://actuary.org/wp-content/uploads/2025/05/Casualty-Brief-SEC-Cyber.pdf
21. American Academy of Actuaries, "Cyber Risk Resource Guide" — https://actuary.org/wp-content/uploads/2024/10/ResourceGuide.pdf
22. Cambridge Centre for Risk Studies / RMS, "Managing Cyber Insurance Accumulation Risk" — https://www.jbs.cam.ac.uk/wp-content/uploads/2020/08/crs-rms-managing-cyber-insurance-accumulation-risk.pdf
23. Geneva Association, "Cyber Risk Accumulation: Fully Tackling the Insurability Challenge" — https://www.genevaassociation.org/sites/default/files/2023-11/Cyber%20Accumulation%20summary_WEB.pdf
24. EY, "Cybersecurity Insurance — A Beginner's Guide" — https://www.ey.com/content/dam/ey-unified-site/ey-com/en-us/campaigns/ciso/documents/ey-cybersecurity-insurance-a-beginners-guide.pdf
25. IRMI, "End of Silent Cyber in Property Insurance" — https://www.irmi.com/articles/expert-commentary/end-of-silent-cyber-in-property-insurance
26. Daniel Woods, "Where Are the Insurance Disputes Over Cyber Hygiene?" (March 2024) — https://www.danielwoods.info/blog/2024/cyber-hygiene-exclusions/
27. Secnap, "The 2025 Guide to Cyber Insurance" — https://www.secnap.com/cyber-crime-news/the-2025-guide-to-cyber-insurance-navigating-the-new-reality-of-cyber-risk/
28. DeepStrike, "Cyber Insurance Statistics 2025" — https://deepstrike.io/blog/cyber-insurance-statistics-2025