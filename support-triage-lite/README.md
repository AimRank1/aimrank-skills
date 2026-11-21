# support-triage-lite: free AimRank teaser skill

Triage Lithuanian support tickets in Claude Code: **intent, urgency, and a draft reply in the right language**. A free teaser of the method behind AimRank's Lithuanian Support Triage blueprint.

*Methodology reference: [Intercom's Fin](https://www.intercom.com/blog/fin-over-email-how-we-built/), an AI agent that answers from a company's own support content and hands over to a person. Referenced for method only; AimRank is not affiliated with Intercom.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/support-triage-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/support-triage-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Triage the ticket in ./ticket.txt"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- Intent + urgency classification with a reason
- A first-draft reply in the ticket's language (LT/EN)
- Two-pass confidence + ⚠️ flags; nothing auto-sends

## What it does not do

This skill handles one ticket at a time inside one conversation. It is not connected to a helpdesk, routes nothing, grounds the draft only in the ticket itself (not in your policies or order data), keeps no record, and its confidence is agreement between two reads, not a calibrated probability.

## The full product

This skill is a teaser for AimRank's **Lithuanian Support Triage + Draft Replies**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are. People who use this skill can leave a work email on the product page; the page says whether that earns a code toward the product's Scaffolding.

Product page: https://www.aimrank.io/products/support-triage-lt/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
