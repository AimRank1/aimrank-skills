# no-show-lite: free AimRank teaser skill

Rank appointment no-show risk in Claude Code from an **anonymised** schedule. A free teaser of the method behind AimRank's No-Show Prediction product.

*Methodology reference: [American Airlines' yield management](https://pubsonline.informs.org/doi/10.1287/inte.22.1.8) (*Interfaces*, 1992), the classic overbooking case. Referenced for method only; AimRank is not affiliated with American Airlines.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/no-show-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/no-show-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Rank no-show risk in ./schedule_anon.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A no-show risk ranking with the driving signals, each one measured on public data rather than assumed
- **The reminder trap**: why SMS reminders look like they *cause* no-shows (they don't), and how the sign flips once you condition on lead time
- Two-pass confidence + ⚠️ flags (incl. stray PII)
- Anonymised-data discipline: ranking only, no overbooking

## What it does not do

This skill ranks the appointments in one file inside one conversation. The rank is not a calibrated probability, so it cannot size overbooking. The skill writes nothing to a scheduling system and keeps no record.

## The full product

This skill is a teaser for AimRank's **No-Show Prediction + Safe Overbooking**, which on 21 November 2026 is built, with one of its own checks not yet cleared (the product page says which). [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/no-show-prediction/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
