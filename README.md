# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-17 at 00:00 UTC.  **Catalog checked:** 2026-11-17 05:21 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 22 | 72.92 | 80.3% | 84.4% | 90.0% |
| 7 days | 16 | 289.95 | 72.8% | 80.8% | 89.4% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 53.2% | 15.8% | 75.8% | 0.00467 |
| 1d | M5+ | 99.7% | 20.8% | 15.7% | 60.3% | 0.00155 |
| 1d | M6+ | 100.0% | 10.0% | 50.0% | 55.0% | 0.00016 |
| 7d | M4.5+ | 94.5% | 82.9% | 28.8% | 88.8% | 0.01637 |
| 7d | M5+ | 97.3% | 57.5% | 19.0% | 77.6% | 0.00755 |
| 7d | M6+ | 99.9% | 31.9% | 75.0% | 66.0% | 0.00097 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
