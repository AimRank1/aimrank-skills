# defect-check-lite: free AimRank teaser skill

Triage product images for defects in Claude Code with **a reason and a location per call**. A free teaser of the method behind AimRank's Industrial Computer Vision QC blueprint.

*Methodology reference: [Landing AI's steel-inspection case study](https://landing.ai/wp-content/uploads/2021/07/LandingAI_CaseStudy_Steel_Inspection.pdf). Referenced for method only; AimRank is not affiliated with Landing AI.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/defect-check-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/defect-check-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Check ./part.jpg for defects"*. The skill triggers automatically. No connectors, no API key, no account.

## What you get

- A defect/no-defect verdict with location + reason
- Confidence + image-quality awareness
- ⚠️ flags on ambiguous images for a human

## What it does not do

This skill looks at the images you give it inside one conversation. It is not trained on your product, its confidence is not calibrated, it has no measured escape or false-reject rate, it cannot run at line speed, and it stores no evidence.

## The full product

This skill is a teaser for AimRank's **Industrial Computer Vision QC**, which on 21 November 2026 is a blueprint: designed and documented, not built yet. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/industrial-cv-qc/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
