# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-08 at 00:00 UTC.  **Catalog checked:** 2026-11-08 02:50 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 13 | 69.57 | 84.8% | 89.3% | 88.9% |
| 7 days | 7 | 284.68 | 78.4% | 84.5% | 82.1% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 53.8% | 14.2% | 76.1% | 0.00431 |
| 1d | M5+ | 99.7% | 25.0% | 18.4% | 62.4% | 0.00149 |
| 1d | M6+ | 100.0% | 11.1% | 50.0% | 55.6% | 0.00025 |
| 7d | M4.5+ | 94.5% | 86.8% | 27.7% | 90.7% | 0.01516 |
| 7d | M5+ | 97.2% | 54.0% | 19.6% | 75.9% | 0.00793 |
| 7d | M6+ | 99.9% | 25.0% | 63.6% | 62.5% | 0.00129 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
