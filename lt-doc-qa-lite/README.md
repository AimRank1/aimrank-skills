# lt-doc-qa-lite: free AimRank teaser skill

Answer questions from Lithuanian documents in Claude Code: **cited per claim, or an honest 'nežinau'**. A free teaser of the method behind AimRank's Lithuanian Document Q&A blueprint.

*Methodology reference: [Uber's Genie](https://www.uber.com/blog/genie-ubers-gen-ai-on-call-copilot/), a copilot that answers from internal documents with citations. Referenced for method only; AimRank is not affiliated with Uber.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/lt-doc-qa-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/lt-doc-qa-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Answer from the documents in ./docs/: <your question>"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- Answers grounded only in your documents
- A verbatim citation behind every claim
- An honest 'nežinau' instead of a guess when unsupported

## What it does not do

This skill answers from the documents you put in one conversation. It has no index or retrieval over a larger corpus, its decision to say `nežinau` is a judgment and not a tuned threshold, and it logs nothing.

## The full product

This skill is a teaser for AimRank's **Lithuanian Document Q&A (RAG)**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/document-qa-lt/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
