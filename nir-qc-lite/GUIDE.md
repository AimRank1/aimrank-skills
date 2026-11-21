# Spectroscopic QC Pipeline: what the full product does

This guide ships with the free skill `nir-qc-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: reference build.** The code exists and AimRank has run and measured it on its own reference data. The label does not mean a system running at a client, and it says nothing yet about results on your data. The [product page](https://www.aimrank.io/products/spectroscopic-qc/) shows the current status.

## Where the free skill stops

This skill reads a table of predictions you already have, inside one conversation. It builds and validates no calibration, computes no intervals or applicability-domain distances itself (it uses the columns you supply), and keeps no audit trail. It never releases a batch.

## What the full product adds

- Split-conformal prediction intervals, with coverage measured on held-out batches
- An applicability-domain guard (Hotelling T² and Q residuals) that triggers the abstention
- A frozen acceptance test (RPD, RPIQ, external RMSEP) that refuses an unvalidated calibration
- Drift monitoring (PSI/KS) with retraining tickets
- The spectral regions behind each prediction, with reasons in plain language
- A hash-chained audit log and an evidence dossier generated from each run
- An MCP server with no release-decision tool: release stays with your Qualified Person

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own. It is for a team with its own developers: you run it and connect it to your data yourselves. No result on your data is promised at this step.
- **PoC.** The product applied to a static export of your data, with no live connection to your systems. It ends in a written verdict within one week of a usable export. No quality is promised before your data has been seen: you pay for the verdict, whatever it says. The application running on your export stays with you.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/spectroscopic-qc/

To ask for a Scaffolding or a PoC, use the **Request this build** button on that page.

## A code for people who use this skill

No code is printed in this skill. People who use it can leave a work email on the product page. Whether that earns a code toward the product's Scaffolding, and what the code gives, is stated on that page and nowhere else.

## What it does not promise

The release decision is never the system's: your Qualified Person signs the validation and every release. Predictions outside the validated range abstain.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
