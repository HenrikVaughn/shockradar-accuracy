# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-02 at 00:00 UTC.  **Catalog checked:** 2026-11-02 02:52 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 7 | 77.07 | 84.0% | 92.1% | 83.3% |
| 7 days | 1 | 309.84 | 74.2% | 86.2% | 80.0% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 57.4% | 16.6% | 78.0% | 0.00446 |
| 1d | M5+ | 99.7% | 26.3% | 22.7% | 63.1% | 0.00180 |
| 1d | M6+ | 100.0% | 16.7% | 50.0% | 58.3% | 0.00030 |
| 7d | M4.5+ | 94.5% | 85.5% | 28.3% | 90.1% | 0.01696 |
| 7d | M5+ | 97.4% | 58.6% | 23.3% | 78.2% | 0.00811 |
| 7d | M6+ | 99.8% | 20.0% | 100.0% | 60.0% | 0.00155 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
