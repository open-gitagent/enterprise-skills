---
name: vendor-discovery-agent
description: >
  Identifies potential vendors based on requirements including industry analysis, capability matching, geographic coverage, and market intelligence gathering.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "FAR, UCC, ISM"
---

# Vendor Discovery

## Domain Overview

Vendor discovery is the upstream phase of strategic sourcing where procurement identifies, screens, and narrows the universe of potential suppliers capable of fulfilling a defined business need. It sits between the "define requirement" and "RFx execution" stages of the CIPS 13-stage procurement cycle, mapping specifically to stages 4 (pre-procurement market testing) through 6 (supplier selection/prequalification). Unlike vendor management — which governs ongoing supplier relationships — discovery operates in ambiguity: the buying organization may not know who is in the market, what capacity exists, or which geographies offer viable alternatives. The skill required is equal parts market intelligence, risk sensing, and structured elimination.

The discipline has undergone fundamental transformation since 2022. Traditional discovery methods — trade shows, broker networks, incumbent referrals, and manual web research — are being displaced by AI-powered supplier intelligence platforms such as Veridion, Tealbook, and Scoutbee, which crawl firmographic, financial, and ESG data across millions of entities globally. According to Spend Matters' 2025 analysis, the category analytics and intelligence market now includes specialized vendor discovery modules that merge spend data, market intelligence, and supplier enrichment into unified workflows. However, technology alone does not solve the core challenge: determining whether a discovered entity can actually deliver reliably, ethically, and at acceptable total cost of ownership.

Regulatory pressure has sharpened the compliance dimension of discovery. The EU Corporate Sustainability Due Diligence Directive (CSDDD, Directive 2024/1760), effective with phased adoption beginning July 2027, requires in-scope companies to identify and mitigate adverse human rights and environmental impacts across their value chains — meaning discovery cannot be separated from ESG screening. The U.S. Uyghur Forced Labor Prevention Act (UFLPA) creates a rebuttable presumption that goods from China's Xinjiang region are made with forced labor, requiring importers to trace supply chains to the entity level during discovery. The German Lieferkettensorgfaltspflichtengesetz (LkSG) imposes analogous obligations for German companies with 1,000+ employees.

Supply chain resilience has elevated vendor discovery from a cost-optimization exercise to a strategic capability. Organizations pursuing nearshoring, friendshoring, and China+1 strategies need discovery processes that systematically map alternative supplier ecosystems in target geographies. The Kraljic Matrix remains the foundational framework for prioritizing which categories warrant deep discovery investment: strategic items (high profit impact, high supply risk) demand exhaustive global searches, while routine items may rely on catalog aggregators or e-procurement marketplaces. Category managers who treat all discovery equally waste resources and miss time-sensitive sourcing windows.

## Core Decision Framework

### The Kraljic-Informed Discovery Intensity Model

The depth of vendor discovery effort should scale directly with the Kraljic quadrant of the category being sourced:

**Strategic Items** (high supply risk, high profit impact): Execute full-spectrum global discovery. Deploy AI-powered supplier intelligence platforms, engage specialist sourcing consultants, conduct site visits to top candidates, and run deep due diligence including financial health (D&B Supplier Risk Score), sanctions screening (OFAC SDN), ESG assessment (EcoVadis), and operational audits. Target: identify 15-30 potential vendors, shortlist 5-8 for RFP.

**Leverage Items** (low supply risk, high profit impact): Focus discovery on competitive intensity. The goal is finding enough qualified vendors to create competitive tension. Use spend analysis to identify alternative suppliers already active in adjacent categories. Target: 8-15 potential vendors, shortlist 3-5 for competitive bidding.

**Bottleneck Items** (high supply risk, low profit impact): Prioritize supply security over cost. Discovery focuses on finding any viable alternatives to reduce single-source dependency. Explore substitute materials/technologies, adjacent industries, and non-traditional suppliers. Target: 3-8 potential vendors, qualify 2-3 as backup sources.

**Routine Items** (low supply risk, low profit impact): Minimize discovery effort. Use catalog purchasing, GPO agreements, or marketplace aggregators. Discovery is triggered only by incumbent failure or contract expiration. Target: validate 2-3 options through marketplace data.

