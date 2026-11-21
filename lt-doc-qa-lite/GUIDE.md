# Lithuanian Document Q&A (RAG): what the full product does

This guide ships with the free skill `lt-doc-qa-lite`. It says what the full product does that the skill does not, what you get at each step of buying it, and where the prices are. It quotes no prices: they live on the product page, and a copy of this file on your machine would not follow them when they change.

**Status on 21 November 2026: blueprint.** The product is designed and documented, and it is not built yet. AimRank builds a blueprint once three businesses have requested it. The [product page](https://www.aimrank.io/products/document-qa-lt/) shows the current status.

## Where the free skill stops

This skill answers from the documents you put in one conversation. It has no index or retrieval over a larger corpus, its decision to say `nežinau` is a judgment and not a tuned threshold, and it logs nothing.

## What the full product is designed to add

- Ingestion of PDFs, scans, tables and DOCX from SharePoint, S3 or a mailbox, split on Lithuanian sentence boundaries and re-indexed when documents change
- Lithuanian-aware hybrid retrieval: LT-tuned embeddings plus keyword search over lemmatised text
- No citation, no sentence: every sentence points at its passage, and click-to-source highlights the page
- Abstention at a tuned threshold, with the abstention rate reported
- An evaluation set built from your own questions: retrieval recall, groundedness, abstention calibration
- A hash-chained audit log per query, and MCP tools so your agents can query the corpus

## What you get at each step

- **Scaffolding.** The product's repository, delivered as a zip that you own, for a team with its own developers. This product is a blueprint, so there is no repository to deliver yet: it exists once the product is built.
- **PoC.** Scoped on request once the product is built. A PoC applies the product to a static export of your data, with no live connection to your systems, and ends in a written verdict. For a blueprint there is nothing to run yet, so no scope or timing is published.
- **Implementation.** Custom. The product connected to your live systems, deployed and monitored, with monthly assurance. It is quoted after a PoC, never before.

## Prices and how to ask

Prices are on the product page: https://www.aimrank.io/products/document-qa-lt/

To ask for this product, use the **Request this build** button on that page. Your request counts toward the three that start the build.

## A code for people who use this skill

No code is printed in this skill. People who use it can leave a work email on the product page. Whether that earns a code toward the product's Scaffolding, and what the code gives, is stated on that page and nowhere else.

## What it does not promise

It will not answer everything: questions your documents do not cover come back as "nežinau" with a pointer to the closest documents, by design.

---

Free skill and guide by [AimRank](https://www.aimrank.io). Keep this notice if you share it. Not legal, financial or compliance advice.
