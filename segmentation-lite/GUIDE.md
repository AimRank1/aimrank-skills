# Segmentation with Bias Auditing: what the full product does

This guide ships with the free skill `segmentation-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/segmentation-bias-audit/) shows the current status.

## Where the free skill stops

This skill proposes segments from one table inside one conversation. It runs no clustering algorithm and no stability test, its bias check is a read and not a statistical disparate-impact test, and it produces no audit report. Do not use its output to decide eligibility or pricing.

## What the full product is designed to add

- Interpretable clusters with plain-language profiles, held to a stability test before they ship
- Four-fifths-rule disparate-impact tests per segment, plus detection of features that act as proxies for protected traits; failing features are removed and the model is re-clustered
- A bias audit report and methodology note with every export
- A re-audit on every data refresh, with drift alerts when segment sizes shift
- A run inside your own warehouse, with an MCP endpoint your CRM and campaign tools can read

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/segmentation-bias-audit/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

A bias audit is evidence, not absolution: it tests what is measurable in your data, and if the data cannot support a fairness claim the report says so.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