### The Three Lenses of Discovery

Every potential vendor must be evaluated through three concurrent lenses before advancing from longlist to shortlist:

1. **Capability Fit**: Can they make/deliver what we need, at the volume we need, with the quality we require? Verify through UNSPSC code matching, capability statements, references, and production capacity data.

2. **Risk Profile**: Do they introduce unacceptable financial, operational, geographic, regulatory, or reputational risk? Screen against sanctions lists, check financial viability (D&B PAYDEX, credit ratings), validate entity legitimacy, and assess country risk.

3. **Strategic Alignment**: Do they advance or hinder the organization's broader objectives — sustainability targets, diversity commitments, total cost reduction, innovation partnerships, or geographic diversification strategies?

## Step-by-Step Process

### Step 1: Define the Discovery Brief
- Translate the business requirement into a supplier-facing specification
- Classify the category using UNSPSC codes (4-digit segment minimum; 8-digit commodity for precision)
- Determine Kraljic quadrant to set discovery intensity
- Document mandatory vs. desirable attributes (certifications, geographies, capacity thresholds, diversity status)
- Identify deal-breakers upfront: prohibited countries, minimum revenue thresholds, required ISO certifications

### Step 2: Conduct Spend and Supply Market Analysis
- Analyze historical spend data to identify current suppliers, spend fragmentation, and maverick spend
- Map the supply market structure: oligopoly, fragmented, regional clusters, vertically integrated
- Identify market trends: capacity utilization rates, input cost trajectories, M&A activity, technology shifts
- Determine the realistic number of viable suppliers globally for this category
- Tools: Sievo, GEP SMART, JAGGAER Category Intelligence, ProcurementIQ

### Step 3: Execute Multi-Channel Supplier Identification
- **AI-Powered Platforms**: Veridion (400M+ global company profiles), Tealbook (supplier data enrichment via NLP), Scoutbee (ML-based supplier matching)
- **Procurement Networks**: SAP Ariba Discovery, Coupa Supplier Network, Amazon Business
- **Industry Sources**: Trade associations, industry exhibitions, trade publications, patent databases
- **Government Registries**: SAM.gov (U.S. federal), Contracts Finder (UK), TED/eSender (EU)
- **Referral Networks**: Existing supplier referrals, category consultants, peer procurement networks (ISM, CIPS)
- **Direct Research**: Company websites, LinkedIn Sales Navigator, financial filings, Crunchbase for startups
- Document the source of each identified vendor for audit trail purposes

### Step 4: Apply First-Pass Screening Filters
- Sanctions and denied-party screening: OFAC SDN List, EU Consolidated List, UN Security Council List
- Entity verification: Confirm legal existence, active registration, D-U-N-S Number validation
- Geographic compliance: Screen against UFLPA Entity List, conflict minerals (Dodd-Frank §1502), country sanctions
- Minimum threshold filters: Revenue floor, years in business, employee count, required certifications
- Diversity certification verification: SBA certifications (8(a), HUBZone, WOSB, SDVOSB), NMSDC (MBE), WBENC (WBE)
- Output: Reduce initial universe (50-200 entities) to a qualified longlist (15-30 entities)

### Step 5: Issue Request for Information (RFI) / Supplier Qualification Questionnaire (SQQ)
- Deploy standardized questionnaire covering: company profile, financial health, technical capability, quality management, ESG practices, references, insurance coverage, IT security posture
- Include category-specific technical questions (e.g., production processes, raw material sourcing, testing capabilities)
- Set clear response deadline (typically 10-15 business days) and format requirements
- Pre-populate known data fields from discovery platforms to reduce supplier burden

### Step 6: Evaluate RFI Responses and Score
- Apply weighted scoring model (see Evaluation Criteria below)
- Cross-reference self-reported data against third-party sources (D&B, EcoVadis, Resilinc, public filings)
- Flag inconsistencies between claimed capabilities and verifiable evidence
- Conduct preliminary financial health assessment using D&B Supplier Evaluation Risk (SER) rating or equivalent
- Output: Reduce longlist to shortlist of 3-8 vendors for RFP/RFQ

