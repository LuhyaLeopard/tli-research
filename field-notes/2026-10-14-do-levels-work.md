# Do Trading Levels Work? 16 Years of Nasdaq Futures vs. Random Zones

**Version 1.0 · 2026-10-14 · Market: NQ (Nasdaq-100 futures), June 2010 to October 2026**
**Based on:** [T12 — Daily Levels vs. Random Zones](../hypotheses/T12-daily-levels-vs-random-zones.md) · [T13 — Weekly Levels vs. Random Zones](../hypotheses/T13-weekly-levels-vs-random-zones.md) · [T16 — Level Confluence vs. Random Zones](../hypotheses/T16-level-confluence.md)

**How to read this:** three layers. **Short answer** (30 seconds), **The story** (5 minutes), then **Full research** (exact definitions, data, every result, limits, and how to cite). Stop wherever you have what you need.

---

## Short answer

We tested 14 daily levels and 13 weekly levels, plus 9 exploratory profile levels, on about 4,000 trading days of Nasdaq-100 futures. None held better than randomly placed zones at the same distance from the day's open by a margin that survives correction for testing many levels (the lowest q-value was 0.35, where 0.10 or below was required). The biggest difference on any daily level was 1.5 points of hold rate, and that one was worse than random. Weekly levels have fewer touches, so smaller effects can't be ruled out there. Zones where three or more levels stack together look much stronger than single levels (+11.6 points) but not stronger than random zones at the same distance (+0.3). Levels remain useful as reference points. In this data, they carried no edge of their own.

---

## The story

### Why it matters

Most chart-based trading assumes some prices matter more than others: yesterday's high, the overnight low, last week's high. The idea is that price tends to stall or bounce there. If that were true, a level should hold more often than a spot picked at random. If it isn't, the lines on a chart are a handy map but not a signal.

### What we asked

One question: when price reaches a widely watched level, does it hold more often than when it reaches a spot chosen at random?

"Hold" has an exact meaning here. After price touches a 25-point-wide zone around the level, it **holds** if price then moves away from the zone by at least 0.3% (about 90 points at recent NQ prices) before an hourly bar closes through the far side. It **breaks** if an hourly bar closes through the far side first. If neither happens by the end of the day, that touch is set aside. The hold rate is holds divided by holds plus breaks.

### How we tested it: the dartboard

For every real level on every day, we built 20 random "dummy" zones on the same side of the day's open, at roughly the same distance from it (within 20% either way). If a real level has something extra, it should hold more often than its dummies. Matching the distance matters, because zones near the open behave differently from zones far from it. Without matching, the comparison is unfair.

We looked at the difference in hold rate between the real level and its dummies, and how uncertain that difference is. Because we tested dozens of levels, a few will look unusual by luck alone. We corrected for that.

### What we found

**Daily levels (14 of them: prior-day high, low and close; overnight high and low; prior-week high and low; volatility-band edges; and the prior day's volume-weighted average price and its one-standard-deviation lines).** Every daily level landed within 1.5 points of its random dummies, in either direction. Three of the 14 carried a label in the raw results: the overnight high looked slightly better (+0.8 points), and two volatility-band edges looked slightly worse (−0.9 and −1.5). After correcting for testing many levels, none cleared the bar (the overnight high's q-value was 0.41; the requirement was 0.10 or lower).

**Exploratory profile levels (3).** After seeing the first results, we added three levels from a standard volume profile (the price with the most traded volume, and the top and bottom of the zone holding 68% of volume). Because we chose them after seeing earlier results, we label them exploratory. The best was the profile's top edge at about +0.9 points (q = 0.35), far short of significance.

