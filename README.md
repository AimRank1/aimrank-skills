# AimRank Skills

Free [Claude Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) from [AimRank](https://aimrank.io).

Each one teaches a method well enough to be genuinely useful on its own. No API key, no account, no connectors — you copy a folder into Claude and it works.

## Skills

| Skill | What it does |
|---|---|
| [`pairwise-ranking-lite`](pairwise-ranking-lite/) | Rank anything by pairwise comparison, with honest uncertainty. Exact Elo, exact Wilson intervals, adaptive pair selection, a stopping rule, position-bias control, and a transitivity check. |

## Install

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
cp -r aimrank-skills/pairwise-ranking-lite ~/.claude/skills/
```

Or drop the folder into `<your-repo>/.claude/skills/` to scope it to one project. Then just ask Claude the thing the skill is for — it triggers on its own.

## Where the line is

These are not crippled demos. `pairwise-ranking-lite` teaches the whole method, including the parts most write-ups skip: that a Wilson interval on win rate is not the confidence interval of an Elo rating, that overlapping intervals mean *no evidence* of a difference rather than proof of equality, and that sequential Elo is order-dependent enough at small n to swap adjacent ranks.

What a single conversation cannot do is persist anything, collect judgments from more than one person, measure inter-rater reliability, or export training data. That is the honest boundary, and each skill says where it sits.

When you hit that boundary, [AimRank](https://app.aimrank.io) is the production version — free tier, no card.

## License

Free to use, copy, modify and share, including at work. Keep the attribution notice in each skill. Not for resale as a product in its own right.

© AimRank 2026
