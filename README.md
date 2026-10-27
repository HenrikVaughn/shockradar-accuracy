# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-10-27 at 00:00 UTC.  **Catalog checked:** 2026-10-27 03:48 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 1 | 88.25 | 92.9% | 100.0% | 100.0% |
| 7 days | Pending | — | — | — | — |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 50.0% | 15.6% | 74.3% | 0.00468 |
| 1d | M5+ | 99.5% | 16.7% | 12.5% | 58.2% | 0.00187 |
| 1d | M6+ | 100.0% | 50.0% | 100.0% | 75.0% | 0.00061 |
| 7d | M4.5+ | — | — | — | — | — |
| 7d | M5+ | — | — | — | — | — |
| 7d | M6+ | — | — | — | — | — |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
