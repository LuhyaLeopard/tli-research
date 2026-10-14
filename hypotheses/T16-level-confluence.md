# T16 — Level Confluence vs. Random Zones
**Status:** Rejected

## Headline verdict
Zones where several levels stack together do not hold better than random zones at the same distance. They only look stronger when compared with single levels.

## Why it matters
"More levels in one place means a stronger level" is a common rule of thumb. This shows where the apparent strength comes from, and it is not the stacking.

## The evidence
Hold rate of confluence zones against two comparisons:

| Zone | Touched | Hold rate | vs matched random zones | vs single-level zones |
|---|---|---|---|---|
| 2 levels within 15 points | 3,058 | 54.4% | +0.2 pp (q = 0.75) | +1.5 pp (q = 0.75) |
| 3+ levels within 15 points | 2,192 | 64.5% | +0.3 pp (q = 0.75) | +11.6 pp (q = 0.003) |

The 3+ result "supports" only against single-level zones. Those zones cluster closer to the open and the sample mixes eras; against distance-matched random zones the edge is 0.3 pp. Within each half, the gap versus singles shrinks to about +1 to +3 pp.

## How we got here
- **Levels (17):** prior high/low/close, overnight high/low, prior-week high/low, value-area proxies, 68% profile levels and volatility-band edges, all known before the open.
- **Zoning:** sort levels, group any within 15 points of the lowest unassigned one; groups of 2 or more are confluence zones; zone = group mean ± 12.5 points.
- **Controls:** 20 distance-matched random zones per confluence zone. Four tests, Benjamini-Hochberg q = 0.10.
- **Data:** NQ 1-minute bars (Databento GLBX.MDP3), 2010–2026.

## Caveats
Gross of costs. Excludes options-based levels, which have no usable history. NQ futures points.
