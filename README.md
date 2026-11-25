# Shockradar — public earthquake forecast accuracy

**Live forecasts:** https://shockradar.pages.dev/  
**Method:** Completed 1-day and 7-day worldwide gridded earthquake forecast windows, scored only after an extra 24-hour USGS reporting buffer.  
**Caution:** Experimental research forecasts, not earthquake warnings or public safety advice. Daily forecast issues overlap and should not be treated as independent tests.

<!-- SHOCKRADAR_ACCURACY_START -->
## Live forecast accuracy (automatically updated)
**Latest generated forecast:** 2026-11-25 at 00:00 UTC.  **Catalog checked:** 2026-11-25 05:46 UTC.

**Only finished windows are scored.** Each forecast is archived unchanged before evaluation; scores use the current USGS M4.5+ catalog after an extra 24-hour reporting buffer.

| Horizon | Scored issues | Poisson NLL / issue ↓ | Top 5% M4.5+ hit rate | Top 5% M5+ hit rate | Top 5% M6+ hit rate |
| :-- | --: | --: | --: | --: | --: |
| 1 day | 30 | 76.56 | 78.9% | 77.9% | 73.3% |
| 7 days | 24 | 309.70 | 72.2% | 72.5% | 82.1% |

**Probability-based accuracy at a fixed 10% threshold** (cumulative across all scored cells):

| Horizon | Magnitude | Accuracy* | Recall | Precision | Balanced accuracy | Brier ↓ |
| :-- | :-- | --: | --: | --: | --: | --: |
| 1d | M4.5+ | 98.3% | 52.5% | 15.8% | 75.5% | 0.00477 |
| 1d | M5+ | 99.7% | 16.9% | 13.6% | 58.4% | 0.00164 |
| 1d | M6+ | 100.0% | 6.7% | 50.0% | 53.3% | 0.00019 |
| 7d | M4.5+ | 94.5% | 81.2% | 30.2% | 88.0% | 0.01686 |
| 7d | M5+ | 97.3% | 55.9% | 20.4% | 76.8% | 0.00846 |
| 7d | M6+ | 99.9% | 22.4% | 50.0% | 61.2% | 0.00097 |

Event counts before publication are shown in DAILY.md. Publication can lag the nominal 00:00 issue cutoff. This is not an earthquake warning service.

Detailed per-issue results: [`accuracy/DAILY.md`](accuracy/DAILY.md) · Machine-readable: [`accuracy/history.csv`](accuracy/history.csv)
<!-- SHOCKRADAR_ACCURACY_END -->
