# lt-invoice-lite: free AimRank teaser skill

Extract Lithuanian VAT invoices in Claude Code with a **citation and a confidence score on every field**. A free teaser of the method behind AimRank's Document Intelligence product.

*Methodology reference: [JPMorgan's DocLLM](https://arxiv.org/abs/2401.00908), a layout-aware document model. Referenced for method only; AimRank is not affiliated with JPMorgan.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/lt-invoice-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/lt-invoice-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Extract the invoice at ./inbox/invoice.pdf"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- The exact 18-field LT VAT invoice schema (flat, CSV/ERP-ready)
- A verbatim source quote for every extracted value
- Two-pass agreement (third read on disagreement), arithmetic and IBAN checks that override confidence, and quote verification against the page, giving a confidence and ⚠️ review flags
- LT-specific handling: legal-name inner quotes, decimal commas, VAT ID format, date normalization, transcribing diacritics exactly as printed
- A field the invoice does not print comes back `null`, never derived

## What it does not do

This skill reads one invoice at a time inside one conversation. It keeps nothing between conversations: no supplier memory, no database, no review queue and no audit trail. Its confidence is agreement between reads plus arithmetic checks, not a calibrated probability, and it quotes the source text but cannot highlight where a value sits on the page.

## The full product

This skill is a teaser for AimRank's **Document Intelligence - Lithuanian**, which on 21 November 2026 is a reference build: built and measured on AimRank's own reference data, which does not mean a system running at a client. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/document-intelligence-lt/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
