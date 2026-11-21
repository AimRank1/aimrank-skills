# growth-model-lite: free AimRank teaser skill

Turn an activity log into a **user-state growth model** in Claude Code: where your users actually sit, what your real retention rates are, and **which lever moves DAU most**. A free teaser of the method behind AimRank's Calibrated Churn Predictor.

*Methodology reference: [Duolingo's growth model](https://blog.duolingo.com/growth-model-duolingo/), which Duolingo says helped grow daily active users 4× since 2019. Referenced for method only; AimRank is not affiliated with Duolingo.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/growth-model-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/growth-model-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Model the growth states in ./activity.csv"*. The skill triggers automatically. No connectors, no API key, no account.

## What you need

Two columns: `user_id`, `date`. One row per user per active day. That's it.

**Not** a one-row-per-customer table with a churn flag: that has no time axis, and this method cannot work on it.

## What you get

- Your users bucketed into 7 mutually exclusive states (`new`, `current`, `reactivated`, `resurrected`, `at_risk_wau`, `at_risk_mau`, `dormant`)
- A transition matrix: the real flow rates between them
- **CURR / NURR / RURR**: current-user, new-user and reactivated-user retention
- A **ranked lever table**: bump each rate 2%, roll forward, see what DAU does, sort
- A DAU reconciliation check, so you know the grid is right before trusting anything

## What it does not do

It's aggregate accounting, and it says so in its own output. Every user in a state gets the same number: in AimRank's reference run on the public [Lichess rated-games database](https://database.lichess.org/) (2013 to 2014), this model says users in `at_risk_wau` return 15.7% of the time, while a per-user model puts those same users anywhere from **1.8% to 40.4%** (10th to 90th percentile). A 22× spread you cannot aim a budget at. It gives no prediction interval, and it keeps nothing between runs.

That's the honest ceiling. It finds the lever; it can't tell you which users.

## The full product

This skill is a teaser for AimRank's **Calibrated Churn Predictor**, which on 21 November 2026 is a reference build: built and measured on AimRank's own reference data, which does not mean a system running at a client. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/churn-predictor/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
