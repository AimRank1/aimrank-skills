# AML / Fraud Detection: what the full product does

This guide ships with the free skill `aml-triage-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: listed as a blueprint.** The product page lists this product as a blueprint, with the PoC scoped once the product is built. The [product page](https://www.aimrank.io/products/aml-fraud-detection/) shows the current status.

## Where the free skill stops

This skill ranks the alerts in one file inside one conversation. It trains no model, its score is a ranking and not a calibrated probability, it sees no account history or counterparty network beyond the file, and it keeps no audit trail. The disposition and any report to the authorities stay with the analyst.

## What the full product is designed to add

- A model trained and calibrated on your own confirmed cases, with anomaly detection for new patterns and counterparty-graph features
- Reason codes per alert, in analyst language, that pre-fill the report narrative
- A shadow run beside your existing rules before any rule is switched off, with compliance sign-off
- Drift monitoring, with analyst dispositions feeding retraining
- A hash-chained audit trail in which every decision can be replayed
- Deployment in your own environment, and MCP tools for investigators' agents (the disposition stays human)

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. The product page lists this product as a blueprint, so ask through the page what can be delivered today.
- **PoC.** Per the product page: scoped once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/aml-fraud-detection/

To ask for this product, use the **Request this build** button on that page.

## What it does not promise

The model cannot add data that is not there: without device or counterparty data, detection quality is lower, and that is said before a contract. The report decision is never automated: the model ranks and explains, the analyst decides.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
