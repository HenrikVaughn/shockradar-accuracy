# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-10-30 at 00:00 UTC.  **Catalog checked:** 2026-10-30 01:41 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 4 | 79.03 | 88.1% | 100.0% | 100.0% |
| 7 days | Pending | — | — | — | — |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.4% | 62.7% | 20.1% | 80.6% | 0.00442 |
| 1d | M5+ | 99.7% | 34.8% | 32.0% | 67.3% | 0.00171 |
| 1d | M6+ | 100.0% | 33.3% | 50.0% | 66.7% | 0.00024 |
| 7d | M4.5+ | — | — | — | — | — |
| 7d | M5+ | — | — | — | — | — |
| 7d | M6+ | — | — | — | — | — |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
