# T15.v2 — Dalton's 80% Rule, Era-Corrected
**Status:** Rejected

## Headline verdict
The "80% rule" says that once price opens outside the prior day's value area and then closes two half-hour bars back inside it, it should travel to the opposite edge about 80% of the time. On NQ the rate was 45%, and no better than a fair same-year baseline.

## Why it matters
The rule is one of the best-known ideas in auction-market trading. It deserves a fair test, so the first version's flaw was corrected rather than the result accepted.

## The evidence
- Event: opens outside the prior value area, then two consecutive 30-minute bars close inside it. Outcome: price reaches the opposite edge before 15:59.
- 933 events; hit rate 45.4% (90% CI 42.7% to 48.1%). The CI excludes 80%.
- Opened above 46.9% (512 events); opened below 43.7% (421 events).
- Event minus same-year baseline: −0.07 points. Status: inconclusive across all three tests.
- Descriptive: price reached the prior session's point of control (the price with the most volume) in 71.3% of events.

## How we got here
- **Why v2:** the original test compared against a fixed distance in points across 2010–2026, but NQ's price rose roughly 15x, so the baseline was high early and low late. v2 expresses distance as a percentage of the open and uses a same-calendar-year baseline. The original result stands unchanged. v2 is post-hoc.
- **Value area:** 68% of volume, 2.5-point price buckets, built from the prior session.
- **Data:** NQ 1-minute bars (Databento GLBX.MDP3), 4,001 usable sessions. Block bootstrap (10-session blocks, 5,000 resamples); three tests in their own Benjamini-Hochberg family at q = 0.10.

## Caveats
Gross of costs. Uses a 68% value area on futures volume; other definitions of value area could differ. NQ futures points.