### Step 7: Validate and Enrich Shortlist
- Request and verify references from comparable customers
- Conduct virtual or in-person capability assessments for strategic categories
- Run enhanced due diligence on beneficial ownership (especially for sub-$50M revenue entities)
- Validate production capacity claims against industry benchmarks
- Confirm insurance coverage adequacy (general liability, professional indemnity, product liability, cyber)
- Obtain EcoVadis scorecard or equivalent sustainability assessment for ESG-sensitive categories

### Step 8: Produce Discovery Output Package
- Compiled shortlist with structured profiles (standardized data fields across all candidates)
- Risk heat map showing comparative risk profiles
- Capability comparison matrix
- Recommended next steps (RFP structure, evaluation panel composition, timeline)
- Discovery audit trail documenting methodology, sources, and elimination rationale

## Evaluation Criteria

### Weighted Scoring Model (Adapt weights to category Kraljic quadrant)

| Criterion | Strategic | Leverage | Bottleneck | Routine |
|-----------|-----------|----------|------------|---------|
| Technical Capability & Fit | 25% | 20% | 30% | 15% |
| Financial Stability | 20% | 10% | 25% | 10% |
| Quality Systems (ISO 9001, AS9100, IATF 16949) | 15% | 15% | 15% | 10% |
| Total Cost of Ownership | 10% | 30% | 5% | 35% |
| ESG/Sustainability Performance | 10% | 5% | 5% | 5% |
| Supply Chain Risk & Resilience | 10% | 5% | 15% | 5% |
| Innovation & Continuous Improvement | 5% | 5% | 0% | 0% |
| Diversity & Inclusion Status | 5% | 10% | 5% | 20% |

### Financial Health Thresholds
- **Green**: D&B SER Rating 1-2, PAYDEX 80+, positive working capital, current ratio >1.5
- **Yellow**: D&B SER Rating 3, PAYDEX 60-79, thin margins but positive cash flow
- **Red**: D&B SER Rating 4-5, PAYDEX <60, negative working capital, material litigation, recent credit downgrades
- **Disqualify**: Active bankruptcy proceedings, unresolved tax liens >$500K, debarment from government contracts

### ESG Scoring Thresholds (EcoVadis or equivalent)
- **Preferred**: EcoVadis Gold or Platinum (score 62+)
- **Acceptable**: EcoVadis Silver (score 45-61)
- **Conditional**: EcoVadis Bronze (score 25-44) — requires improvement plan with milestones
- **Disqualify**: Score below 25, refused assessment, or presence on known ESG violation lists

## Red Flags & Edge Cases

1. **Shell Company Indicators**: Vendor has a registered address at a virtual office or residential property, no verifiable employees on LinkedIn, website domain registered <12 months ago, and D-U-N-S Number was created in the last 90 days. Common in procurement fraud schemes where an insider creates a fictitious vendor (per DoD Inspector General fraud red flag guidance).

2. **Beneficial Ownership Obfuscation**: Vendor operates through layered holding structures across multiple jurisdictions (e.g., BVI → Singapore → operating entity), and the Ultimate Beneficial Owner (UBO) cannot be identified through standard screening. This pattern correlates with sanctions evasion and money laundering, per OFAC advisory guidance.

3. **Suspiciously Perfect RFI Response**: Vendor's SQQ responses mirror the buying organization's specification language verbatim, claim compliance with every listed standard, and provide no caveats or limitations. This often indicates a broker or trading company that plans to subcontract 100% of delivery — they are selling access, not capability.

4. **UFLPA Entity List Adjacency**: Vendor is not on the UFLPA Entity List but sources polysilicon, cotton, tomato products, or other high-risk inputs from Xinjiang-adjacent supply chains. CBP enforcement applies the rebuttable presumption broadly, and detention of goods at the border creates unpredictable lead time risk even when the Tier 1 vendor appears compliant.

5. **Financial Cliff Risk**: Vendor shows strong historical revenue but has a debt maturity wall within 18 months, a major customer representing >40% of revenue is known to be re-sourcing, or the vendor's industry is facing structural decline. D&B data may lag by 60-90 days; supplement with real-time signals from news monitoring and credit agency alerts.

