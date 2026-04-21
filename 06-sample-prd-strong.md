# PRD: Trust-Signal Insert in Checkout

**Author:** J. Doe, Senior PM, Payments
**Status:** Draft v3, pre-review
**Reviewers:** Eng, Design, Risk, Legal

## TL;DR

We're losing ~8% of checkout starts at the "Review & Pay" step on new-account orders >$200. Qualitative and quant evidence point to trust friction — users don't recognize the merchant, don't see a guarantee, and bail. We propose a compact trust-signal module on the Review step, shown only to new-to-merchant buyers above a dynamic order-value threshold. Primary metric: new-to-merchant checkout completion rate. Target: +2.5 pp over 6 weeks at GA.

## Problem

**What we know:**
- On the Review & Pay step, checkout completion for **new-to-merchant buyers** is 84.1% below $200, and 76.3% above $200. For returning buyers, the spread is <1 pp.
- Session replays (n=42, sampled from bounced sessions) show the pattern: users land on Review, scroll up and down once, exit. Avg dwell before exit: 11 seconds.
- User interviews (n=14, bounced buyers in the last 30 days): 9 mentioned "I wasn't sure if this was legit" or close variants. 3 mentioned shipping concerns. 2 cited price surprise.

**What we don't yet know:**
- Whether the Review-step friction is caused by the merchant brand (unfamiliar) or the checkout UI itself. Our data can't distinguish these. See "Risks."

## Who this is for

- **Primary:** first-time buyers at a given merchant, order value ≥ dynamic threshold (starts at $200, tunable per vertical).
- **Not for:** returning buyers at the same merchant (already converting), or small orders (no observed friction).

## Proposed solution

Above the pay button on the Review step, render a compact, scannable **Trust Signal** module containing:

1. Buyer-protection guarantee (existing policy, newly surfaced).
2. Merchant signals we already have: years on platform, total orders shipped, dispute rate.
3. An estimated delivery window pulled from the shipping quote.

No new data collection. No policy changes. All fields come from existing systems.

## Why this, not something else

| Alternative | Why rejected (for v1) |
|---|---|
| Full merchant-profile modal on click | Adds a step and hides info behind interaction. Bouncers don't click. |
| Highlighted guarantee banner only | Tested in Q1 as a banner experiment; moved the metric 0.3 pp, not significant. |
| Price-surprise fix (shipping earlier) | Separate workstream already committed for H2. Not a blocker for this. |
| Do nothing, wait for brand work | Brand team's new-merchant trust initiative ships in 9 months. We can't wait. |

## Success metrics

**Primary:** new-to-merchant Review→Complete rate, order value ≥ threshold.
Target: **+2.5 pp** absolute (currently 76.3% → 78.8%) by 6 weeks post-GA.

**Secondary:** GMV from the eligible cohort, +1.5% MoM.

**Counter-metrics:**
- Dispute rate on affected orders (must not increase more than 10% relative).
- Checkout time to complete (must not increase >1.5 seconds p50).
- Returning-buyer completion (should not change; if it drops, we're crowding the UI).

**Leading indicators in-experiment:** dwell time on Review step, scroll depth.

## Scope

**In scope:** the module, the eligibility logic, the dynamic threshold config, instrumentation.

**Non-goals:**
- Modifying guarantee policy or wording of Terms.
- Returning-buyer UX.
- Merchant-facing settings.
- Localization beyond US-EN for v1 (v2 scope).

## Risks & unknowns

1. **Attribution risk.** If the cohort completes more, we won't cleanly know whether it was the module or coincidence. Mitigation: 50/50 holdout for 4 weeks before GA; do not GA without a 95% significant primary-metric lift.
2. **Crowding.** The Review step is dense. If the module pushes the pay button below the fold on smaller screens, we could regress the control cohort. Mitigation: sticky pay button; design review specifically for 375px width.
3. **Merchant-signal honesty.** "98.2% positive" feels marketing-y. Legal has signed off on phrasing; we'll re-check post-launch for any complaints.
4. **The real cause might be pricing, not trust.** If primary metric fails to move, the next experiment should test an earlier-shipping-surface (already scoped, separate PRD).

## Rollout

- Wk 0: internal employees only, verify instrumentation.
- Wk 1–4: 50/50 holdout, eligible cohort, 3 mid-sized verticals.
- Wk 5: readout. Kill criterion: primary metric <+1 pp at p<0.05 → we kill and write up.
- Wk 6–8: expand to all verticals if green.

## Dependencies

- Shipping-quote service: latency budget confirmed with Shipping team.
- Experimentation platform: standard.
- Legal review of module wording: in flight, eta Wk -1.

## Open questions

- Do we want to show the module to signed-in buyers who are new to *this* merchant but established on the platform? Leaning yes; confirming with Risk.
- The threshold is currently per-vertical flat. Should it be per-merchant-category? Deferring to v1.1.
