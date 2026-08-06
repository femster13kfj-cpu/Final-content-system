# Performance Module

Everything else in this engine was built by analyzing other people's winners. This module is the mechanism that makes the repo learn from OUR results: it logs what we publish, judges it against our own baseline, promotes what wins into the pattern and example files, and feeds real numbers back into brand profiles and the rubric's validation log.

## What gets logged

Every published piece that came out of the engine, one entry in `log.md`, filed under the brand it ran for. If it shipped, it gets a row; pieces made outside the engine can be logged too when their numbers are worth learning from.

## The cadence: three touches per piece

1. **At publish:** create the entry. Date, brand, platform, format, goal, build doc link, the hooks used verbatim, the ramp, and the grades they shipped with. Two minutes, done while posting.
2. **At 48 hours:** first numbers. Early velocity is its own signal.
3. **At day 7:** final numbers and the verdict. If a post spikes later, update the entry whenever it's noticed.

An entry with blank number cells is fine. A guessed number is not: never estimate, a blank beats a fake. Real numbers only, same hard floor as receipts.

## One number decides: the goal metric

Each piece is judged FIRST by the metric its goal serves, the same mapping the Slide Job Framework uses:

| Goal | Goal metric |
|---|---|
| Capturing leads | Keyword comments + DMs (lead count) |
| Authority | Follows gained + profile visits |
| Virality | Shares + reach |
| Connection | Substantive comments |
| Educational | Saves |

Everything else is context. A lead-capture post with huge views and zero keyword comments did not win; it found a zero factor.

## The verdict: relative, never absolute

- **Baseline** = the median goal-metric number of that brand's last 10 posts on that platform. Recompute it lazily, whenever a verdict is being written.
- **2x baseline or better on the goal metric = WINNER.**
- **Under half of baseline = FLOP.**
- **In between = normal.** Log it and move on; most posts live here.
- **Override:** any post that produces a real lead, DM conversation, or client = WINNER regardless of numbers. Business results outrank metrics.
- Sandcastles outlier scores can stand in for the baseline math when the account is connected there.
- Under 10 posts of history (a new client account), log everything and skip verdicts until the baseline exists.

## The promotion rule (what happens to winners)

1. The winning hooks go into the matching layer's `examples.md` with the platform, the real numbers, and an ADAPT IT line, marked OWN RESULT. Our verified winners outrank analyzed strangers.
2. An entry lands in `swipe-file/inbox.md`.
3. The build doc's status section gets the numbers, per `_builds/README.md`.
4. The result becomes a receipt in the brand's profile: tier 5 in the brand's own file, and a client win ALSO logs to `clients/kyndle.md` as tier 4 material, worded for each brand.
5. If the result disagrees with its grade (shipped a B, ran 4x), it goes in the rubric's validation log for the quarterly review. Surprises are the most valuable rows in the whole system.

## The diagnosis rule (what happens to flops)

One line per flop, two possible diagnoses:

1. Which conversion factor was the zero (signal, trust, ramp, offer), per `conversion/funnel.md`, or
2. Which hook layer failed and how, using the failure types in `grading/revision-playbook.md`.

Three occurrences of the same failure means the GENERATION step needs the fix, not the revision step (playbook rule 3); log it in the rubric's validation log. The re-post rule applies: a flop with an A-grade hook was probably under-distributed; a flop with a B earns its revision pass and a repost with the better cover or opener.

## Cadence with the rest of the repo

- **Monthly**, in the same session as the swipe-file sort: sweep entries missing day-7 numbers, run pending promotions, prune noise.
- **Quarterly:** this log is the evidence base for the rubric review. The question the review asks: did our own winners and flops agree with the grades we gave them? Where they disagree, the rubric moves.

## Where numbers come from

Platform analytics directly (Instagram, Facebook, LinkedIn insights), or Sandcastles personal analytics when connected. Log the source in the entry the first time it's non-obvious.
