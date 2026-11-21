# invoice-coding-lite: free AimRank teaser skill

Code invoices to GL codes in Claude Code with **a reason and an anomaly check per line**. A free teaser of the method behind AimRank's Invoice Classification blueprint.

*Methodology reference: [Intuit's Rel-Cat](https://arxiv.org/abs/2506.09234), a graph-based transaction categoriser. Referenced for method only; AimRank is not affiliated with Intuit.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/invoice-coding-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/invoice-coding-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Code the invoice at ./invoice.pdf to GL codes"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A GL code + reason per line
- A VAT arithmetic sanity check
- Anomaly flags (duplicate · round · out-of-pattern · new vendor)

## What it does not do

This skill codes the invoices you give it inside one conversation. It has not learned your past coding decisions, its confidence is not calibrated, its anomaly flags see only what is in the conversation (no vendor history), and it posts nothing to an accounting system.

## The full product

This skill is a teaser for AimRank's **Invoice Classification + Anomaly Detection**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/invoice-classification/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
