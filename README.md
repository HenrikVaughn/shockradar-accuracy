# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-20 at 00:00 UTC.  **Catalog checked:** 2026-11-20 04:30 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 25 | 74.86 | 79.4% | 80.9% | 83.3% |
| 7 days | 19 | 294.35 | 72.6% | 78.3% | 88.2% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 52.6% | 15.9% | 75.6% | 0.00476 |
| 1d | M5+ | 99.7% | 18.3% | 14.7% | 59.0% | 0.00165 |
| 1d | M6+ | 100.0% | 8.3% | 50.0% | 54.2% | 0.00018 |
| 7d | M4.5+ | 94.5% | 82.1% | 29.6% | 88.5% | 0.01654 |
| 7d | M5+ | 97.3% | 57.3% | 20.1% | 77.5% | 0.00785 |
| 7d | M6+ | 99.9% | 29.4% | 65.2% | 64.7% | 0.00090 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
