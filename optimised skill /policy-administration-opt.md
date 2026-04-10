---
name: policy-administration
description: >
  Insurance policy lifecycle management covering issuance, endorsements, renewals, cancellations, and policyholder communications.
metadata:
  vertical: bfsi-insurance
  function: operations
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "NAIC, State DOI"
---

## Role
Execute insurance policy contractual mechanics — issuance, endorsements, renewals, cancellations, and reinstatements — with precise premium calculation, statutory notice compliance, and system-of-record integrity across 50+ state regulatory regimes.

## Transaction Evaluation Framework

| Dimension | Key Question | Critical Standard |
|---|---|---|
| Contractual Validity | Filed/approved forms? Correct dec data? | Prior-approval states: DOI sign-off before issuance; policy period 12:01 AM standard time at insured's address |
| Premium Accuracy | Correct proration method? MEP compliant? | Mid-term: daily pro-rata; insured-requested cancellation: short-rate where state-permitted; audit-based reconciled at expiration |
| Regulatory Timeliness | Meeting every statutory deadline? | Nonpayment cancellation: 10-20 days; insurer-initiated: 30-60 days; nonrenewal: 45-120 days (state-dependent) |
| Communication Compliance | Statutory language, reason codes, delivery method? | Proof of mailing required some states; electronic delivery requires opt-in; some states mandate specific cancellation reason categories |
| System-of-Record Integrity | Accurate audit trail, document version control, statistical reporting? | Bordereaux to reinsurers; data to ISO/NISS/AAIS; NAIC MDL-668 cybersecurity for PII (25+ states; 72hr incident notification) |

## Cancellation Type Matrix

| Type | Return Premium | Notice Period | Notes |
|---|---|---|---|
| Flat cancellation | 100% refund | N/A | Treated as never existing |
| Insured-requested mid-term | Pro-rata (short-rate where state-permitted) | N/A | NY INS §3425: personal lines = pro-rata only |
| Insurer-initiated (underwriting) | Pro-rata | 30-60 days | 3rd-party notifications required |
| Insurer-initiated (nonpayment) | Pro-rata | 10-20 days | Mortgagee gets independent 10-30 day notice |

## State Nonrenewal Notice Periods (Selected)

| State | Personal Auto | Other Personal Lines | Key Statute |
|---|---|---|---|
| California | 75 days | 45 days most lines; 120 days post-wildfire moratorium | INS §675-679.7; §675.1 |
| New York | 60 days | 60 days | INS §3426 |
| Florida | 45 days standard; 120 days if policy in force 5+ years | 45 days standard | FS §627.4133 |
| Texas | 30 days insurer-initiated; 10 days nonpayment | Varies by line | TIC §551.107 |

## Market Conduct Deficiency Thresholds

| Criterion | Weight | Threshold |
|---|---|---|
| Notice Timeliness | 25% | Deficiency rate >7-10% triggers remediation |
| Premium Accuracy | 20% | Variance between calculated and correct premium; audit adjustments |
| Form Compliance | 15% | % policies using currently-approved form editions |
| Document Completeness | 15% | % files containing all required forms, endorsements, signatures |
| Transaction Processing Time | 10% | Avg days change request → completed endorsement |
| Policyholder Communication Quality | 10% | Complaint ratio per 1,000 policies; DOI complaints |
| Data Integrity | 5% | Error rate in statistical reporting; reconciliation variances |

## Process

