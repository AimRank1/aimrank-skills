# agent-guardrails-lite: free AimRank teaser skill

Review an LLM agent and get a layered **guardrail plan** in Claude Code: input, dialog, retrieval, execution and output rails, plus the human-approval gates. A free teaser of the method behind AimRank's Agent Assurance product.

*Methodology reference: [NVIDIA's NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) and its [five rail types](https://docs.nvidia.com/nemo/guardrails/latest/about-nemo-guardrails-library/rail-types). Referenced for method only; AimRank is not affiliated with NVIDIA.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/agent-guardrails-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/agent-guardrails-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Review this agent's tools and prompt and design its guardrails"*. The skill triggers automatically. No connectors, no API key, no account.

## What you need

A description of the agent: system prompt, the tools it can call, what it retrieves from, and its highest-stakes action. A config file or a paragraph is enough.

## What you get

- A rail-by-rail plan across all five layers (input · dialog · retrieval · execution · output)
- Each rail rated present / partial / missing, with the highest-risk gap flagged
- The one human-approval (🔴) gate that must exist before the agent gets authority

## What it does not do

It's a design review, not a runtime: it tells you which rails to build, it doesn't enforce them, test them or log anything. Rails trade off catch rate against false refusals. No guardrail removes the human on high-stakes actions.

## The full product

This skill is a teaser for AimRank's **Agent Assurance**, which on 21 November 2026 is not built as a packaged product: its page runs a waitlist. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/agent-assurance/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
