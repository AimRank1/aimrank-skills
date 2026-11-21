# Dynamic Pricing for E-commerce: what the full product does

This guide ships with the free skill `pricing-check-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/dynamic-pricing/) shows the current status.

## Where the free skill stops

This skill reviews the price moves in one file inside one conversation. Its elasticity read is a judgment and not an estimate with error bars, it backtests nothing, it watches no competitor or stock signals, and it changes no live price.

## What the full product is designed to add

- Elasticity estimated from your own order history, with error bars, and backtested before any live price moves
- Signals assembled per SKU (competitor prices, stock cover, traffic, seasonality); conflicting signals hold the price
- Guardrails as code you approve: margin floors, maximum daily moves, category rules, the EU rule on showing the lowest price of the last 30 days when a reduction is announced, one price for everyone
- Every move logged with its reason and signals, and one-click overrides that feed the model
- A connection to your shop platform, with an MCP endpoint for category managers' tools

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/dynamic-pricing/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

Not a revenue dial: SKUs with too little data are held, not moved, and no live price is touched before a backtest. No personalised prices per visitor.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
