# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-28 at 00:00 UTC.  **Catalog checked:** 2026-11-28 05:06 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 33 | 75.00 | 79.0% | 77.7% | 75.0% |
| 7 days | 27 | 310.09 | 71.5% | 71.7% | 80.0% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 53.1% | 15.8% | 75.8% | 0.00470 |
| 1d | M5+ | 99.7% | 14.9% | 11.9% | 57.3% | 0.00164 |
| 1d | M6+ | 100.0% | 6.2% | 50.0% | 53.1% | 0.00018 |
| 7d | M4.5+ | 94.4% | 80.3% | 29.8% | 87.6% | 0.01696 |
| 7d | M5+ | 97.3% | 55.7% | 20.3% | 76.7% | 0.00850 |
| 7d | M6+ | 99.9% | 18.8% | 45.5% | 59.4% | 0.00105 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
