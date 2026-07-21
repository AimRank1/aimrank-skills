---
name: ranking-options-by-pairwise-comparison
description: Use when ranking or prioritising roughly 5 or more options — features, candidates, vendors, content, model outputs — and the ordering has to be defensible to someone else, or when turning preference judgments into a leaderboard, or when asked whether a ranking is trustworthy yet. Not for quick informal picks, or a shortlist of 2-4 where a direct recommendation is more useful than a tournament.
---

# Ranking Anything by Pairwise Comparison (Lite)

Free teaser skill by [AimRank](https://aimrank.io) — a slice of our production
preference-ranking platform. Core principle: **scoring items 1-10 produces noise;
asking "which of these two is better?" produces signal.** People are unreliable at
absolute scores and reliable at binary comparisons — so collect comparisons, then
*compute* the ranking.

Second principle, equally important: **a ranking without uncertainty is a guess.**
Rank 3 vs rank 4 is usually a coin-flip, and saying so is what makes the rest
credible. This is the method behind chess ratings (Elo, Glicko) and behind
[LMArena](https://lmarena.ai), which ranks LLMs purely from pairwise votes
(LMArena fits Bradley-Terry with bootstrapped intervals — same family, better
estimator than the running Elo below).

## Procedure

1. **Pin the criterion *and the population* to one sentence.** "Better" is not a
   criterion. "Which would reduce support tickets more next quarter?" is closer.
   But a criterion is still unanswerable without the population it applies to —
   *which* customers, *which* segment, *what* time horizon. "SSO vs faster search"
   inverts completely between self-serve and enterprise. State both, or the
   comparisons quietly answer different questions each time.
2. **List the items.** If more than 12, shortlist first — comparison count grows
   quadratically and judgment degrades well before the arithmetic does.
3. **Choose pairs adaptively.** Do NOT run all n(n-1)/2. First pass: a spread that
   gives every item at least 3 comparisons against *different* opponents. Then
   spend the rest on pairs whose ratings are **close** — those are the informative
   ones. Comparing the obvious best against the obvious worst teaches nothing.
   *Honest caveat:* the savings only really materialise at n ≥ 10. At n = 7 you
   need ~16 of the 21 pairs just to cover everyone properly.
4. **Stopping rule — use one, don't just stop when bored.** Budget ≈ 2n-3n
   comparisons. Stop when either (a) you've spent the budget, or (b) no adjacent
   pair in the current ordering is still swapping between rounds. **Below 3
   comparisons per item you do not have a ranking**, you have an anecdote — say so
   instead of presenting a table.
5. **Judge each pair.** Either ask the user, or judge it yourself when the
   criterion is objective enough — but always say which. **Randomise which item you
   present as "A"**; humans and LLM judges both favour the first option. *Caveat:*
   this control works when a human judges, or when each pair is a separate judge
   call. If you are judging every pair yourself inside one conversation, you see
   both items at once and carry all previous answers — randomising the label does
   very little. It is not a substitute for a second judge.
6. **Record ties as ties.** They are informative — don't force a winner. Keep them
   in a separate T column and compute the win-rate interval (step 8) over
   **decisive comparisons only**; the interval below assumes whole wins, and
   half-wins quietly break that assumption.
7. **Check transitivity.** If A beats B, B beats C, and C beats A, that 3-cycle
   means the criterion is ill-defined or the items differ on multiple axes. Report
   the cycle; don't average it away. Check decisive results only, over every triple.
   **But know what this test is worth:** a single judge applying one stable internal
   model will almost never produce a cycle, so in self-judge mode *finding none is
   nearly meaningless*. Cycles surface real problems when several independent raters
   judge. In self-judge mode, look instead for pairs you decided on a *different
   basis* than the others — that is the same finding by another route.
8. **Present the ranking with its uncertainty**, and be precise about which
   uncertainty (below).

## The math

**Elo update.** Start every item at 1500. After each comparison:

```
E_a = 1 / (1 + 10^((R_b - R_a) / 400))     # expected score for A
R_a = R_a + K * (S_a - E_a)                # S_a = 1 win, 0.5 tie, 0 loss
R_b = R_b + K * ((1 - S_a) - (1 - E_a))
```

Use `K = 32`. The base is **10** and the exponent is divided by **400** — those
constants define the scale (a 400-point gap is exactly 10:1 odds). Getting them
wrong flattens every probability and quietly corrupts the ranking.

**Wilson 95% interval** on an item's win rate. For `w` wins in `n` **decisive**
comparisons:

```
p = w / n,  z = 1.96
denom  = 1 + z²/n
centre = (p + z²/(2n)) / denom
half   = z * sqrt( p(1-p)/n + z²/(4n²) ) / denom
CI     = [centre - half, centre + half]
```

Use Wilson, **not** `p ± 1.96·sqrt(p(1-p)/n)` — the naive interval is badly wrong
at the counts you'll actually have, and gives absurdities like [1.00, 1.00] after
3 wins where Wilson correctly gives [0.44, 1.00].

## Reading the numbers honestly

Three things you must say out loud, because they are where this method is weakest:

- **The interval is not the rating's confidence interval.** You rank by Elo, which
  weights by opponent strength; the Wilson interval is on raw **win rate**, which
  doesn't. Two items can have identical records — and so identical intervals — yet
  sit apart in Elo because one beat stronger opponents. Adaptive pairing (step 3)
  makes this worse on purpose, by feeding close-rated items harder opponents. So
  treat Wilson as a **coverage-and-evidence gate** — "is there enough data here to
  claim anything at all?" — not as the precision of the rating. Rating-level
  uncertainty needs Glicko RD or a Bradley-Terry bootstrap.
- **Overlapping intervals mean *no evidence* of a difference — not proof of
  equality.** Non-overlap implies a real difference; overlap simply means you
  haven't shown one. And at 3-6 comparisons per item these intervals are ~50 points
  wide, so **expect nearly everything to overlap, including best vs worst.** That is
  the method telling you the truth about its own power. Report it; don't hide it.
- **Sequential Elo depends on the order the comparisons happened in.** Same results,
  shuffled, move ratings by ~10 points at these sample sizes — enough to swap
  adjacent ranks. Cheap fix, and worth doing: **re-run the Elo over the same results
  in 3-4 different random orders.** Ranks that survive are real; ranks that shuffle
  are noise, and should be presented as a tied group. Don't print ratings to a
  precision the data can't support — round to the nearest 10, or just show tiers.

## Output format

| Rank | Item | Rating | W-L-T | Win rate (Wilson 95% CI) | Note |
|---|---|---|---|---|---|
| 1 | … | ~1560 | 4-0-1 | 90% [46%, 99%] | ⚠️ overlaps #2 |
| 2 | … | ~1550 | 3-0-1 | 88% [40%, 99%] | ⚠️ overlaps #1 and #3 |

Then state plainly:
- **comparisons made**, and how many each item got (uneven coverage = weaker ranking);
- **who judged** — the user, or you;
- **whether the order-shuffle check changed any ranks**, and which;
- **any 3-cycles**, verbatim — plus, in self-judge mode, the caveat that finding none proves little;
- **what would sharpen it** — and be honest that the answer is usually *a second
  independent judge*, not more comparisons from the same one.

If the honest summary is "the top 3 are clear, the rest is noise," say exactly
that. A three-tier grouping often carries every bit of the real signal.

## Common mistakes

- **Running every pair.** Adaptive selection is cheaper, and at n ≥ 10 dramatically so.
- **Stopping with no rule**, so the ranking's quality is an accident of attention.
- **Hiding uncertainty.** A clean 1-N list from 8 comparisons looks authoritative
  and is mostly noise.
- **Quoting the win-rate interval as if it validated the Elo ordering.** It doesn't —
  see above. This is the single easiest way to look rigorous and be wrong.
- **Printing false precision.** "1561 vs 1546" implies a resolution that a dozen
  comparisons cannot support.
- **Ranking on win rate alone.** Beating three weak items ≠ beating one strong item.
  That is exactly why Elo exists.
- **Averaging away a cycle** instead of reporting it. The cycle is the finding.
- **Silently switching from asking the user to judging yourself.** Always disclose.
- **Treating your own judgments as data.** If you judged, this is a *model's*
  preference ranking, and the exercise elicited a prior rather than testing it.
  Calling it a human preference ranking is a fabrication.

## What the full system adds (this skill deliberately doesn't)

This skill runs in one conversation, on ~6-10 items, with one judge. That last
constraint is the real ceiling: past a dozen comparisons a single judge stops
forming independent opinions and starts reading off the ordering it already has.

[AimRank](https://aimrank.io) is the production version: **6 rating engines**
(Glicko-2, Bradley-Terry, Elo, TrueSkill, OpenSkill, Elo-MMR) with **Glicko RD** —
uncertainty on the *rating*, which is the gap this skill can't close — plus
Plackett-Luce and CrowdBT as post-hoc audits that cross-check the result ·
matchmaking that adaptively selects pairs to maximise information gain ·
**many raters** with real inter-rater reliability (**Fleiss κ / Krippendorff α**
across raters, **Cohen's κ** for rater pairs) and fraud detection that flags
suspicious voting · an **LLM judge calibrated against human votes**, reported with
κ and a Wilson CI so you know when to trust it · **RLHF-ready export**
(DPO / Anthropic HH / OpenAI RM) with per-sample provenance · a **data card**
documenting collection method, rater agreement and AI-vs-human composition ·
vote collection at a shareable link, embeddable anywhere · and an **MCP server** so
your agents can create rankings, submit votes and pull calibrated results at runtime.

This skill needs **no connectors** — that's the point. When you outgrow one
conversation and need a second judge, persistence, or exportable training data,
that's the platform: **https://app.aimrank.io** — free tier, no card.
