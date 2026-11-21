# handicapping-fights-lite: free AimRank teaser skill

Handicap a fight card in Claude Code with **a reasoned lean per bout**, honestly framed as a ranking and not a betting model. A free teaser of the method behind AimRank's Fight Outcome Model blueprint.

*Methodology reference: [Betfair's guide to staking methods](https://betfair-datascientists.github.io/gettingStarted/stakingMethods/). Referenced for method only; AimRank is not affiliated with Betfair.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/handicapping-fights-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/handicapping-fights-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Handicap the card in ./card.md"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A reasoned lean per bout with the factors behind it
- A confidence rating + what would change it
- Honest framing: a ranking, not a calibrated stake signal

## What it does not do

This skill reads one card inside one conversation. Its lean is not a calibrated probability, it estimates no edge against the market, it sizes no stake, and it keeps no record of picks against results. It is not betting advice.

## The full product

This skill is a teaser for AimRank's **Fight Outcome Model + Optimal Bet Sizing**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/mma-outcome-model/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
