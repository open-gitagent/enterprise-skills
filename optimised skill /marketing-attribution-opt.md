---
name: marketing-attribution
description: >
  Multi-touch marketing attribution modeling including first-touch, last-touch, linear, time-decay, and data-driven attribution methodologies.
metadata:
  vertical: marketing
  function: analytics
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "GDPR, CCPA, Cookie Laws"
---

## Role
Assign fractional conversion credit to marketing touchpoints using rule-based or algorithmic models to inform budget allocation decisions.

## Attribution Model Selection Matrix

| Model | Credit Assignment | Best For | Fatal Flaw |
|---|---|---|---|
| First-Touch | 100% to first interaction | Brand/demand-gen awareness; net-new prospect sourcing | Ignores nurture and conversion-stage touches |
| Last-Touch | 100% to final pre-conversion interaction | Short e-commerce cycles (<7 days) | Over-credits branded search/retargeting; starves upper-funnel |
| Linear | Equal credit across all touchpoints | Baseline when no hypothesis exists | Treats accidental impression = high-intent demo request |
| Time-Decay | Exponential credit closer to conversion | 2-4 week considered purchases; GA4 default 7-day half-life | Undervalues early brand-building touches in long journeys |
| Position-Based (U-Shaped) | 40% first / 40% last / 20% middle | Mid-market without DDA capabilities | 40/40/20 split is arbitrary; may not reflect actual influence |
| Data-Driven (DDA) | Algorithmic (Shapley values/Markov chains) | High-volume properties; requires ≥400 conversions/30 days | Silent fallback to last-click if volume drops; opaque |

## The Triangulation Principle

| Layer | Methodology | Answers | Cadence |
|---|---|---|---|
| Tactical | MTA (Multi-Touch Attribution) | Which channels drive conversions this week? | Weekly |
| Strategic | MMM (Marketing Mix Modeling) | How to allocate $5M budget next quarter? | Quarterly |
| Causal | Incrementality/Lift Testing | Did this campaign cause incremental conversions? | Semi-annual |

**When MTA says 30% credit to paid social but incrementality shows 12% lift: MTA captures correlation, not causation. MMM provides calibration anchor.**

## Attribution Model Quality Scorecard

| Criterion | Weight |
|---|---|
| Conversion path coverage (≥2 touchpoints captured) | 20% |
| Incrementality alignment (attributed credit vs. measured lift) | 20% |
| Cross-device identity resolution rate | 15% |
| Statistical significance of DDA (conversion volume vs. minimum) | 15% |
| Lookback window appropriateness (matches sales cycle) | 10% |
| Consent/tracking compliance (Consent Mode coverage) | 10% |
| Actionability (evidence attribution changed budget allocation) | 10% |

**<60% = do not use for budget decisions. 60-80% = directional only. >80% = automated optimization eligible.**

## Lookback Windows by Conversion Type

| Conversion Type | Recommended Window | Rationale |
|---|---|---|
| E-commerce impulse | 7 days | Minimal consideration time |
| Considered B2C | 30 days | Product research phase |
| B2B pipeline creation | 90 days | Multi-touch buying journey |
| B2B closed-won revenue | 180+ days | Long enterprise sales cycles |

## Process

**Phase 1 — Data Foundation (Weeks 1-4)**
1. **Audit tracking** — Verify UTM parameter governance (campaign/source/medium taxonomy), pixel deployment, server-side tagging; confirm Google Consent Mode v2 for EU traffic (`ad_user_data` and `ad_personalization` parameters)
2. **Map conversion taxonomy** — Define primary conversions (purchase/SQLs/closed-won) and micro-conversions (email signup/content download/demo request) with consistent event names
3. **Establish identity resolution** — First-party identifiers (logged-in user IDs, hashed emails); CDP for probabilistic matching where deterministic unavailable
4. **Define lookback windows** — Per conversion type; document rationale (shorter windows bias toward lower-funnel)

**Phase 2 — Model Selection & Configuration (Weeks 5-8)**
5. **Baseline with last-touch** — All subsequent comparisons reference last-touch as control
6. **Evaluate DDA sufficiency** — GA4 minimum: 400 conversions/30 days; below threshold → GA4 silently falls back to last-click; verify in attribution settings monthly
7. **Select primary model** — Mid-market B2C: time-decay or DDA; B2B: position-based or custom first-touch-heavy model
8. **Build custom model** — Markov chain or Shapley: extract path data from GA4 BigQuery export or CDP; R `ChannelAttribution` package or Python `pychattr`; validate removal effects

**Phase 3 — Validation & Calibration (Weeks 9-12)**
9. **Run incrementality tests** — Holdout groups (typically 10-20% withheld); geographic or audience holdouts on top 2-3 channels by spend
10. **Compare model outputs** — Channel-by-channel: last-touch vs. selected model vs. incrementality; flag divergence >50% between attributed credit and incremental lift
11. **Calibrate weights** — Adjust DDA weights using incrementality test results as ground truth (Bayesian update)
12. **Establish cadence** — Weekly MTA dashboards; monthly model comparison; quarterly MMM refresh; semi-annual incrementality cycles

