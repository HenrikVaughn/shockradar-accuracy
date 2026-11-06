# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-06 at 00:00 UTC.  **Catalog checked:** 2026-11-06 03:48 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 11 | 71.52 | 85.5% | 92.3% | 85.7% |
| 7 days | 5 | 293.57 | 77.8% | 86.3% | 76.2% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 55.8% | 15.1% | 77.1% | 0.00434 |
| 1d | M5+ | 99.7% | 26.9% | 21.2% | 63.4% | 0.00161 |
| 1d | M6+ | 100.0% | 14.3% | 50.0% | 57.1% | 0.00023 |
| 7d | M4.5+ | 94.5% | 86.5% | 28.8% | 90.6% | 0.01562 |
| 7d | M5+ | 97.3% | 54.1% | 21.5% | 75.9% | 0.00835 |
| 7d | M6+ | 99.9% | 23.8% | 83.3% | 61.9% | 0.00132 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
