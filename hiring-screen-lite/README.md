# hiring-screen-lite: free AimRank teaser skill

Draft a candidate shortlist in Claude Code, **scored on job-relevant evidence only, for a human to decide**. A free teaser of the method behind AimRank's Hiring Screening blueprint.

*Methodology reference: [LinkedIn's fairness-aware ranking](https://arxiv.org/abs/1905.01989), deployed to all LinkedIn Recruiter users per its paper. Referenced for method only; AimRank is not affiliated with LinkedIn.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/hiring-screen-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/hiring-screen-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Screen the CVs in ./candidates/ against ./role.md"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A fit ranking scored only on job-relevant criteria
- A reason per candidate + two-pass confidence
- A shortlist for a human, never an auto-reject

## What it does not do

This skill drafts a shortlist from the CVs in one conversation. It does not blind the documents before reading them, measures no adverse impact across groups, keeps no decision log, and is not a compliant high-risk system. It never rejects anyone.

## The full product

This skill is a teaser for AimRank's **Hiring Screening with Bias Controls**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/hiring-screening/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
