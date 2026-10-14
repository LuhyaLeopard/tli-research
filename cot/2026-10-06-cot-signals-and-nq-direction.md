# COT Signals and NQ Direction
**Status:** Shelved (weekly tests inconclusive; T2 N1 Rejected)

## Headline verdict
Weekly futures-positioning data (the CFTC's Commitments of Traders report) does not forecast Nasdaq futures direction beyond the standalone Commercials flag. Use it as weekly context, not as a trigger.

## Why it matters
COT gets a lot of attention as a "smart money" read. Tested over roughly two decades of weekly reports, none of the tested patterns gave a reliable directional edge.

## The evidence
Weekly tests on NQ positioning, entry on the Friday after each report, outcomes measured at 1, 4 and 8 weeks. Episode counts are small because weekly data is scarce.

| Idea | Episodes | Result |
|---|---|---|
| T1 — Commercials mirror (extreme Commercials position) | 48 | Inconclusive |
| T2 — Consecutive weeks of hedge-fund short covering (1 week) | 158 | Against the idea |
| T2 — 2 and 3 weeks | 98 / 55 | Inconclusive |
| T3 — Covering without institutional buying | 134 | Inconclusive |
| T4 — Crowded short in volatility futures | 42 | Inconclusive |
| T5 — Rising yields near a market high | 32 | Inconclusive |

No weekly COT test reached Confirmed.

## How we got here
- **Data:** CFTC Traders in Financial Futures and legacy reports (public), NDX closes from FRED, 2006 onward; discovery 2006–2018, confirmation 2019+.
- **Episodes:** anchored at the first event; later events within 4 weeks belong to it. Baseline = the same outcome at every entry Friday.
- **Statistics:** block bootstrap (8-week blocks, 5,000 resamples), Benjamini-Hochberg across every test in the batch.
- **Commercials flag:** a descriptive rule (commercial hedgers' net position in the top 10% of its 52-week range). It is reported as context and was not itself confirmed as a trading signal.
- **What would change the call:** a pattern with at least 30 episodes that holds in both halves after correction.

## Caveats
COT is published with a lag (Friday release of Tuesday positions). Small episode counts limit what can be detected. Gross of costs.
