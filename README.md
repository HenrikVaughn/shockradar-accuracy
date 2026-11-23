# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-23 at 00:00 UTC.  **Catalog checked:** 2026-11-23 04:11 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 28 | 75.71 | 79.1% | 79.1% | 78.6% |
| 7 days | 22 | 301.50 | 72.3% | 73.8% | 84.7% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 52.4% | 15.6% | 75.4% | 0.00475 |
| 1d | M5+ | 99.7% | 17.8% | 14.5% | 58.8% | 0.00166 |
| 1d | M6+ | 100.0% | 7.1% | 50.0% | 53.6% | 0.00018 |
| 7d | M4.5+ | 94.5% | 81.5% | 29.7% | 88.1% | 0.01666 |
| 7d | M5+ | 97.3% | 56.5% | 20.7% | 77.1% | 0.00830 |
| 7d | M6+ | 99.9% | 25.4% | 55.6% | 62.7% | 0.00092 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
