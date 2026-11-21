# aml-triage-lite: free AimRank teaser skill

Put a fraud review queue in order in Claude Code, with **a reason and a confidence per payment**. A free teaser of the method behind AimRank's AML / Fraud Detection product.

*Methodology reference: [Stripe's Radar](https://stripe.com/guides/primer-on-machine-learning-for-fraud-protection): score every payment, and treat the threshold as a cost decision. This skill sees one file, not a network. Referenced for method only; AimRank is not affiliated with Stripe.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/aml-triage-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/aml-triage-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Triage the payments in ./payments.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you need

A CSV of payments. Timestamps must be ISO 8601 (`YYYY-MM-DDTHH:MM:SS`) and identifiers must be pseudonymous tokens; the skill asks instead of guessing.

## What you get

- A queue ordered by risk, each payment with the signals behind it and their values
- Two-pass confidence + ⚠️ flags for accounts with no history to compare against
- A signals rubric: velocity · amount · counterparty · place · device · channel and time

## What it does not do

Not transaction monitoring for money laundering, not sanctions screening, and not a decision: a person reviews every case. The score is a ranking, not a probability. It sees one file, trains no model and keeps no audit trail.

## The full product

This skill is a teaser for AimRank's **AML / Fraud Detection**, which on 21 November 2026 is listed on its product page as a blueprint. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/aml-fraud-detection/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
