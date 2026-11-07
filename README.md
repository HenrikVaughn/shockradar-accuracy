# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-07 at 00:00 UTC.  **Catalog checked:** 2026-11-07 03:21 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 12 | 71.12 | 84.6% | 89.1% | 87.5% |
| 7 days | 6 | 289.07 | 77.9% | 85.0% | 79.2% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.2% | 53.0% | 14.3% | 75.7% | 0.00438 |
| 1d | M5+ | 99.7% | 25.5% | 19.7% | 62.6% | 0.00158 |
| 1d | M6+ | 100.0% | 12.5% | 50.0% | 56.2% | 0.00024 |
| 7d | M4.5+ | 94.5% | 86.3% | 28.2% | 90.5% | 0.01547 |
| 7d | M5+ | 97.2% | 53.9% | 20.4% | 75.8% | 0.00813 |
| 7d | M6+ | 99.9% | 25.0% | 66.7% | 62.5% | 0.00127 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
