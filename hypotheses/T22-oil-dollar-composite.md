# T22 — Oil/Dollar Composite vs. Nasdaq
**Status:** Shelved

## Headline verdict
Oil and dollar surges do not predict the next day's direction for Nasdaq futures. A dollar surge is followed by a wider next-day range, but that is a volatility pattern, not a direction signal, and a combined oil-and-dollar measure is no better than its parts.

## Why it matters
Macro moves are often read as clues for the next session. Direction is what a trader needs, and here it is absent.

## The evidence
Event: a surge in the oil, dollar or combined measure (z-score of 1.5 or more, meaning 1.5 standard deviations above its recent norm). Outcome: next NQ regular-session return and range.

| Factor | Outcome | Events | Difference vs base | q |
|---|---|---|---|---|
| Oil | next-day return | 240 | −0.03% | 0.861 |
| Dollar | next-day return | 260 | −0.11% | 0.142 |
| Combined | next-day return | 228 | −0.01% | 0.871 |
| Dollar | next-day range | 260 | +0.27% of open | 0.001 |
| Combined | next-day range | 228 | +0.14% of open | 0.090 |

The dollar-range effect is mostly in 2020 and 2025 and is much smaller in the discovery half (+0.09%) than the confirmation half (+0.47%), so it fails the consistency test. Volatility clustering (calm and wild days tend to come in streaks) was not controlled for.

## How we got here
- **Data:** NQ 1-minute bars, 2010–2026; oil and dollar series from public FRED data; 60-day windows for z-scores, known at the prior close.
- **Split:** discovery 2010–2018, confirmation 2019+, written into the spec first.
- **Composite rule:** useful only if it beats both single factors on every outcome. It beat neither.
- **Statistics:** block bootstrap; Benjamini-Hochberg q = 0.10.

## Caveats
Treat the dollar-range finding as a context note, not a result. Gross of costs.
