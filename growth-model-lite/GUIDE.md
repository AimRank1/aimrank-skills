# Calibrated Churn Predictor: what the full product does

This guide ships with the free skill `growth-model-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: reference build.** The code exists and AimRank has run and measured it on its own reference data. The label does not mean a system running at a client, and it says nothing yet about results on your data. The [product page](https://www.aimrank.io/products/churn-predictor/) shows the current status.

## Where the free skill stops

This skill is aggregate accounting inside one conversation. It gives every user in a state the same number, gives no prediction interval, and keeps nothing between runs: no per-user scores, no drift alerts, no audit trail.

## What the full product adds

- Per-user calibrated probabilities that add up to the transition matrix, so the forecast and the per-user scores cannot disagree
- Prediction intervals whose coverage is measured on dates the calibration never saw
- A reason for each user's score
- Drift detection on the transition matrix itself (a falling CURR is the alert)
- A tamper-evident audit log and Annex IV documentation generated from the run
- An MCP endpoint for your own agents

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own. It is for a team with its own developers: you run it and connect it to your data yourselves. No result on your data is promised at this step.
- **PoC.** The product applied to a static export of your data, with no live connection to your systems. It ends in a written verdict within one week of a usable export. No quality is promised before your data has been seen: you pay for the verdict, whatever it says. The application running on your export stays with you.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/churn-predictor/

To ask for a Scaffolding or a PoC, use the **Request this build** button on that page.

## A code for people who use this skill

No code is printed in this skill. People who use it can leave a work email on the product page. Whether that earns a code toward the product's Scaffolding, and what the code gives, is stated on that page and nowhere else.

## What it does not promise

If the product itself is the reason people leave, no targeting fixes churn: the model finds who is leaving and why. With under about 18 months of history, expect wider uncertainty in the first year.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
