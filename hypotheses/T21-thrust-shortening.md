# T21 — Thrust Shortening (3m/15m/60m)
**Status:** Rejected

## Headline verdict
When a run of same-direction candles gets shorter and shorter, price does not reverse more often than usual. No timeframe or direction passed the significance filter.

## Why it matters
"The thrust is fading" is a common reason to fade a move. This tests that on 19,000+ runs.

## The evidence
Event: a run of same-direction bars whose ranges shrink three times in a row. Outcome: the next move reverses first. Compared with the same measure across all runs of that kind.

| Cell | Events | Event | Baseline | Difference | q |
|---|---|---|---|---|---|
| 15m up-runs | 349 | 52.2% | 47.4% | +4.9 pp | 0.437 |
| 15m down-runs | 305 | 49.1% | 48.7% | +0.5 pp | 0.894 |
| 3m down-runs | 1,041 | 51.6% | 51.4% | +0.2 pp | 0.894 |

All 6 cells (3m, 15m, 60m, up and down) failed the q filter; the smallest q was 0.437. The only interval excluding zero (15m up) fails correction.

## How we got here
- **Data:** NQ 1-minute bars aggregated to 3m, 15m and 60m, 19,166 events over 3,962 sessions.
- **v2 note:** the 60m average true range (ATR, a standard measure of typical bar size) is seeded from three prior sessions because 60m has only 7 bars a day; v1 left the 60m cells empty. Found in a dry run before any result was produced.
- **Statistics:** block bootstrap; Benjamini-Hochberg q = 0.10 across the 6 primary tests.

## Caveats
Gross of costs. Bar-shape rules can be defined many ways; this tested one frozen definition.
