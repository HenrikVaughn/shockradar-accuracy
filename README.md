# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-26 at 00:00 UTC.  **Catalog checked:** 2026-11-26 05:36 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 31 | 75.90 | 79.1% | 77.9% | 75.0% |
| 7 days | 25 | 309.51 | 72.0% | 71.8% | 80.6% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 52.7% | 15.8% | 75.6% | 0.00476 |
| 1d | M5+ | 99.7% | 16.4% | 13.2% | 58.1% | 0.00164 |
| 1d | M6+ | 100.0% | 6.2% | 50.0% | 53.1% | 0.00019 |
| 7d | M4.5+ | 94.5% | 81.0% | 30.0% | 87.9% | 0.01679 |
| 7d | M5+ | 97.3% | 55.4% | 20.3% | 76.6% | 0.00850 |
| 7d | M6+ | 99.9% | 20.8% | 48.4% | 60.4% | 0.00101 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
