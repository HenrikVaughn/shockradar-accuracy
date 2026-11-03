# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-03 at 00:00 UTC.  **Catalog checked:** 2026-11-03 04:09 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 8 | 74.78 | 84.3% | 92.7% | 85.7% |
| 7 days | 2 | 300.69 | 75.4% | 87.7% | 77.8% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 57.8% | 15.9% | 78.2% | 0.00426 |
| 1d | M5+ | 99.7% | 29.3% | 24.0% | 64.5% | 0.00168 |
| 1d | M6+ | 100.0% | 14.3% | 50.0% | 57.1% | 0.00031 |
| 7d | M4.5+ | 94.4% | 85.2% | 27.8% | 90.0% | 0.01647 |
| 7d | M5+ | 97.3% | 57.9% | 22.4% | 77.8% | 0.00783 |
| 7d | M6+ | 99.9% | 22.2% | 100.0% | 61.1% | 0.00139 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
