# T25 — Post-13F Overlap Drift
**Status:** Shelved (definition only; no data for years)

## Headline verdict
No result yet, and none is expected for years. The test is defined here, in full, before any data exists so the method cannot be adjusted afterwards.

## Why it matters
Large institutions disclose holdings quarterly (Form 13F). When several of them add the same stock, does it drift differently afterwards? A fixed definition made now lets any future answer be taken at face value.

## The evidence
None yet. 13F filings arrive quarterly, so enough episodes take years to build.

## How we got here
Definition, frozen before any result:
- **Episode:** a stock added by 3 or more institutions in the same filing period (3+ institution overlap).
- **Measurement:** price drift at 1, 2, 3, 4, 5 and 6 weeks after the filing, each window tested separately.
- **Baseline:** a sector- or index-matched baseline, not zero.
- **Correction:** Benjamini-Hochberg applied across all six windows together once enough episodes exist.
- **What would change the call:** nothing, since results come later. Any change to the definition is a new version, reported separately.

## Caveats
13F data is delayed by up to 45 days after quarter-end, so drift is measured from the filing date, not from when positions were taken.
