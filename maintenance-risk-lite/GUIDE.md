# Predictive Maintenance: what the full product does

This guide ships with the free skill `maintenance-risk-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/predictive-maintenance/) shows the current status.

## Where the free skill stops

This skill reads the logs you paste into one conversation. Its urgency window is a judgment, not a calibrated remaining-useful-life estimate, it learns no per-machine baseline, it writes nothing to a maintenance system, and it keeps no record of alerts and outcomes.

## What the full product is designed to add

- A connection to the sensors you already have (historian or OPC-UA), with a baseline per machine and per operating mode
- A remaining-useful-life estimate with a named failure mode and an honest P10 to P90 window
- Draft work orders into your maintenance system that the planner approves
- Confirmed and missed failures retraining the baselines, with sensor drift and dead channels flagged
- A log from every alert to its outcome
- A run on-premises or in your cloud, with an MCP endpoint

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/predictive-maintenance/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

Failures that leave no signature in the data, such as a sudden shaft fracture, cannot be predicted. Precision and recall are reported per failure mode, and every estimate is a range.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
