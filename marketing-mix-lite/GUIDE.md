# Marketing Mix Model + Budget Optimizer: what the full product does

This guide ships with the free skill `marketing-mix-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/marketing-mix-model/) shows the current status.

## Where the free skill stops

This skill reads one spend-and-results file inside one conversation. It fits no model: no adstock, no saturation curve, no interval. What it reports is correlation with caveats, not incrementality, and it should not move a real budget.

## What the full product is designed to add

- A Bayesian marketing-mix model with adstock (carry-over) and saturation per channel, on weekly aggregate data with no user-level tracking
- Every channel's return with a credible interval, and a response curve per channel
- A budget optimiser over the fitted curves, under your total budget, channel minimums and commitments
- Validation on held-out weeks and, where you can run one, a geo-lift or holdout test
- A refit as new weeks land, with drift alerts when a channel's response shifts
- A hash-chained audit log of every run, and MCP tools for your agents

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/marketing-mix-model/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

It needs history: under roughly two years of weekly data the honest answer may be "these channels cannot be separated yet". It is aggregate by construction and cannot say which individual converted.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
