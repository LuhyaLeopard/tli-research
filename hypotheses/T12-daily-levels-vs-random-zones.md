# T12/T12b — Daily Levels vs. Random Zones
**Status:** Rejected

## Headline verdict
Widely watched daily price levels (prior high, prior low, overnight high and low and similar) hold no better than randomly placed zones at the same distance from the open.

## Why it matters
Most chart-based trading assumes some prices matter more than others. If a "mapped" level does not hold better than a random one, the map adds nothing for entries, whatever it feels like on the screen.

## The evidence
Each level was scored on whether price touched it and then held, against 20 distance-matched random controls per level. Hold rate = held divided by (held plus broke). Held means a later hourly bar retreats at least 0.3% of price from the zone; broke means a close through the far side; unresolved touches are excluded.

- 14 daily levels tested (prior-day high/low/close, overnight high/low, prior-week high/low, value-area proxies, volatility-band edges). Before correction, 3 of the 14 carried a non-neutral label (1 "supports", 2 "against"); none beat controls by a practical margin.
- T12b (post-hoc, defined after the first results): three volume-profile levels (POC, value-area high and low, with POC meaning the price with the most traded volume). Best case was the value-area high: about +0.95 pp over controls, q = 0.35.
- Across all level tests, the best daily result was ONH at +0.8 pp (q = 0.41); the exploratory VAH68 reached +0.95 pp (q = 0.35). Pre-set rule: a level counted as confirmed only if its hold rate beat matched controls with a 90% interval excluding zero, in both halves, at q <= 0.10. The 3-point practical yardstick was adopted later, with the T17/T18 tests, and is applied here afterwards.

## How we got here
- **Data:** NQ front-month 1-minute bars (Databento GLBX.MDP3), 4,001 usable sessions, 2010–2026. Discovery 2010–2018, confirmation 2019+.
- **Scoring:** hourly regular-session bars; zone = level ± 12.5 points; side judged relative to the 09:30 open.
- **Controls:** 20 random zones per level, same side of the open, distance times a random factor between 0.8 and 1.2, seeded by date.
- **Statistics:** block bootstrap (10-session blocks, 5,000 resamples), Benjamini-Hochberg q = 0.10.
- **T12b is exploratory** because it was chosen after seeing T12.
- **What would change the call:** a level type that beats matched controls by 3 pp or more in both halves.

## Caveats
Gross of costs. NQ futures points. Says nothing about discretionary context around a level.
