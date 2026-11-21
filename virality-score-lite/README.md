# virality-score-lite: free AimRank teaser skill

Score a draft before you post it in Claude Code: **a reasoned ranking with the one fix that matters**. A free teaser of the method behind AimRank's Content Virality Predictor blueprint.

*Methodology reference: [the "heavy ranker" in X's open-sourced recommendation code](https://github.com/twitter/the-algorithm-ml/blob/main/projects/home/recap/README.md). Referenced for method only; AimRank is not affiliated with X.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/virality-score-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/virality-score-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Score the draft in ./post.md before I publish"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A 0 to 100 score with the drivers behind it
- Head-to-head ranking of multiple drafts
- The single highest-leverage improvement, honestly framed as a ranking

## What it does not do

This skill scores the drafts you paste inside one conversation, from general practice. It has not seen your account history, its score is a ranking and not a forecast, and it never checks a prediction against what happened after posting.

## The full product

This skill is a teaser for AimRank's **Content Virality Predictor**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/virality-predictor/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
