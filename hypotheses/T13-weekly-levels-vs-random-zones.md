# T13/T13b — Weekly Levels vs. Random Zones
**Status:** Rejected

## Headline verdict
Weekly price levels hold no better than random zones at the same distance. The answer matches the daily-level test.

## Why it matters
A longer timeframe is often said to make levels "stronger." This checks that claim directly for weekly highs, lows, value areas and weekly average prices.

## The evidence
- 13 weekly level types (prior-week high/low on full and regular sessions, value-area and POC levels, anchored and weekly VWAP, meaning volume-weighted average price). Event counts ranged from about 240 to 360 per level. All read inconclusive against matched controls.
- T13b (post-hoc): the 68%-volume value-area version of each profile level, 6 variants, about 320 events each. All inconclusive.
- Pre-set rule: a level counted as confirmed only if its hold rate beat matched controls with a 90% interval excluding zero, in both halves, at q <= 0.10. The 3-point practical yardstick was adopted later, with the T17/T18 tests, and is applied here afterwards. The largest weekly difference was the prior-week low (full week) at +2.3 pp, 90% interval -0.5 to +4.9, q = 0.49. Each weekly level has only 244 to 357 touches, so the intervals are wide (several reach about +4 to +5 points) and smaller effects cannot be ruled out.

## How we got here
Same method, data and controls as [T12/T12b](T12-daily-levels-vs-random-zones.md): NQ 1-minute bars, 2010–2026, 20 distance-matched controls per level, block bootstrap, Benjamini-Hochberg across the family. T13b used 655 weeks and was chosen after the first results, so it is exploratory.

## Caveats
Weekly levels have far fewer events than daily ones, so small effects would be hard to detect. Gross of costs. NQ futures points.
