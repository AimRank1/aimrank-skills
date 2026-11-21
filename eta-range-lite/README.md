# eta-range-lite: free AimRank teaser skill

Estimate cross-border freight ETAs in Claude Code as an **honest range with the drivers**. A free teaser of the method behind AimRank's Cross-Border Logistics ETA blueprint.

*Methodology reference: [DoorDash's probabilistic ETAs](https://careersatdoordash.com/blog/improving-etas-with-multi-task-models-deep-learning-and-probabilistic-forecasts/). Referenced for method only; AimRank is not affiliated with DoorDash.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/eta-range-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/eta-range-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Estimate the ETA for the shipment in ./shipment.json"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A best/likely/worst range instead of a false-precision point
- The drivers behind the range (customs, transfers, weather)
- ⚠️ flags on high-variance lanes

## What it does not do

This skill estimates from the shipment details you give it inside one conversation. Its range is a judgment and not learned from your shipment history, it has no live border or carrier data, and it tracks nothing after the estimate.

## The full product

This skill is a teaser for AimRank's **Cross-Border Logistics ETA**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/logistics-eta/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
