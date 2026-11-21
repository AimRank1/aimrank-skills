# demand-forecast-lite: free AimRank teaser skill

Forecast demand in Claude Code with **honest P10/P50/P90 ranges** instead of false-precision points. A free teaser of the method behind AimRank's Demand Forecasting product.

*Methodology reference: [Amazon's DeepAR](https://arxiv.org/abs/1704.04110): forecast a distribution, not a number. Referenced for method only; AimRank is not affiliated with Amazon.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/demand-forecast-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/demand-forecast-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Forecast next 14 days per SKU from ./sales.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you need

A CSV with `date`, `store`, `SKU` and `units`; `promo` and `price` columns help if you have them. Dates must be ISO (`YYYY-MM-DD`); any other format is asked about, not guessed.

## What you get

- A P10/P50/P90 range per SKU/store and day, 14 days ahead by default
- A check of the range against your own last weeks, where the history allows
- Calendar (incl. Lithuanian public holidays), promo and new-SKU adjustments called out
- ⚠️ flags on wide-uncertainty cases

## What it does not do

This skill forecasts from one CSV inside one conversation. Its range is a judgment checked, at best, against your own last two weeks. It is not calibrated, it is not backtested against a pass/fail test, and it keeps no record of forecasts and outcomes.

## The full product

This skill is a teaser for AimRank's **Demand Forecasting (LT calendar)**, which on 21 November 2026 is listed on its product page as a blueprint. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/demand-forecasting/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
