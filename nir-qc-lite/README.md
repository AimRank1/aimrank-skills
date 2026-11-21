# nir-qc-lite: free AimRank teaser skill

Turn NIR spectroscopy readings into an honest **PASS / REVIEW / FAIL / ABSTAIN** quality verdict in Claude Code, with a reason on every sample. A free teaser of the method behind AimRank's Spectroscopic QC Pipeline.

*Methodology reference: [an inline NIR study from Cipla](https://link.springer.com/article/10.1208/s12249-022-02392-9) (*AAPS PharmSciTech*, 2022) on real-time release of blends. Referenced for method only; AimRank is not affiliated with Cipla.*

## Install (30 seconds)

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
# personal (all projects)
cp -r aimrank-skills/nir-qc-lite ~/.claude/skills/
# or project-local
cp -r aimrank-skills/nir-qc-lite <your-repo>/.claude/skills/
```

Then in Claude Code: *"Read the NIR results in ./readings.csv against a 195 mg lower limit"*. The skill triggers automatically. No connectors, no API key, no account.

## What you need

A CSV of NIR readings per sample (a predicted value; ideally a prediction interval and a distance-to-training column) and the spec limits. No uncertainty columns → the verdict caps at REVIEW, and the skill tells you so.

## What you get

- A PASS / REVIEW / FAIL / ABSTAIN verdict per sample, read off the **interval**, not the point
- A plain-language reason per verdict (which limit or band drove it)
- ABSTAIN on out-of-domain samples: no compliance is asserted for a material the calibration never saw

## What it does not do

It is decision-support, not release: a person signs the batch (in pharma, the Qualified Person). NIR has hard limits (C3 syrups, low-ppm dyes, legal species identity → ABSTAIN, confirm with the reference method). A verdict is only as good as the calibration behind it, and this skill builds and validates none: it reads the columns you supply. "Defensible and auditable", never "court-proof".

## The full product

This skill is a teaser for AimRank's **Spectroscopic QC Pipeline**, which on 21 November 2026 is a reference build: built and measured on AimRank's own reference data, which does not mean a system running at a client. [GUIDE.md](GUIDE.md) says what the full product adds, what you get at each step of buying it, and where the prices are.

Product page: https://www.aimrank.io/products/spectroscopic-qc/

License: free to use and share as-is (keep this notice); not for resale.
© AimRank 2026.