6. **Capability Inflation via Subcontracting**: Vendor claims ISO 13485 (medical devices) or AS9100 (aerospace) certification but holds it only at a facility not involved in your production. Alternatively, the vendor intends to subcontract to a certified entity — meaning you have no direct quality oversight of the actual production site.

7. **Diversity Certification Fraud**: Vendor claims MWBE/WOSB/HUBZone status, but the certified owner is a passive figurehead while the business is operationally controlled by non-qualifying individuals. This "rent-a-cert" scheme exposes the buying organization to False Claims Act liability (31 U.S.C. §3729) in government contracting contexts.

8. **Geographic Concentration After Diversification**: Discovery exercise identifies three "new" vendors, but all three source critical sub-components from the same Tier 2 supplier in the same geographic region. The appearance of diversification masks actual single-point-of-failure risk at the sub-tier level.

9. **Sanctions Circumvention via Transshipment**: Vendor is registered in a non-sanctioned jurisdiction (UAE, Turkey, Malaysia) but exhibits trade patterns — Bill of Lading data, shipping routes, product origin markings — consistent with transshipment of goods originating from sanctioned countries (Russia, Iran, North Korea, Belarus).

10. **Zombie Vendor in ERP Master Data**: Internal vendor master file contains thousands of entries, many inactive or duplicate. A "new" vendor submitted through discovery turns out to already exist in the system under a different legal entity name or prior D-U-N-S number — creating duplicate master data, payment routing confusion, and lost leverage from spend consolidation.

11. **Bid Rigging Collusion Pattern**: Multiple vendors responding to an RFI share the same IP address for portal submissions, use nearly identical document templates with the same metadata author, or submit pricing that follows suspiciously uniform patterns. Per DOJ Antitrust Division indicators, complementary bidding (one high, one low by design) is the most common procurement collusion tactic.

12. **ESG Greenwashing**: Vendor prominently displays sustainability commitments and carbon neutrality claims on its website but has no EcoVadis rating, no CDP disclosure, and no verifiable third-party audit. When pressed, the vendor provides a self-authored "sustainability report" with no metrics, no baselines, and no targets — a compliance liability under CSDDD.

13. **Catastrophic Single-Source Lock-in**: Discovery is initiated after an existing sole-source vendor announces a 25% price increase, but the market scan reveals that the vendor holds proprietary tooling, molds, or IP that would cost $2M+ and 18 months to replicate — making switching effectively impossible without strategic investment.

## Common Mistakes

1. **Starting Discovery Too Late**: Category managers begin vendor discovery after a contract expires or an incumbent fails, rather than maintaining a rolling market sensing practice. This forces compressed timelines that skip due diligence steps and result in hasty selections.

2. **Over-Reliance on Incumbent Referrals**: Asking existing suppliers "who else does this?" creates a biased discovery pool. Incumbents refer companies they've collaborated with, not their best competitors. The longlist ends up populated with non-threatening alternatives.

3. **Ignoring Total Cost of Ownership**: Selecting vendors based on unit price rather than TCO — which includes freight, duties, quality defect rates, lead time variability, inventory carrying costs, supplier management overhead, and switching costs. A vendor 8% cheaper on unit price but requiring 30% more safety stock is not actually cheaper.

4. **Treating Discovery as a One-Time Event**: Best practice per ISM (Institute for Supply Management) is continuous market sensing, not episodic discovery triggered only by crises. Organizations that discover on a rolling basis maintain "warm" shortlists and can activate alternatives in days, not months.

5. **Failing to Validate Self-Reported Data**: Accepting RFI responses at face value without cross-referencing against D&B data, public filings, site visits, or customer references. A 2024 Veridion analysis found that up to 30% of self-reported supplier data (revenue, certifications, capacity) contains material inaccuracies.

6. **Diversity Theater**: Adding diverse vendors to the longlist to satisfy reporting requirements without genuine intent to award business. This erodes trust with diverse suppliers, wastes their bid preparation resources, and ultimately undermines the organization's supplier diversity program credibility.

