# ai-act-self-check-lite: free AimRank teaser skill

Self-check an AI system against the EU AI Act in Claude Code: **risk class, obligations with their dates, and the honest evidence gap**. A free teaser of the method behind AimRank's AI Act Compliance Evidence Pipeline.

*Methodology reference: [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03993) (Mitchell et al., Google). Referenced for method only; AimRank is not affiliated with Google.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/ai-act-self-check-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/ai-act-self-check-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Run an AI Act self-check on this system: <describe it>"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A risk classification with the reasoning
- The obligations that follow from that class, with the date each applies from
- An honest list of the evidence you'd still need

## What it does not do

This skill classifies a system from your description inside one conversation. It measures nothing on the real system, generates no technical file, keeps no decision log, and is not legal advice: a qualified person confirms the risk class.

## The full product

This skill is a teaser for AimRank's **AI Act Compliance Evidence Pipeline**, which on 21 November 2026 is built, with one of its own checks not yet cleared (the product page says which). [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/ai-act-compliance-pipeline/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
