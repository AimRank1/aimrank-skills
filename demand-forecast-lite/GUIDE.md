# Demand Forecasting (LT calendar): what the full product does

This guide ships with the free skill `demand-forecast-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: listed as a blueprint.** The product page lists this product as a blueprint, with the PoC scoped once the product is built. The [product page](https://www.aimrank.io/products/demand-forecasting/) shows the current status.

## Where the free skill stops

This skill forecasts from one CSV inside one conversation. Its range is a judgment checked, at best, against your own last two weeks. It is not calibrated, it is not backtested against a pass/fail test, and it keeps no record of forecasts and outcomes.

## What the full product is designed to add

- A P10 to P90 band calibrated on held-out weeks and checked by a rolling backtest against a frozen pass/fail test: it must beat the seasonal-naive forecast, and coverage must sit near the stated 80%
- A breakdown of each forecast into its drivers: trend, seasonality, promotion, holiday
- Coverage and drift monitoring, with recalibration when the band stops holding
- A tamper-evident audit log
- An MCP endpoint so your own agents can call it
- Scoped per engagement on your data: reconciliation across SKU, category and store, safety-stock sizing to a service level, and ERP/WMS integration

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. The product page lists this product as a blueprint, so ask through the page what can be delivered today.
- **PoC.** Per the product page: scoped once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/demand-forecasting/

To ask for this product, use the **Request this build** button on that page.

## What it does not promise

New SKUs and promotion spikes are the hard cases: they get wider ranges, not confident numbers, and your planner keeps the final say on every order. With under two full years of history, expect wider ranges in the first year.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
