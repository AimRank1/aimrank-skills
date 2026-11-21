# aml-triage-lite: free AimRank teaser skill

Prioritise AML/fraud alerts in Claude Code with **a reason and a confidence per alert**. A free teaser of the method behind AimRank's AML / Fraud Detection product.

*Methodology reference: [Stripe's Radar](https://stripe.com/guides/primer-on-machine-learning-for-fraud-protection), real-time machine-learning fraud scoring. Referenced for method only; AimRank is not affiliated with Stripe.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/aml-triage-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/aml-triage-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Triage the flagged transactions in ./alerts.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A risk-ranked queue with the typologies behind each alert
- Two-pass confidence + ⚠️ flags for the analyst
- A red-flag typology rubric (structuring · velocity · geography · counterparty)

## What it does not do

This skill ranks the alerts in one file inside one conversation. It trains no model, its score is a ranking and not a calibrated probability, it sees no account history or counterparty network beyond the file, and it keeps no audit trail. The disposition and any report to the authorities stay with the analyst.

## The full product

This skill is a teaser for AimRank's **AML / Fraud Detection**, which on 21 November 2026 is listed on its product page as a blueprint. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/aml-fraud-detection/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
