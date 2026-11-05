# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-05 at 00:00 UTC.  **Catalog checked:** 2026-11-05 03:51 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 10 | 73.82 | 85.5% | 92.0% | 85.7% |
| 7 days | 4 | 297.13 | 77.4% | 87.4% | 76.5% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 55.7% | 15.7% | 77.1% | 0.00444 |
| 1d | M5+ | 99.7% | 24.0% | 19.7% | 61.9% | 0.00170 |
| 1d | M6+ | 100.0% | 14.3% | 50.0% | 57.1% | 0.00025 |
| 7d | M4.5+ | 94.5% | 86.7% | 28.7% | 90.7% | 0.01575 |
| 7d | M5+ | 97.3% | 55.5% | 22.6% | 76.6% | 0.00832 |
| 7d | M6+ | 99.9% | 23.5% | 100.0% | 61.8% | 0.00134 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