7. **Neglecting Sub-Tier Visibility**: Qualifying a Tier 1 vendor without understanding their Tier 2 and Tier 3 dependencies. The 2021 Suez Canal blockage and 2020-2023 semiconductor shortage demonstrated that disruptions cascade from sub-tier failures, not Tier 1.

8. **Discovery Without Defined Decision Criteria**: Launching market scans before aligning stakeholders on evaluation weights, mandatory qualifications, and disqualification thresholds. This leads to scope creep, re-evaluation loops, and stakeholder disputes after responses are received.

9. **Omitting Cybersecurity Assessment**: Vendor discovery for technology, SaaS, or data-handling services that skips SOC 2 Type II, ISO 27001, or equivalent security validation. Third-party breaches are now among the top enterprise risk vectors, per Gartner's Third-Party Risk Management framework.

10. **Confusing Market Presence with Capability Fit**: Adding globally recognized brands to shortlists without verifying they serve the buyer's specific segment, geography, or volume tier. A Fortune 500 vendor may decline to quote a $200K opportunity or deliver inferior service to small accounts.

## Regulatory & Compliance Requirements

### International Standards
- **ISO 20400:2017** — Sustainable procurement guidance; provides framework for integrating sustainability into procurement processes including supplier evaluation criteria. Not certifiable but widely referenced as best practice benchmark.
- **ISO 9001:2015** — Quality management systems; baseline certification expected for manufacturing and many service vendors.
- **ISO 14001:2015** — Environmental management systems; increasingly required for vendors supplying to organizations with net-zero commitments.
- **ISO 27001:2022** — Information security management; mandatory for vendors handling sensitive data.

### U.S. Federal Regulations
- **FAR Part 19** — Small Business Programs; federal acquisitions require consideration of small business set-asides (8(a), HUBZone, SDVOSB, WOSB). Discovery for government contracts must include SBA-registered entities via SAM.gov.
- **UFLPA (P.L. 117-78)** — Requires importers to demonstrate goods are not produced with forced labor in Xinjiang. CBP enforces through the Forced Labor Enforcement Task Force (FLETF) Entity List. Discovery must screen vendors and their sub-suppliers against this list.
- **Dodd-Frank Act §1502** — Conflict minerals (tin, tantalum, tungsten, gold — 3TG) reporting requirements for SEC-reporting companies; discovery for electronics, aerospace, or industrial categories must include conflict mineral due diligence.
- **OFAC Sanctions** — Vendors must be screened against the Specially Designated Nationals (SDN) List, the Sectoral Sanctions Identification (SSI) List, and the Non-SDN Chinese Military-Industrial Complex Companies List before any engagement.

### European Union Regulations
- **EU CSDDD (Directive 2024/1760)** — Corporate Sustainability Due Diligence Directive; requires in-scope companies (phased from 2027-2029 based on size) to identify, prevent, and mitigate adverse human rights and environmental impacts in their value chains, including during vendor selection.
- **German LkSG (Lieferkettensorgfaltspflichtengesetz)** — Supply Chain Due Diligence Act; effective since January 2023 for companies with 1,000+ employees; mandates risk analysis, preventive measures, and remediation for human rights violations in supply chains.
- **EU Deforestation Regulation (EUDR, Regulation 2023/1115)** — Requires due diligence to ensure commodities (palm oil, soy, cattle, cocoa, coffee, rubber, wood) are deforestation-free; impacts vendor discovery for these raw materials.

### United Kingdom
- **Modern Slavery Act 2015, Section 54** — Requires organizations with £36M+ annual turnover to publish annual transparency statements on steps taken to identify and prevent modern slavery in supply chains. New statutory guidance (2025) increases expectations for supply chain mapping during vendor onboarding.

### Industry-Specific
- **IATF 16949** — Automotive quality management; mandatory for Tier 1 and Tier 2 automotive suppliers.
- **AS9100 Rev D** — Aerospace quality management; required for vendors in aerospace and defense supply chains.
- **GxP Compliance** — Pharmaceutical and life sciences vendors must comply with Good Manufacturing Practice (GMP), Good Distribution Practice (GDP), and related standards per FDA 21 CFR Parts 210/211 and EU GMP Annex 16.

