# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-21 at 00:00 UTC.  **Catalog checked:** 2026-11-21 04:24 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 26 | 75.38 | 79.3% | 80.0% | 83.3% |
| 7 days | 20 | 297.29 | 72.6% | 77.0% | 86.8% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 52.1% | 15.7% | 75.3% | 0.00477 |
| 1d | M5+ | 99.7% | 17.5% | 14.2% | 58.7% | 0.00166 |
| 1d | M6+ | 100.0% | 8.3% | 50.0% | 54.2% | 0.00017 |
| 7d | M4.5+ | 94.5% | 82.0% | 29.8% | 88.4% | 0.01658 |
| 7d | M5+ | 97.3% | 56.9% | 20.2% | 77.3% | 0.00803 |
| 7d | M6+ | 99.9% | 28.3% | 62.5% | 64.1% | 0.00089 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
