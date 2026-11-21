# segmentation-lite: free AimRank teaser skill

Segment customers in Claude Code **with a first bias read on every segment**. A free teaser of the method behind AimRank's Segmentation with Bias Auditing blueprint.

*Methodology reference: [Fairlearn](https://github.com/fairlearn/fairlearn), the open-source fairness package started at Microsoft. Referenced for method only; AimRank is not affiliated with Microsoft or Fairlearn.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/segmentation-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/segmentation-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Segment the customers in ./customers.csv and check for bias"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- 3 to 6 described, actionable segments with sizes
- A per-segment bias read against protected proxies
- A rubric for describing segments (value · behaviour · lifecycle)

## What it does not do

This skill proposes segments from one table inside one conversation. It runs no clustering algorithm and no stability test, its bias check is a read and not a statistical disparate-impact test, and it produces no audit report. Do not use its output to decide eligibility or pricing.

## The full product

This skill is a teaser for AimRank's **Segmentation with Bias Auditing**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/segmentation-bias-audit/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
