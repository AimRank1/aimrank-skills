# load-forecast-lite: free AimRank teaser skill

Forecast electricity load in Claude Code with **honest P10/P50/P90 ranges**. A free teaser of the method behind AimRank's Energy Demand Forecasting blueprint.

*Methodology reference: [National Grid ESO's solar nowcasting project with Open Climate Fix](https://www.neso.energy/news/former-deepmind-experts-ai-tool-could-help-boost-national-grid-esos-solar-forecasts), a neighbouring short-horizon forecasting problem. Referenced for method only; AimRank is not affiliated with National Grid ESO or Open Climate Fix.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/load-forecast-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/load-forecast-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Forecast day-ahead load from ./load_history.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A P10/P50/P90 load range per period
- Temperature + calendar drivers called out
- ⚠️ flags on wide-uncertainty periods

## What it does not do

This skill forecasts from one load-history file inside one conversation. Its range is a judgment and not a calibrated interval, it ingests no weather forecast runs, it prepares no regulatory reporting, and it archives nothing.

## The full product

This skill is a teaser for AimRank's **Energy Demand Forecasting**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/energy-forecasting/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
