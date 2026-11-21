# maintenance-risk-lite: free AimRank teaser skill

Flag equipment failure risk in Claude Code with **a reason and a rough lead time per asset**. A free teaser of the method behind AimRank's Predictive Maintenance blueprint.

*Methodology reference: [Shell's predictive maintenance programme](https://c3.ai/shell-achieves-major-milestone-scales-artificial-intelligence-predictive-maintenance-to-10000-pieces-of-equipment-using-c3-ai/), as reported by C3 AI. Referenced for method only; AimRank is not affiliated with Shell or C3 AI.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/maintenance-risk-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/maintenance-risk-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Flag failure risk from ./sensor_log.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A risk + urgency flag per asset with the driving signals
- Low-signal assets marked, not guessed
- A signal rubric (trend · usage · faults · gaps)

## What it does not do

This skill reads the logs you paste into one conversation. Its urgency window is a judgment, not a calibrated remaining-useful-life estimate, it learns no per-machine baseline, it writes nothing to a maintenance system, and it keeps no record of alerts and outcomes.

## The full product

This skill is a teaser for AimRank's **Predictive Maintenance**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/predictive-maintenance/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
