# AimRank Skills

Free [Claude Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) from [AimRank](https://www.aimrank.io).

Each one teaches a method well enough to be genuinely useful on its own. No API key, no account, no connectors: you copy a folder into Claude and it works.

## Skills

### The ranking platform

| Skill | What it does |
|---|---|
| [`pairwise-ranking-lite`](pairwise-ranking-lite/) | Rank anything by pairwise comparison, with honest uncertainty. Exact Elo, exact Wilson intervals, adaptive pair selection, a stopping rule, position-bias control, and a transitivity check. |

### One per catalog product

Each of these teaches the first step of one product in the [AimRank catalog](https://www.aimrank.io/products/). Every folder carries a `GUIDE.md`: what the full product does that the skill does not, whether it is built yet, what you get at each step of buying it, and a link to the product page, which is the only place prices are published.

The status column is as of 21 November 2026; the product page shows the current one. **Blueprint** means designed and documented, not built: AimRank builds a blueprint once three businesses have requested it. **Reference build** means the code exists and has been run and measured on AimRank's own reference data, which is not the same as a system running at a client.

| Skill | What it does | Full product and status |
|---|---|---|
| [`lt-invoice-lite`](lt-invoice-lite/) | Extract Lithuanian VAT invoices with a source quote and a confidence on every field. | [#01 Document Intelligence - Lithuanian](https://www.aimrank.io/products/document-intelligence-lt/) · reference build |
| [`growth-model-lite`](growth-model-lite/) | Turn an activity log into user states, retention rates and a ranked lever table. | [#02 Calibrated Churn Predictor](https://www.aimrank.io/products/churn-predictor/) · reference build |
| [`support-triage-lite`](support-triage-lite/) | Triage Lithuanian support tickets by intent and urgency and draft a first reply. | [#04 Lithuanian Support Triage + Draft Replies](https://www.aimrank.io/products/support-triage-lt/) · blueprint |
| [`aml-triage-lite`](aml-triage-lite/) | Rank flagged transactions with a reason and a confidence per alert. | [#05 AML / Fraud Detection](https://www.aimrank.io/products/aml-fraud-detection/) · listed as a blueprint |
| [`brand-content-lite`](brand-content-lite/) | Draft on-brand marketing copy with a claims self-check. | [#06 Brand-Voice Content + Compliance Filter](https://www.aimrank.io/products/content-generation/) · blueprint |
| [`segmentation-lite`](segmentation-lite/) | Propose customer segments with a first bias read on each. | [#07 Segmentation with Bias Auditing](https://www.aimrank.io/products/segmentation-bias-audit/) · blueprint |
| [`demand-forecast-lite`](demand-forecast-lite/) | Forecast demand per SKU as a P10/P50/P90 range, with the Lithuanian calendar. | [#08 Demand Forecasting (LT calendar)](https://www.aimrank.io/products/demand-forecasting/) · listed as a blueprint |
| [`hiring-screen-lite`](hiring-screen-lite/) | Draft a candidate shortlist scored only on job-relevant evidence, for a human to decide. | [#09 Hiring Screening with Bias Controls](https://www.aimrank.io/products/hiring-screening/) · blueprint |
| [`maintenance-risk-lite`](maintenance-risk-lite/) | Flag equipment failure risk with a reason and a rough lead time per asset. | [#10 Predictive Maintenance](https://www.aimrank.io/products/predictive-maintenance/) · blueprint |
| [`no-show-lite`](no-show-lite/) | Rank appointments by no-show risk from an anonymised schedule, without falling into the reminder trap. | [#11 No-Show Prediction + Safe Overbooking](https://www.aimrank.io/products/no-show-prediction/) · built, gate not cleared |
| [`invoice-coding-lite`](invoice-coding-lite/) | Code invoices to GL codes with a reason and an anomaly check per line. | [#12 Invoice Classification + Anomaly Detection](https://www.aimrank.io/products/invoice-classification/) · blueprint |
| [`call-analysis-lite`](call-analysis-lite/) | Analyse a Lithuanian sales call: talk ratio, objections and next steps, each with a quote. | [#13 Sales Call Analysis (LT)](https://www.aimrank.io/products/sales-conversation-analysis-lt/) · blueprint |
| [`seo-clustering-lite`](seo-clustering-lite/) | Cluster keywords by search intent and turn the top gap into a brief. | [#14 SEO + Content Strategy](https://www.aimrank.io/products/seo-content-strategy/) · blueprint |
| [`defect-check-lite`](defect-check-lite/) | Triage product images for defects with a reason and a location per call. | [#15 Industrial Computer Vision QC](https://www.aimrank.io/products/industrial-cv-qc/) · blueprint |
| [`nir-qc-lite`](nir-qc-lite/) | Turn NIR readings into a PASS / REVIEW / FAIL / ABSTAIN verdict read off the interval. | [#16 Spectroscopic QC Pipeline](https://www.aimrank.io/products/spectroscopic-qc/) · reference build |
| [`ai-act-self-check-lite`](ai-act-self-check-lite/) | Classify a system under the EU AI Act and list the obligations with the date each applies from. | [#17 AI Act Compliance Evidence Pipeline](https://www.aimrank.io/products/ai-act-compliance-pipeline/) · built, gate not cleared |
| [`pricing-check-lite`](pricing-check-lite/) | Check proposed price moves against margin and fairness guardrails. | [#18 Dynamic Pricing for E-commerce](https://www.aimrank.io/products/dynamic-pricing/) · blueprint |
| [`eta-range-lite`](eta-range-lite/) | Estimate cross-border freight ETAs as a best/likely/worst range with its drivers. | [#19 Cross-Border Logistics ETA](https://www.aimrank.io/products/logistics-eta/) · blueprint |
| [`load-forecast-lite`](load-forecast-lite/) | Forecast electricity load as a P10/P50/P90 range. | [#20 Energy Demand Forecasting](https://www.aimrank.io/products/energy-forecasting/) · blueprint |
| [`virality-score-lite`](virality-score-lite/) | Score and rank drafts before posting, with the one fix that matters most. | [#21 Content Virality Predictor](https://www.aimrank.io/products/virality-predictor/) · blueprint |
| [`handicapping-fights-lite`](handicapping-fights-lite/) | Read a fight card into a reasoned lean per bout. A ranking, never a stake signal. | [#23 Fight Outcome Model + Optimal Bet Sizing](https://www.aimrank.io/products/mma-outcome-model/) · blueprint |
| [`lt-doc-qa-lite`](lt-doc-qa-lite/) | Answer from Lithuanian documents with a citation per claim, or an honest "nežinau". | [#24 Lithuanian Document Q&A (RAG)](https://www.aimrank.io/products/document-qa-lt/) · blueprint |
| [`marketing-mix-lite`](marketing-mix-lite/) | Read which channels appear to drive results, with the confounders named. | [#25 Marketing Mix Model + Budget Optimizer](https://www.aimrank.io/products/marketing-mix-model/) · blueprint |
| [`agent-guardrails-lite`](agent-guardrails-lite/) | Review an LLM agent and plan its guardrails across five rail layers. | [Agent Assurance](https://www.aimrank.io/products/agent-assurance/) · packaged product not built, waitlist open |
| [`review-response-lite`](review-response-lite/) | Break an online review into aspects and draft a reply that reveals no patient. | [#28 Reputation Guardian](https://www.aimrank.io/products/reputation-guardian/) · blueprint |

## Install

```bash
git clone https://github.com/AimRank1/aimrank-skills.git
cp -r aimrank-skills/pairwise-ranking-lite ~/.claude/skills/
```

Swap in the folder name of the skill you want, or drop the folder into `<your-repo>/.claude/skills/` to scope it to one project. Then just ask Claude the thing the skill is for: it triggers on its own.

## Where the line is

These are not crippled demos. `pairwise-ranking-lite` teaches the whole method, including the parts most write-ups skip: that a Wilson interval on win rate is not the confidence interval of an Elo rating, that overlapping intervals mean *no evidence* of a difference rather than proof of equality, and that sequential Elo is order-dependent enough at small n to swap adjacent ranks.

What a single conversation cannot do is persist anything, collect judgments from more than one person, measure inter-rater reliability, or export training data. That is the honest boundary, and each skill says where it sits.

When you hit that boundary with `pairwise-ranking-lite`, [AimRank](https://app.aimrank.io) is the production version: free tier, no card.

The product skills hold the same line, with one difference: most of their full products are blueprints, and each skill and its `GUIDE.md` says so. A skill mentions its full product at most once in a conversation, and only when you ask for something the skill says it does not do. There is no sales line at the end of a run.

## License

Free to use, copy, modify and share, including at work. Keep the attribution notice in each skill. Not for resale as a product in its own right.

© AimRank 2026