**Phase 4 — Operationalization (Ongoing)**
13. **Automate budget recommendations** — Guardrail: no single channel reallocation >15% without incrementality validation
14. **Monitor model drift** — Track month-over-month channel credit shifts; single-channel shift >25% = investigate for tracking breakage before accepting as genuine
15. **Maintain consent compliance** — Re-validate Consent Mode v2 quarterly; monitor consent rates by geography; declining EU opt-in degrades DDA model quality

## Glossary

| Term | Definition |
|---|---|
| MTA (Multi-Touch Attribution) | Assigns fractional credit to multiple touchpoints using rule-based or algorithmic models |
| First-Touch | 100% credit to first recorded interaction |
| Last-Touch | 100% credit to final pre-conversion interaction; historical default |
| Time-Decay | Exponential credit closer to conversion; GA4 default 7-day half-life |
| Position-Based (U-Shaped) | 40% first / 40% last / 20% middle touchpoints |
| DDA (Data-Driven Attribution) | ML-based (Shapley values/Markov chains) using converting and non-converting paths; ≥400 conversions/30 days |
| Shapley Value | Cooperative game theory: each channel's average marginal contribution across all coalitions; GA4 DDA foundation |
| Markov Chain | Probabilistic model calculating "removal effect" — conversion rate decrease if channel eliminated from all paths |
| Removal Effect | Markov: % conversion decrease when a channel is removed; basis for proportional credit |
| Lookback Window | Max period before conversion for eligible touchpoints; 7/30/60/90/180 days |
| View-Through Conversion | Conversion after ad served but not clicked; 1-day window standard post-ATT |
| Incrementality Testing | Experimental holdout methodology measuring causal, incremental impact beyond organic baseline |
| MMM (Marketing Mix Modeling) | Regression on aggregate spend/outcome data; immune to cookie/tracking limitations |
| Conversion Path | Ordered sequence of touchpoints before conversion; raw data input for attribution |
| Identity Resolution | Linking multiple device/session identifiers to single user via deterministic or probabilistic matching |
| Cross-Device Attribution | Tracking credit across user's multiple devices; requires identity resolution |
| Assisted Conversion | Touchpoint on conversion path that did not receive last-touch credit |
| CDP (Customer Data Platform) | Unifies first-party data for persistent user profiles; enables identity resolution |
| UTM Parameters | utm_source/medium/campaign/content/term — URL query strings for traffic source identification |
| Consent Mode | Google framework adjusting tag behavior by consent status; v2 required EU March 2024; `ad_user_data` + `ad_personalization` |
| SKAdNetwork (SKAN) | Apple's privacy-preserving iOS app install attribution; 24-48 hr delays; limited postbacks; no user IDs |
| Holdout Group | 10-20% audience excluded from marketing treatment; incrementality test control |
| Walled Garden | Closed platform (Meta/Amazon/Google/Apple) restricting user-level data export |
| Account-Based Attribution | Rolls up individual touchpoints to account/opportunity level for B2B buying committees |

## Checklist

- [ ] UTM taxonomy audit: all active campaigns use consistent, validated parameters; no duplicates or misspellings
- [ ] Conversions deduplicated: each counted exactly once; no double-counting between pixels and server-side events
- [ ] Lookback windows documented with written rationale per conversion type
- [ ] GA4 DDA threshold verified: >400 conversions/30 days; fallback model documented if below
- [ ] Cross-device identity resolution rate measured and reported
- [ ] Incrementality test completed within last 6 months on top-spend channel
- [ ] Platform-reported vs. independent attribution compared; discrepancies documented (Meta/Google/TikTok self-attribution vs. neutral platform)
- [ ] Google Consent Mode v2 confirmed active with `ad_user_data` and `ad_personalization` parameters; EU consent rate monitored
- [ ] Offline touchpoints (trade shows/direct mail/outbound calls) logged in CRM and included in attribution paths
- [ ] Model output stability monitored: single-channel shift >25% month-over-month investigated before accepting as genuine
- [ ] Non-converting paths included in DDA training (not just converter paths)
- [ ] Budget reallocation guardrails: no channel shifted >15% based solely on MTA without incrementality or MMM corroboration
- [ ] Walled garden dark spots documented; MMM or platform-specific measurement fills gap
- [ ] Total attributed revenue reconciles to actual revenue within ±5%; discrepancies explained

## References
GDPR Articles 5, 6, 7; ePrivacy Directive 2002/58/EC (explicit consent for cross-site cookies); CCPA/CPRA Cal. Civ. Code §1798.100-199.100 (GPC signals; opt-out of sharing/cross-context behavioral advertising); Google Consent Mode v2 (enforcement March 2024; `ad_user_data` + `ad_personalization`); IAB TCF 2.2; Apple ATT iOS 14.5 (~25% IDFA opt-in); SKAdNetwork (SKAN); MRC Accreditation; IAB Attribution Council Guidelines; HBR 2024 (rule-based models over-credit by 30-40%); GA4 DDA (Shapley values; ≥400 conversions/30 days minimum); Meta Incremental Attribution 2025; Demandbase; 6sense; HubSpot; Branch; AppsFlyer
