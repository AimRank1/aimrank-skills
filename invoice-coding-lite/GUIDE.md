# Invoice Classification + Anomaly Detection: what the full product does

This guide ships with the free skill `invoice-coding-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/invoice-classification/) shows the current status.

## Where the free skill stops

This skill codes the invoices you give it inside one conversation. It has not learned your past coding decisions, its confidence is not calibrated, its anomaly flags see only what is in the conversation (no vendor history), and it posts nothing to an accounting system.

## What the full product is designed to add

- A classifier trained on each client's own historical coding, tuned for Lithuanian invoice text and each client's GL and VAT preferences
- Calibrated confidence: confident postings flow through, uncertain ones land in a review queue with the best guess
- Anomalies flagged on arrival with the reason: duplicates, VAT mismatches, vendor changes, Benford outliers
- Write-back to the accounting system (i.MAS, Sąskaita123, Rivilė), gated per client until that client passes the accuracy bar
- A reason for every classification and every flag, and an audit trail
- An MCP endpoint for accountants' agents

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/invoice-classification/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

Every client codes differently, and the model has to learn each one: expect a period of human-in-the-loop tuning per client. Write-back stays gated per client until that client passes the accuracy bar.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
