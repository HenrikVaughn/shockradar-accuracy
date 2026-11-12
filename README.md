# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-12 at 00:00 UTC.  **Catalog checked:** 2026-11-12 04:29 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 17 | 70.22 | 82.6% | 90.3% | 90.0% |
| 7 days | 11 | 275.54 | 76.7% | 83.3% | 87.2% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 53.4% | 15.1% | 76.0% | 0.00449 |
| 1d | M5+ | 99.7% | 22.2% | 16.5% | 61.0% | 0.00148 |
| 1d | M6+ | 100.0% | 10.0% | 50.0% | 55.0% | 0.00021 |
| 7d | M4.5+ | 94.5% | 86.3% | 27.5% | 90.5% | 0.01539 |
| 7d | M5+ | 97.3% | 55.9% | 18.3% | 76.8% | 0.00737 |
| 7d | M6+ | 99.9% | 25.6% | 66.7% | 62.8% | 0.00116 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
