# Industrial Computer Vision QC: what the full product does

This guide ships with the free skill `defect-check-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/industrial-cv-qc/) shows the current status.

## Where the free skill stops

This skill looks at the images you give it inside one conversation. It is not trained on your product, its confidence is not calibrated, it has no measured escape or false-reject rate, it cannot run at line speed, and it stores no evidence.

## What the full product is designed to add

- Camera, lens and lighting designed for your product and line speed, before any model
- Anomaly detection that learns your good product, so rare defects can be flagged from a few examples
- Pass or reject at line speed on edge hardware beside the line
- Every reject stored with its frame, heatmap and score
- Escape rate and false-reject rate measured against your human QC, with drift alerts on lighting and camera shift
- An MCP endpoint for MES and QMS integration; the reject policy stays yours

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/industrial-cv-qc/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## What it does not promise

A defect that is invisible from the camera's angle stays invisible: optics and lighting are half the project and come first. Both escapes and false rejects are measured, not assumed.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
