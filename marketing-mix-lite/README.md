# marketing-mix-lite: free AimRank teaser skill

Read which channels appear to drive results in Claude Code: **a directional hypothesis with its caveats**. A free teaser of the method behind AimRank's Marketing Mix Model blueprint.

*Methodology reference: [Meta's Robyn](https://github.com/facebookexperimental/Robyn), the open-source marketing-mix modelling package. Referenced for method only; AimRank is not affiliated with Meta.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/marketing-mix-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/marketing-mix-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Read channel contribution from ./spend_revenue.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A per-channel contribution read with the signals behind it
- Confounders flagged (seasonality · promos · collinearity)
- The one experiment that would actually test it, honestly framed

## What it does not do

This skill reads one spend-and-results file inside one conversation. It fits no model: no adstock, no saturation curve, no interval. What it reports is correlation with caveats, not incrementality, and it should not move a real budget.

## The full product

This skill is a teaser for AimRank's **Marketing Mix Model + Budget Optimizer**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/marketing-mix-model/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
