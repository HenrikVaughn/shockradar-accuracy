# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-04 at 00:00 UTC.  **Catalog checked:** 2026-11-04 03:27 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 9 | 74.63 | 84.7% | 91.3% | 85.7% |
| 7 days | 3 | 298.45 | 76.6% | 87.5% | 76.9% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 55.9% | 15.8% | 77.2% | 0.00440 |
| 1d | M5+ | 99.7% | 26.1% | 21.8% | 63.0% | 0.00171 |
| 1d | M6+ | 100.0% | 14.3% | 50.0% | 57.1% | 0.00028 |
| 7d | M4.5+ | 94.5% | 86.4% | 28.3% | 90.6% | 0.01611 |
| 7d | M5+ | 97.3% | 56.8% | 22.8% | 77.3% | 0.00808 |
| 7d | M6+ | 99.9% | 23.1% | 100.0% | 61.5% | 0.00135 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