**Weekly levels (13).** The answer was similar, with a caveat. Each weekly level had only 244 to 357 touches over 16 years, so the results are noisier. The largest differences were around +2 points (the prior week's low: +2.3, with an interval from −0.5 to +4.9). None came close to significance, but these intervals are wide enough that we cannot rule out a small to moderate effect for weekly levels.

**Stacked levels.** A common rule of thumb says more levels in one place means a stronger level.

| Zone | Times touched | Hold rate | vs. random zones | vs. single-level zones |
|---|---|---|---|---|
| 2 levels within 15 points | 3,058 | 54.4% | +0.2 pp (q = 0.75) | +1.5 pp (q = 0.75) |
| 3 or more levels within 15 points | 2,192 | 64.5% | +0.3 pp (q = 0.75) | +11.6 pp (q = 0.003) |

("pp" means percentage points.) The three-level zones look strong against single levels, a gap that passes the test. But a random zone at the same distance from the open holds 64.2% of the time. The test's own diagnostic points to distance, not stacking: zones where levels cluster sit closer to the open. Within each half of the data, the gap against single levels shrinks to +2.5 and +1.3 points.

### A trap worth knowing

How you set up the comparison can manufacture an edge. When we compared each daily level against randomly placed zones *anywhere* in the day's range instead of at the same distance, the differences swung from −6.5 to +4.0 points. That's almost entirely distance. It is why the matched comparison is the one that counts.

### What this does and doesn't say

It says that, under these definitions, the level alone didn't predict a reaction. It does not say levels are useless: a level can still mark where an idea is wrong or where to take profit. It also can't speak to other markets, other definitions of "hold," discretionary judgment around a level, or levels built from options positioning, which have no usable history.

---

## Full research

### 1. Definitions (frozen before any result was seen)

The definitions for T12, T13 and T16 were written and committed on 2026-10-06 before any price data was downloaded. T12b and T13b were defined afterward and are labelled exploratory (section 4).

**Sessions.** Regular trading hours (RTH) are 09:30 to 15:59 ET. The open is the 09:30 bar's opening price; the close is the 15:59 bar's closing price. A day is valid only with a 09:30 bar, a 15:59 bar and at least 370 RTH one-minute bars. A day is analysed only if every bar from the previous session's 09:30 through its own 15:59 belongs to the same futures contract; days spanning a roll are skipped.

**Zone.** Level L becomes a zone [L − 12.5, L + 12.5] points, 25 points wide. Real levels and controls use the same width. (At NQ 30,000, 25 points is about 0.08% of price.)

**Side.** Relative to the day's 09:30 open: a zone above it is resistance, below it is support. A zone that contains the open is "started inside" and is not scored.

**Bars.** One-minute bars are combined into 60-minute RTH bars starting at 09:30 (09:30, 10:30, … 15:30; the last bar is 30 minutes). Bars with high equal to low are ignored.

**Touch, hold, break** (the existing `score_zone` rule, imported unchanged). The first bar that touches the zone is the touch: for resistance, the bar's high reaches the zone's bottom; for support, the bar's low reaches the zone's top.
- If the touching bar closes beyond the far side of the zone (resistance: above the top; support: below the bottom), the touch is a **break**.
- Otherwise, scanning later bars in order: a bar that retreats from the zone by at least 0.3% of price (resistance: low at or below the zone bottom × 0.997; support: high at or above the zone top × 1.003) marks a **hold**. A bar that closes beyond the far side marks a **break**. The hold check comes first within a bar.
- If neither happens before the day ends, the touch is **unresolved** and is excluded.
- **Hold rate** = holds ÷ (holds + breaks), over touched real zones. "Events" in the tables are touches that resolved as hold or break.

**Primary controls (distance-matched).** For each real level in a session, 20 control zones are drawn on the same side of the open at distance max(12.5, d × u) from the open, where d is the real level's distance from the open and u is uniform between 0.8 and 1.2. Draws are seeded by the session date plus the level name. Controls are scored by exactly the same rule, and a control that starts inside is not scored.

**Secondary controls.** Twenty zones per session with centres uniform across PDC × (1 ± σ) (weekly: the prior week's last RTH close ± one weekly σ), reported as a second comparison.

**Statistic.** For each level type, the hold rate of its real zones minus the hold rate of its own matched controls pooled over the same sessions. The claim being tested was "higher."

**Daily levels, T12 (14):**
- Prior-day high, low and close (PDH, PDL, PDC), from the previous valid RTH session.
- Overnight high and low (ONH, ONL), from the 18:00 ET bar the previous evening through 09:29.
- Prior-week high and low (PWH, PWL), from the previous Monday–Friday RTH sessions (at least 4 valid sessions required).
- Volatility-band edges: PDC × (1 ± 0.5σ) and PDC × (1 ± σ), where σ is the prior session's ^VXN close ÷ 16 ÷ 100.
- POC\*, VAH\*, VAL\*: the previous RTH session's volume-weighted average price and its ±1 volume-weighted standard deviation (typical price (H+L+C)/3 per one-minute bar, weighted by volume). These are labelled proxies, not a true volume profile.

**Weekly levels, T13 (13).** Levels from the prior week, scored over the following week against that week's first RTH open: prior-week high and low (full futures week, Sunday 18:00 to Friday 17:00, and RTH only); weekly volume-profile POC, VAH and VAL at 0.25-point resolution with a 70% value area (full and RTH versions); weekly volume-weighted average price (full and RTH); and a volume-weighted average price anchored at the prior week's low. Weekly samples use blocks of 4 weeks (655 weeks).

**Exploratory profile levels (T12b: 3 daily; T13b: 6 weekly).** A 68% value area on a profile with 2.5-point rows. Each one-minute bar's volume is spread equally over every row it touches. The point of control (POC68) is the row with the most volume. The value area is built outward from it, repeatedly adding the side whose next two rows hold more volume, until it holds at least 68% of volume. VAH68 is the top edge of the highest row and VAL68 the bottom edge of the lowest.

**Confluence zones, T16.** Seventeen distinct daily levels known before the open (the 14 above plus POC68, VAH68, VAL68). Sort ascending; take the lowest unassigned level and group every unassigned level within 15 points above it; repeat. A group of two or more is a confluence zone ("2" or "3+"), centred on the group's mean ± 12.5. A group of one is a single-level zone. All are scored like T12, with 20 distance-matched controls per confluence zone.

### 2. Data

- **Source:** Databento GLBX.MDP3, one-minute bars (`ohlcv-1m`), symbol `NQ.v.0` (continuous front month by volume), as of 2026-10-06.
- **Coverage:** 5,534,183 one-minute bars, 2010-06-07 to 2026-10-05. The run reports 4,068 valid RTH sessions and 4,001 usable sessions (single contract and volatility index available). Skipped: 128 invalid RTH days and 66 with a contract roll inside the reference window.
- **Prices** are NQ futures front-contract points, not the cash index. The volatility input is the prior day's ^VXN close (daily data from yfinance).
- **Cross-check:** Databento's 2026-10-02 session high, low and last matched independently verified figures exactly (31,282.50 / 30,988.00 / 31,070.00).
- **Splits:** discovery 2010-06-06 to 2018-12-31; confirmation 2019-01-01 onward.

### 3. Inference

Moving-block bootstrap over whole sessions (blocks of 10 sessions for daily levels, 4 weeks for weekly), 5,000 resamples, seed 20261006, reporting 90% intervals. Benjamini-Hochberg correction at q = 0.10: across all 37 tests in the first batch (T12, T13, and others), and across a separate family of 16 tests for T12b, T13b, T15 and T16. A result counted as "confirmed" only if the claimed outcome had the right sign, its interval excluded zero, both halves had at least 10 events with the right sign and at least half the size, q was 0.10 or lower, and no claimed outcome was significantly opposite.

### 4. Pre-registered versus exploratory

- **Pre-registered:** T12, T13 and T16 (defined before results were seen).
- **Exploratory:** T12b and T13b were defined after the T12 and T13 results were seen.
- **Practical yardstick:** a 3-percentage-point margin was adopted later, with the T17 and T18 tests. It was not part of the T12, T13 or T16 definitions. It is used here only afterward, as a way to read the sizes.

### 5. Results

**5.1 Daily levels, T12.** Differences are in percentage points of hold rate vs. matched controls; "vs. uniform" is the secondary comparison.

| Level | Touches | Hold rate | Matched | Difference | 90% interval | q | 2010–18 | 2019+ | vs. uniform |
|---|---|---|---|---|---|---|---|---|---|
| PDH | 1,156 | 54.1% | 54.6% | −0.4 | −1.3 to 0.5 | 0.667 | +0.4 | −0.9 | −6.5 |
| PDL | 1,148 | 60.7% | 61.0% | −0.2 | −1.3 to 0.7 | 0.801 | 0.0 | −0.3 | 0.0 |
| PDC | 1,436 | 56.9% | 56.5% | +0.4 | −0.4 to 1.2 | 0.649 | +0.7 | +0.3 | −3.8 |
| ONH | 1,449 | 55.8% | 55.0% | +0.8 | 0.1 to 1.5 | 0.409 | +0.5 | +0.9 | −4.9 |
| ONL | 1,519 | 59.7% | 59.7% | +0.1 | −0.7 to 0.8 | 0.986 | −0.9 | +0.4 | −1.0 |
| PWH | 596 | 58.7% | 58.9% | −0.1 | −1.6 to 1.2 | 0.975 | −0.2 | −0.2 | −2.1 |
| PWL | 492 | 63.6% | 62.6% | +1.0 | −0.6 to 2.7 | 0.617 | +3.2 | −0.7 | +2.8 |
| Band +0.5σ | 1,310 | 62.4% | 61.6% | +0.7 | −0.1 to 1.5 | 0.443 | +0.8 | +0.3 | +1.7 |
| Band −0.5σ | 1,374 | 64.7% | 65.6% | −0.9 | −1.8 to 0.0 | 0.424 | −1.3 | −0.6 | +4.0 |
| Band +1σ | 664 | 55.3% | 56.8% | −1.5 | −3.0 to −0.1 | 0.424 | −1.1 | −2.1 | −5.4 |
| Band −1σ | 798 | 63.0% | 63.7% | −0.7 | −1.9 to 0.5 | 0.617 | +0.6 | −1.6 | +2.4 |
| POC\* | 1,449 | 58.9% | 58.9% | 0.0 | −0.8 to 0.8 | 0.986 | −0.1 | 0.0 | −1.7 |
| VAH\* | 1,348 | 56.9% | 56.9% | 0.0 | −0.9 to 0.9 | 0.986 | −0.9 | +0.5 | −3.8 |
| VAL\* | 1,350 | 60.5% | 60.3% | +0.2 | −0.6 to 1.1 | 0.801 | +0.5 | −0.5 | −0.2 |

Raw labels: ONH "supports" (interval excludes zero); Band −0.5σ and Band +1σ "against"; the rest inconclusive. None was confirmed (q > 0.10 for every row).

**5.2 Exploratory daily profile levels, T12b.**

| Level | Touches | Hold rate | Matched | Difference | 90% interval | q | 2010–18 | 2019+ | vs. uniform |
|---|---|---|---|---|---|---|---|---|---|
| POC68 | 1,440 | 61.3% | 60.8% | +0.5 | −0.2 to 1.2 | 0.749 | +0.1 | +0.8 | +0.7 |
| VAH68 | 1,377 | 57.1% | 56.1% | +0.9 (0.95 from raw counts) | 0.2 to 1.8 | 0.346 | +0.6 | +0.9 | −3.5 |
| VAL68 | 1,328 | 60.3% | 60.3% | +0.1 | −0.8 to 0.9 | 0.960 | +0.4 | −0.2 | −0.3 |

**5.3 Weekly levels, T13.** All 13 were labelled inconclusive.

| Level | Touches | Hold rate | Matched | Difference | 90% interval | q | 2010–18 | 2019+ |
|---|---|---|---|---|---|---|---|---|
| Prior-week high, full | 302 | 51.7% | 52.1% | −0.5 | −2.9 to 1.9 | 0.830 | +1.6 | −1.6 |
| Prior-week low, full | 244 | 63.5% | 61.3% | +2.3 | −0.5 to 4.9 | 0.492 | +3.6 | +0.2 |
| Prior-week high, RTH | 311 | 51.1% | 51.0% | +0.1 | −2.3 to 2.5 | 0.986 | −0.4 | +0.5 |
| Prior-week low, RTH | 259 | 62.5% | 60.9% | +1.6 | −1.4 to 4.5 | 0.620 | +4.0 | −1.5 |
| POC, full | 315 | 58.7% | 60.0% | −1.2 | −3.3 to 0.9 | 0.617 | −0.3 | −2.2 |
| VAH, full | 329 | 56.8% | 56.1% | +0.7 | −1.3 to 2.7 | 0.772 | −2.5 | +3.3 |
| VAL, full | 311 | 62.7% | 60.8% | +1.9 | −0.4 to 4.1 | 0.492 | −1.0 | +4.5 |
| POC, RTH | 316 | 54.1% | 56.1% | −2.0 | −4.2 to 0.1 | 0.443 | −2.1 | −1.8 |
| VAH, RTH | 335 | 53.4% | 54.6% | −1.2 | −3.3 to 0.9 | 0.617 | −1.8 | −0.4 |
| VAL, RTH | 312 | 61.9% | 59.8% | +2.0 | −0.2 to 4.2 | 0.443 | +0.3 | +3.7 |
| Weekly VWAP, full | 348 | 53.4% | 55.1% | −1.6 | −3.8 to 0.4 | 0.495 | −1.7 | −1.5 |
| Weekly VWAP, RTH | 357 | 54.6% | 55.4% | −0.8 | −3.0 to 1.4 | 0.764 | +0.3 | −1.8 |
| VWAP anchored at prior-week low | 354 | 55.4% | 56.6% | −1.3 | −3.4 to 0.8 | 0.617 | −1.9 | −0.6 |

The six exploratory weekly profile levels (T13b) were all labelled inconclusive; see the T13 page for details.

**5.4 Confluence, T16.** Zones scored (not started inside): 2-level 7,107 (3,058 touched), 3+ level 4,815 (2,192 touched), single-level 19,041 (5,520 touched). Single-level zones held 52.9%.

| Comparison | Event | Control | Difference | 90% interval | q | 2010–18 | 2019+ |
|---|---|---|---|---|---|---|---|
| 2 levels vs. matched random | 54.4% | 54.2% | +0.2 | −0.3 to 0.7 | 0.749 | −0.1 | +0.4 |
| 2 levels vs. single-level zones | 54.4% | 52.9% | +1.5 | −0.4 to 3.4 | 0.749 | −0.7 | −0.8 |
| 3+ levels vs. matched random | 64.5% | 64.2% | +0.3 | −0.3 to 0.9 | 0.749 | +0.4 | +0.1 |
| 3+ levels vs. single-level zones | 64.5% | 52.9% | +11.6 | 9.4 to 13.8 | 0.003 | +2.5 | +1.3 |

### 6. Limitations

- Results are in NQ points and **gross of commissions and slippage.**
- **Definitions drive the answer.** The zone is a fixed 25 points while the hold threshold is 0.3% of price, so the threshold was about 6 points at NQ 2,000 and about 90 points at NQ 30,000. Controls use the same rule in the same era, so comparisons stay fair, but absolute hold rates (about 55–65%) are not comparable across eras. A price-scaled zone or a different hold rule could behave differently.
- **Weekly precision is low.** Intervals reach about +4 to +5 points for several weekly levels, so small to moderate effects are not ruled out there. Daily intervals are about ±1 point, which does rule out effects larger than roughly 1.5 to 2 points.
- **One market, one data vendor, hourly bars, one hold rule.** Different bar sizes or touch definitions were not tested.
- **Excluded:** options-based levels (no usable history), discretionary context, and costs.
- **Multiple testing** was corrected within each declared family of tests (37 in the first batch, 16 in the second), not across all tests ever run.
- Prices are the continuous front-month contract; days spanning a roll were skipped.

### 7. What would change the conclusion

A level type that beats its distance-matched controls by at least 3 percentage points in both halves of the data, with q of 0.10 or lower, in a test defined before its results are seen. A weekly-level test with more events than 16 years of weekly data can supply would also sharpen the weekly answer.

### 8. How to build on this

- The definitions above are complete enough to re-implement. The test scripts are not published.
- Raw price data is not included in this repository; it comes from Databento and is subject to their license.
- Open questions for anyone extending this: price-scaled zone widths and hold thresholds; other markets; options-based levels once history exists; weekly levels with more data.

### 9. Version, changelog and how to cite

- **v1.0, 2026-10-14:** first release.
- **Cite as:** Awori, C. (2026). *Do Trading Levels Work? 16 Years of Nasdaq Futures vs. Random Zones* (v1.0). TLI Research. https://github.com/LuhyaLeopard/tli-research

*Research and findings only; not financial advice.*
