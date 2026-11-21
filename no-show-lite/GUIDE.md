# No-Show Prediction + Safe Overbooking: what the full product does

This guide ships with the free skill `no-show-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: built, gate not cleared.** The code exists and has been run, and it has not yet passed one of its own checks. The product page says which check and why. The status does not mean a system running at a client. The [product page](https://www.aimrank.io/products/no-show-prediction/) shows the current status.

## Where the free skill stops

This skill ranks the appointments in one file inside one conversation. The rank is not a calibrated probability, so it cannot size overbooking. The skill writes nothing to a scheduling system and keeps no record.

## What the full product adds

- A calibrated no-show probability per appointment, with reasons, from booking behaviour only: no clinical data, no age, no sex
- An expected-cost overbooking policy under a cap the clinic sets and the system never exceeds
- A backtest that replays the policy against weeks that already happened
- A fairness check on calibration by group, drift monitoring, and a hash-chained audit log
- MCP tools for clinic operations agents
- At Implementation: write-back to the scheduling system with the cap enforced

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own. It is for a team with its own developers: you run it and connect it to your data yourselves. No result on your data is promised at this step.
- **PoC.** A decision, not software. You export your appointment history once as a CSV, with no integration. The model is refitted and calibrated on it, and the overbooking policy is replayed against weeks that already happened. It ends, within one week of a usable export, in a written go or no-go, which may be "do not buy the build". No quality is promised before your data has been seen: you pay for the verdict, whatever it says.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/no-show-prediction/

To ask for a Scaffolding or a PoC, use the **Request this build** button on that page.

## What it does not promise

Overbooking is a risk trade, not a free win: the cap bounds your exposure and does not promise zero turned-away patients. The reference figures on the product page come from a public dataset, not from your practice.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