## Terminology

1. **Approved Vendor List (AVL)**: The organization's master registry of vendors that have completed qualification and are authorized to receive purchase orders. Discovery outputs feed the AVL; being "discovered" does not equal being "approved."

2. **Category Management**: The strategic approach to procurement that segments organizational spend into discrete groups of products/services (categories) and manages each as a mini-business. Vendor discovery intensity is determined by category strategy.

3. **D-U-N-S Number**: A unique nine-digit identifier assigned by Dun & Bradstreet to individual business entities. Serves as the universal vendor identification key in procurement systems and is required for SAM.gov registration.

4. **EcoVadis Rating**: A sustainability assessment score (0-100) covering Environment, Labor & Human Rights, Ethics, and Sustainable Procurement. Used by 130,000+ companies as a standardized supplier ESG benchmark.

5. **Expression of Interest (EOI)**: A formal market engagement where potential vendors signal their interest and basic qualifications before a detailed RFI or RFP. Used to gauge market depth before committing to full discovery.

6. **First-Pass Screening**: The automated or semi-automated elimination of vendors from the initial universe based on binary pass/fail criteria (sanctions, geography, certifications) before detailed evaluation begins.

7. **Kraljic Matrix**: A 2x2 framework (Peter Kraljic, 1983) classifying purchased items by supply risk and profit impact into four quadrants: Strategic, Leverage, Bottleneck, Routine. Determines the appropriate level of discovery effort and relationship model.

8. **Longlist**: The initial set of potentially qualified vendors (typically 15-30) that have passed first-pass screening but have not yet been evaluated in depth. Precedes the shortlist.

9. **Maverick Spend**: Purchasing activity that occurs outside contracted suppliers or approved procurement channels. Discovery should account for maverick spend patterns that indicate unmet needs or inadequate AVL coverage.

10. **PAYDEX Score**: D&B's proprietary score (0-100) measuring a company's historical payment performance. A PAYDEX of 80 indicates on-time payment; scores below 60 signal systemic cash flow problems and vendor reliability risk.

11. **Request for Information (RFI)**: A structured questionnaire sent to longlisted vendors to gather detailed information on capabilities, financials, certifications, and references. Non-binding; used for prequalification, not pricing.

12. **Shortlist**: The reduced set of qualified vendors (typically 3-8) invited to participate in the formal RFP/RFQ/competitive bidding process. Represents the output of the discovery phase.

13. **Supplier Qualification Questionnaire (SQQ)**: A standardized form — often aligned with industry frameworks like JAGGAER or SAP Ariba templates — capturing a vendor's operational, financial, legal, and compliance profile. More detailed than an RFI; used for formal prequalification.

14. **Supply Market Analysis**: The systematic assessment of a supply market's structure, dynamics, and trends. Covers the number and distribution of suppliers, barriers to entry, pricing drivers, capacity utilization, and substitution risks.

15. **Total Cost of Ownership (TCO)**: The complete cost of acquiring, using, maintaining, and eventually disposing of a product or service. Includes purchase price plus freight, duties, quality costs, inventory carrying costs, administration costs, and switching costs.

16. **UNSPSC (United Nations Standard Products and Services Code)**: A hierarchical taxonomy (Segment → Family → Class → Commodity) used to classify procurement spend. The standard enables structured discovery by allowing precise matching of vendor capabilities to required commodity codes.

17. **Ultimate Beneficial Owner (UBO)**: The natural person(s) who ultimately own or control a legal entity, typically defined as holding >25% ownership or exercising significant control. UBO identification is required under anti-money laundering regulations and critical for sanctions screening.

18. **Vendor Master Data**: The centralized record within ERP systems (SAP MM, Oracle Procurement Cloud) containing all approved vendor profiles — legal name, tax ID, banking details, payment terms, performance ratings, and status. Discovery feeds new records into this master.

19. **Supply Base Rationalization**: The deliberate reduction or restructuring of the total number of active suppliers to optimize leverage, reduce management overhead, and strengthen strategic relationships. Discovery sometimes serves rationalization goals by identifying consolidation candidates.

