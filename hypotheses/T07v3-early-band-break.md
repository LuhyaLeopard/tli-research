# T7.v3 — Early Band Break
**Status:** Rejected

## Headline verdict
When NQ breaks out of its expected daily range before 11:00 ET, it more often closes outside that range, but it finishes near the extreme of the move less often. The two results pull in opposite directions, so there is no clean edge.

## Why it matters
Traders often treat an early breakout as a sign of a trend day. This test checks whether that holds up over 16 years. It half does: the day is more likely to end outside the range, but it is much less likely to end at the high or low of the move, so chasing the break gives back ground.

## The evidence
Band = prior close ± 0.5 standard deviation of expected daily move (a volatility-based range). Early = first breach before 11:00 ET; comparison = breaches at 11:00 or later. 611 early-break episodes, 2010-06 to 2026-10.

| Outcome (claimed higher) | Early | After 11:00 | Difference | 90% CI | q* |
|---|---|---|---|---|---|
| Close outside band | 56.8% | 49.3% | +7.5 pp | +2.9 to +11.9 | 0.067 |
| Close in the breach-side quartile | 35.2% | 55.0% | −19.8 pp | −24.3 to −15.6 | 0.002 |

*q = p-value adjusted for running many tests at once (Benjamini-Hochberg, a standard multiple-testing correction).*

Both halves agree in sign: close outside band +7.0 pp (2010–2018) and +7.3 pp (2019+); side quartile −19.0 pp and −21.4 pp.

By timing, a break on the 09:30 bar itself closes outside the band 67.3% of the time (+18.1 pp, descriptive only), while breaks between 10:00 and 10:59 show no difference (−2.8 pp).

## How we got here
- **Data:** NQ front-month 1-minute bars (Databento GLBX.MDP3), 4,001 usable regular-hours sessions.
- **Definitions** were frozen before any result was seen. Event = first regular-session 1-minute bar breaching the band; one event per episode (later breaks within 5 sessions belong to the first).
- **Statistics:** moving-block bootstrap (blocks of 10 sessions, 5,000 resamples) for 90% CIs; Benjamini-Hochberg at q = 0.10 across all tests in the batch.
- **Ladder:** Confirmed needs the right sign, a CI excluding zero, both halves agreeing at no less than half the effect, q ≤ 0.10, and no claimed outcome significantly opposite. The first run read "Confirmed"; the opposing quartile result was caught and the ladder was tightened afterwards, which turned this into Mixed.
- **What would change the call:** a version of the rule that keeps the outside-band gain without the loss at the extreme.

## Caveats
Gross of commissions and slippage. Futures points, not cash index points. Not a trading rule.
