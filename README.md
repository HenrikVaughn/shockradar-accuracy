# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-10 at 00:00 UTC.  **Catalog checked:** 2026-11-10 04:52 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 15 | 68.92 | 83.4% | 88.3% | 88.9% |
| 7 days | 9 | 280.62 | 77.5% | 83.3% | 84.8% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 53.5% | 14.5% | 76.0% | 0.00437 |
| 1d | M5+ | 99.7% | 23.3% | 16.1% | 61.6% | 0.00140 |
| 1d | M6+ | 100.0% | 11.1% | 50.0% | 55.6% | 0.00022 |
| 7d | M4.5+ | 94.5% | 86.9% | 27.6% | 90.8% | 0.01516 |
| 7d | M5+ | 97.3% | 54.6% | 18.8% | 76.2% | 0.00765 |
| 7d | M6+ | 99.9% | 24.2% | 61.5% | 62.1% | 0.00120 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