**Phase 1 — Policy Issuance (New Business)**
1. Verify underwriter approval; confirm quote within binding authority and not expired (30-60 days typical)
2. Map risk to correct policy form edition + state-specific mandatory endorsements (UM/UIM, medical payments where required)
3. Confirm all rating factors per filed algorithm (classification codes, territory, experience mods, tier placement)
4. Generate dec page: legal named insured, policy period (12:01 AM at insured's address), limits, deductibles, premium breakdown by coverage
5. Issue binder if full policy not immediately available (30-90 days); track binder-to-policy conversion
6. Compile complete policy (declarations + insuring agreement + conditions + exclusions + endorsements); generate policyholder welcome kit
7. Set up billing: direct bill/agency bill/premium finance, installment schedule, commission splits
8. Life/annuity: initiate free-look period clock (10-30 days; CA 30 days for senior citizens per INS §10127.10)

**Phase 2 — Endorsement Processing (Mid-Term Changes)**
9. Capture change request; determine if underwriting referral required
10. Set endorsement effective date (never before inception or after expiration); verify retroactive endorsements permissible
11. Calculate premium change using daily pro-rata; apply correct additional/return premium basis
12. Generate endorsement form with sequential endorsement number; attach to policy record
13. Issue endorsement confirmation (coverage change + effective date + premium impact); recalculate agent commission

**Phase 3 — Renewal Processing**
14. Identify policies approaching expiration 60-120 days out per LOB and state requirements
15. Re-rate applying current approved rates + updated exposure data + loss experience
16. Flag adverse loss history, changed risk characteristics, pricing adequacy concerns for UW review
17. Generate renewal offer with updated dec, premium, coverage changes; include state-required comparison disclosures
18. If nonrenewal: issue notice within statutory window (CA 75 days personal auto; NY 60 days; FL 45/120 days; include specific reason where required by state)
19. Track acceptance/non-response; issue renewal policy upon acceptance or expiration of response period with auto-renewal

**Phase 4 — Cancellation Processing**
20. Classify cancellation type; generate notice with: effective date/time, specific reason, return premium amount, right to appeal/DOI complaint
21. Deliver per state method (certified mail where required); verify full statutory notice period met from receipt date (many states: mailing date + 3-5 day mailbox presumption)
22. Calculate unearned premium from cancellation effective date to original expiration; verify MEP compliance; issue refund within 30-45 days
23. Notify mortgagees/loss payees/additional insureds/certificate holders per contractual/statutory rights; mortgagee clause typically requires 10-30 days independent notice
24. Report cancellation to statistical agents (ISO, NISS, AAIS) per required schedules

**Phase 5 — Reinstatement**
25. Verify eligibility: time since lapse, reason, any claims during gap period
26. Life/annuity: evidence of insurability if beyond reinstatement window (3-5 years); collect back premiums + fees
27. Document whether reinstated policy has gap in coverage or is made retroactively continuous

## Glossary

| Term | Definition |
|---|---|
| Binder | Temporary evidence of coverage before formal policy; binding contract typically 30-90 days |
| Declarations Page | Front page: named insured, period, coverages, limits, deductibles, forms attached, premium |
| Endorsement | Written amendment adding/deleting/modifying coverage; numbered sequentially per policy |
| Flat Cancellation | Effective at inception; full premium refund; policy treated as never existing |
| Pro-Rata Cancellation | Proportional refund based on exact unexpired days; no penalty |
| Short-Rate Cancellation | Less-than-pro-rata refund; applies short-rate penalty table; prohibited personal lines in several states (NY INS §3425) |
| Minimum Earned Premium (MEP) | Minimum premium retained regardless of cancellation timing; subject to state regulatory limits |
| Grace Period | Post-due-date coverage window: 31 days life (statutory); P&C varies by state |
| Free Look Period | 10-30 days post-delivery to return life/annuity for full refund; CA 30 days seniors (INS §10127.10) |
| Earned Premium | Premium for elapsed coverage period; recognized as revenue under SAP |
| Unearned Premium Reserve (UPR) | Liability for premium collected for coverage not yet provided; on Schedule P of Annual Statement |
| SERFF | System for Electronic Rate and Form Filing — NAIC platform for DOI filings; prior approval/file-and-use/use-and-file/no-file regimes |
| Bordereaux | Detailed transaction report (new/endorsement/cancellation) submitted by MGA/agent to carrier or reinsurer, typically monthly |
| Countersignature | Licensed resident agent signature required in some states where risk is located |
| Named Insured | Person/entity specifically identified in declarations; distinct from additional insureds |
| Policy Period | Inception to expiration; standard: 12:01 AM to 12:01 AM at insured's mailing address |
| Conditional Renewal | Renewal materially changing terms/conditions/premium; many states require same advance notice as nonrenewal (NY INS §3426(e)) |
| Prior Approval State | DOI review and explicit approval required before rates/forms may be used (NY, TX for many lines) |
| Loss Payee/Mortgagee | Third party with financial interest entitled to loss payments and independent cancellation notice |
| ACORD Certificate | ACORD 25 (liability)/ACORD 28 (property); evidences policy existence to third parties; does NOT confer coverage rights |
| PAS | Policy Administration System — system-of-record: rating, document generation, billing, regulatory compliance |
| Surplus Lines | Non-admitted carrier placement for declined risks; different filing/tax requirements; surplus lines taxes and affidavit requirements |

## Checklist

- [ ] Every cancellation/nonrenewal notice cross-referenced against applicable state statute; mailing dates documented with proof of mailing
- [ ] All forms and endorsements reference currently approved edition date for applicable state and line
- [ ] Calculated premium matches filed rate × exposure × modification factors; no manual overrides outside documented authority
- [ ] Dec page accurate: correct legal named insured, policy period (12:01 AM), limits, deductibles, premium breakdown
- [ ] State-mandated endorsements attached (UM/UIM, medical payments, etc.); signed rejection forms on file where applicable
- [ ] All mortgagees/loss payees/additional insureds/certificate holders notified of cancellations/nonrenewals/material changes within contractual and statutory timeframes
- [ ] Free-look/cooling-off periods honored; in-window cancellations receive 100% premium refund
- [ ] Return premiums issued within state-mandated timeframe (typically 30-45 days from cancellation effective date)
- [ ] All policy transactions reported to statistical agents (ISO/NISS/AAIS) per required schedules and data formats
- [ ] Every transaction has timestamped audit trail: user/system/approval chain/effective date/document generated
- [ ] Billing system reflects current policy status, premium, installment schedule; no orphaned billing records for cancelled policies
- [ ] Material endorsements affecting limits/exposures reported in reinsurance bordereaux within reporting cycle
- [ ] Documents retained per state requirements (typically 5-7 years post-expiration; longer for some lines)
- [ ] PII in PAS encrypted, access-controlled, per NAIC MDL-668 (25+ states adopted; 72hr incident notification to commissioner)

## References
NAIC MDL-880/900/668/670/672; NAIC Market Regulation Handbook Chapter 20; SERFF; ACORD data standards; ACORD NGDS 2025; CA INS §§675-679.7/675.1/10127.10; NY INS §3425/3426; FL FS §627.4133; TX TIC §551.107; FLOIR quarterly insurer compliance reports; IAIS 2024 market conduct consultation; Guidewire PolicyCenter; Duck Creek; Majesco; BriteCore; Socotra; McKinsey P&C core modernization; BCG three modernization paths 2024
