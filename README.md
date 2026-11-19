# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-19 at 00:00 UTC.  **Catalog checked:** 2026-11-19 04:39 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 24 | 72.47 | 80.2% | 83.5% | 90.9% |
| 7 days | 18 | 291.27 | 72.6% | 79.5% | 89.8% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 53.1% | 15.7% | 75.8% | 0.00466 |
| 1d | M5+ | 99.7% | 20.4% | 15.2% | 60.1% | 0.00153 |
| 1d | M6+ | 100.0% | 9.1% | 50.0% | 54.5% | 0.00017 |
| 7d | M4.5+ | 94.5% | 82.3% | 29.4% | 88.6% | 0.01640 |
| 7d | M5+ | 97.3% | 57.7% | 19.8% | 77.7% | 0.00771 |
| 7d | M6+ | 99.9% | 30.6% | 68.2% | 65.3% | 0.00091 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
