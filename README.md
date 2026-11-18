# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-18 at 00:00 UTC.  **Catalog checked:** 2026-11-18 04:49 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 23 | 73.09 | 80.5% | 84.0% | 90.9% |
| 7 days | 17 | 292.64 | 72.6% | 80.0% | 89.6% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 52.4% | 15.6% | 75.5% | 0.00470 |
| 1d | M5+ | 99.7% | 21.0% | 15.8% | 60.4% | 0.00155 |
| 1d | M6+ | 100.0% | 9.1% | 50.0% | 54.5% | 0.00017 |
| 7d | M4.5+ | 94.5% | 82.3% | 29.2% | 88.6% | 0.01647 |
| 7d | M5+ | 97.3% | 57.5% | 19.3% | 77.6% | 0.00765 |
| 7d | M6+ | 99.9% | 31.2% | 71.4% | 65.6% | 0.00093 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
