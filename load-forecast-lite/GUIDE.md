# Energy Demand Forecasting: what the full product does

This guide ships with the free skill `load-forecast-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/energy-forecasting/) shows the current status.

## Where the free skill stops

This skill forecasts from one load-history file inside one conversation. Its range is a judgment and not a calibrated interval, it ingests no weather forecast runs, it prepares no regulatory reporting, and it archives nothing.

## What the full product is designed to add

- A model of your own load shape from two years of metering data: daily peaks, weekday and weekend, Lithuanian holidays, degree-days
- Several numerical weather runs as input, with the range widening when they disagree
- Hourly P10/P50/P90 for day-ahead and intraday, with calibration tracked so that P90 means 90%
- ENTSO-E transparency reporting prepared from the run
- Every forecast archived with its inputs: weather run, calendar, model version
- An MCP endpoint for trading-desk tools

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/energy-forecasting/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

Extreme events still surprise forecasts. The design is to widen the range honestly when the weather runs disagree, and to show it when the P90 stops covering 90%.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