20. **Nearshoring/Friendshoring**: Supply chain strategies that relocate sourcing from distant/geopolitically risky regions to nearby countries (nearshoring) or politically allied nations (friendshoring). Drives discovery toward new geographic supplier pools (e.g., Mexico, Vietnam, India, Eastern Europe).

21. **Tier 1/Tier 2/Tier N Supplier**: The supply chain hierarchy. Tier 1 suppliers provide directly to the buying organization; Tier 2 suppliers supply Tier 1; Tier N extends down the chain. Discovery must assess sub-tier dependencies, not just Tier 1 relationships.

22. **Debarment**: Formal exclusion of a vendor from eligibility for government contracts, typically for fraud, corruption, or performance failure. The U.S. System for Award Management (SAM.gov) publishes the federal debarment list; discovery must screen against it.

23. **Supplier Diversity**: Programs and policies that actively include businesses owned by underrepresented groups (minorities, women, veterans, LGBTQ+, disabled individuals) in procurement. Key certifications: NMSDC (MBE), WBENC (WBE), SBA 8(a), SDVOSB.

24. **Category Intelligence**: Data-driven insight into supply market conditions, pricing benchmarks, supplier landscapes, and risk factors for a specific procurement category. Platforms like JAGGAER Category Intelligence and ProcurementIQ provide structured market data to accelerate discovery.

## Quality Checklist

- [ ] **Discovery brief documented and signed off** — Business requirement translated into supplier-facing specification with UNSPSC classification, Kraljic quadrant assignment, and explicit mandatory/desirable criteria.
- [ ] **Minimum three independent source channels used** — Discovery drew from at least three distinct channels (e.g., AI platform + trade association + government registry) to avoid source bias.
- [ ] **Sanctions and denied-party screening completed** — All longlisted vendors screened against OFAC SDN, EU Consolidated List, and applicable country-specific sanctions lists with documented results and date-stamps.
- [ ] **Entity verification performed** — D-U-N-S Number validated, legal entity name confirmed against corporate registry filings, registered address verified as non-residential/non-virtual.
- [ ] **Financial health assessed for all shortlisted vendors** — D&B SER rating, PAYDEX score, or equivalent credit assessment obtained within 90 days of discovery completion.
- [ ] **ESG/Sustainability screening applied** — EcoVadis rating or equivalent sustainability assessment obtained or requested for categories subject to CSDDD, LkSG, or organizational ESG policy.
- [ ] **Diversity status verified** — Claimed diversity certifications confirmed through issuing body databases (SBA, NMSDC, WBENC) — not just vendor self-declaration.
- [ ] **Sub-tier dependency mapped for strategic categories** — For shortlisted vendors in Kraljic "Strategic" or "Bottleneck" quadrants, Tier 2 critical material/component sources documented.
- [ ] **RFI/SQQ responses cross-referenced** — Self-reported vendor data validated against at least one independent source (D&B, public filings, customer references, site assessment).
- [ ] **Geographic concentration risk assessed** — Shortlist reviewed to confirm that geographic diversification is real, not superficial (i.e., vendors are not all dependent on the same sub-tier region).
- [ ] **Audit trail complete** — Full documentation of methodology, sources searched, vendors identified, screening criteria applied, elimination rationale, and scoring methodology preserved for procurement audit.
- [ ] **Stakeholder alignment confirmed** — Evaluation criteria and weights reviewed and approved by cross-functional stakeholders (category manager, business owner, quality, legal, finance) before scoring.
- [ ] **TCO framework defined** — Evaluation includes total cost of ownership components beyond unit price: logistics, quality costs, inventory impact, tariffs/duties, currency risk, and switching costs.
- [ ] **Cybersecurity posture assessed** — For vendors that will access organizational systems, handle data, or provide technology services: SOC 2 Type II, ISO 27001, or equivalent validation obtained.
- [ ] **Discovery output package delivered** — Shortlist with standardized vendor profiles, risk heat map, capability comparison matrix, and recommended next steps provided to sourcing team.

## References

