# pairwise-ranking-lite — free AimRank teaser skill

Rank anything in Claude by **pairwise comparison with honest uncertainty** — instead of gut-feel ordering or 1-10 scores that don't survive scrutiny. A slice of AimRank's production preference-ranking platform.

*The method behind chess ratings (Elo/Glicko) and [LMArena](https://lmarena.ai), which ranks LLMs purely from pairwise votes.*

## Install (30 seconds)

```bash
# personal (all projects)
cp -r pairwise-ranking-lite ~/.claude/skills/
# or project-local
cp -r pairwise-ranking-lite <your-repo>/.claude/skills/
```

Then in Claude: *"Rank these 8 features by which would cut support tickets most"* — the skill triggers automatically. No connectors, no API key, no account.

## What you get

- A ranking computed from comparisons (Elo), not from vibes
- A **Wilson 95% interval** per item, correctly framed as an evidence gate rather than a rating CI
- **Adaptive pair selection** plus an explicit **stopping rule**, so you don't run all n(n-1)/2
- An **order-shuffle check** — re-runs the same results in several orders, so ranks that are just noise get reported as ties
- A **transitivity check**, with an honest note on when it's actually informative
- Disclosure of who judged: you, or the model

## Good for

Feature prioritisation · vendor/candidate shortlists · content or creative picks · comparing model outputs · any "which of these is better" call you need to defend to someone else.

## What it deliberately won't do

One conversation, ~6-10 items, one judge. It elicits and organises a judgment; it does not test that judgment against anyone else's. Past a dozen comparisons a single judge stops forming independent opinions. That ceiling is real, and the skill says so where it matters.

## What the production system adds

6 rating engines with **Glicko RD** (uncertainty on the rating itself) plus Plackett-Luce and CrowdBT as post-hoc audits · information-gain matchmaking · many raters with real inter-rater reliability (**Fleiss κ / Krippendorff α** across raters, **Cohen's κ** for pairs) + fraud flagging · an LLM judge calibrated against human votes · RLHF-ready export (DPO / Anthropic HH / OpenAI RM) with per-sample provenance · a data card documenting collection method and rater agreement · shareable + embeddable vote collection · MCP server for agents.

**https://app.aimrank.io** — free tier, no card.

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
