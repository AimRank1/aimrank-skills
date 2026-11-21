# AML / Fraud Detection: what the full product does

This guide ships with the free skill `aml-triage-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: listed as a blueprint.** The product page lists this product as a blueprint, with the PoC scoped once the product is built. The [product page](https://www.aimrank.io/products/aml-fraud-detection/) shows the current status.

## Where the free skill stops

This skill orders the payments in one file inside one conversation. It trains no model, its score is a ranking and not a probability, it sees only that file, and it keeps no audit trail. It is not transaction monitoring for money laundering and not sanctions screening, and it decides, blocks and reports nothing.

## What the full product is designed to add

- A model trained on the institution's own history that returns a probability calibrated on held-out data and checked inside the alert queue
- Reasons computed from the model itself, not written after the fact
- The alert threshold shown as a cost table, so the business chooses it
- A frozen pass/fail test the build must clear before it ships: it has to beat a rules baseline
- A fairness check on who lands in the queue, and drift monitoring
- A tamper-evident audit log
- An MCP endpoint so your own agents can call it
- Scoped per engagement on your data. It ranks for a human analyst and blocks or files nothing

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. The product page lists this product as a blueprint, so ask through the page what can be delivered today.
- **PoC.** Per the product page: scoped once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/aml-fraud-detection/

To ask for this product, use the **Request this build** button on that page.

## A code for people who use this skill

No code is printed in this skill. People who use it can leave a work email on the product page. Whether that earns a code toward the product's Scaffolding, and what the code gives, is stated on that page and nowhere else.

## What it does not promise

It blocks nothing, freezes nothing and files nothing: a person decides every alert. It is not an anti-money-laundering system, and nothing in it says that a system meets the EU AI Act, anti-money-laundering rules or a supervisor's expectations.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