1. Veridion — "Ultimate Guide to Procurement Best Practices in 2024" — https://veridion.com/wp-content/uploads/2024/02/Ultimate-Guide-to-Procurement-Best-Practices-in-2024-Compress.pdf
2. CIPS — "The Thirteen Steps of the Procurement Process" — https://www.cips.org/intelligence-hub/procurement/procurement-process
3. CIPS — "Supplier Selection Process" — https://www.cips.org/intelligence-hub/managing-suppliers/supplier-selection
4. CIPS — "Kraljic Matrix" — https://www.cips.org/intelligence-hub/supplier-relationship-management/kraljic-matrix
5. Zapro AI — "Top Vendor Discovery Platforms 2026" — https://zapro.ai/vendor-management/top-vendor-discovery-platforms/
6. BitSight — "The Vendor Due Diligence Checklist: A 5-Step Guide" — https://www.bitsight.com/blog/five-step-vendor-due-dilligence-checklist
7. European Commission — "Corporate Sustainability Due Diligence" — https://commission.europa.eu/topics/business-and-industry/doing-business-eu/sustainability-due-diligence-responsible-business/corporate-sustainability-due-diligence_en
8. PwC — "The Corporate Sustainability Due Diligence Directive (2025)" — https://www.pwc.ch/en/publications/2025/the-corporate-sustainability-due-diligence-directive.pdf
9. OFAC — "Sanctions List Search Tool" — https://ofac.treasury.gov/sanctions-list-search-tool
10. BitSight — "OFAC and Vendor Management" — https://www.bitsight.com/blog/ofac-and-vendor-management
11. U.S. CBP — "UFLPA Enforcement FAQs" — https://www.cbp.gov/trade/forced-labor/faqs-uflpa-enforcement
12. DoD Inspector General — "Fraud Red Flags and Indicators" — https://www.dodig.mil/Resources/Fraud-Detection-Resources/Fraud-Red-Flags/
13. Trustpair — "Vendor Fraud Red Flags" — https://trustpair.com/blog/6-red-flags-of-vendor-fraud-to-watch-out-for/
14. Dun & Bradstreet — "DUNS for Vendor Onboarding and Risk Assessment" — https://www.dnb.co.in/blog/duns-for-vendor-onboarding
15. FAR Part 19 — "Small Business Programs" — https://www.acquisition.gov/far/part-19
16. SAM.gov — System for Award Management — https://sam.gov/
17. EcoVadis — "Supply Chain Sustainability Ratings" — https://ecovadis.com/solutions/ratings/
18. ISM — "Strategic Sourcing Step-by-Step Guide" — https://www.ism.ws/logistics/strategic-sourcing/
19. Veridion — "How AI Transforms Supplier Discovery" — https://veridion.com/blog-posts/how-ai-transforms-supplier-discovery/
20. Tealbook — "The Role of AI in Supplier Data Enrichment" — https://www.tealbook.com/blog/the-role-of-ai-in-supplier-data-enrichment/
21. Spend Matters — "Category Analytics and Intelligence Providers" — https://spendmatters.com/2020/02/10/category-analytics-and-intelligence-providers-defining-and-exploring-a-nascent-market-for-procurement-solutions-part-1-introduction/
22. JAGGAER — "Category Intelligence" — https://www.jaggaer.com/solutions/category-intelligence
23. Mitratech — "Managing Supply Chain Concentration Risk" — https://mitratech.com/resource-hub/blog/supply-chain-concentration-risk/
24. Vizibl — "Comprehensive Guide to ISO 20400" — https://www.vizibl.co/blog/comprehensive-guide-to-iso-20400-sustainable-procurement-standard
25. UNGM — "UNSPSC Classification" — https://www.ungm.org/public/unspsc
26. Compliance and Risks — "Complete Guide to Supply Chain Sustainability Due Diligence (2025)" — https://www.complianceandrisks.com/blog/the-complete-guide-to-supply-chain-sustainability-due-diligence-navigating-regulatory-compliance-in-2025/
27. SupplierGateway — "Understanding Supplier Diversity Certifications" — https://www.suppliergateway.com/understanding-supplier-diversity-certifications/
28. IDC — "IT Procurement Best Practices 2024" — https://info.idc.com/rs/081-ATC-910/images/IDC-IT-Procurement-Best-Practices-2024-AP.pdf