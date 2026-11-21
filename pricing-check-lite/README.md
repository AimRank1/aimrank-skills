# pricing-check-lite: free AimRank teaser skill

Check proposed price moves in Claude Code for **margin and fairness guardrails** before they go live. A free teaser of the method behind AimRank's Dynamic Pricing blueprint.

*Methodology reference: [Zalando's forecast-then-optimize pricing](https://arxiv.org/abs/2606.13741), validated in 23 A/B tests across 12 markets. Referenced for method only; AimRank is not affiliated with Zalando.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/pricing-check-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/pricing-check-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Check the proposed prices in ./price_moves.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- An elasticity read + margin impact per move
- Guardrail checks (margin floor · change cap · fairness)
- ⚠️ flags on violations and thin-data moves

## What it does not do

This skill reviews the price moves in one file inside one conversation. Its elasticity read is a judgment and not an estimate with error bars, it backtests nothing, it watches no competitor or stock signals, and it changes no live price.

## The full product

This skill is a teaser for AimRank's **Dynamic Pricing for E-commerce**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/dynamic-pricing/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
