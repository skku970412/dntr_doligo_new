# AITOD Subset-50 (final50 tag)

- **Run Command**: `source venv/bin/activate && cd DNTR/mmdet-dntr && ./run.sh subset --limit 50 --tag final50`
- **Log**: `DNTR/mmdet-dntr/logs/20251110_054006_subset50_final50/run.log`
- **Results Pickle**: `DNTR/mmdet-dntr/logs/20251110_054006_subset50_final50/results.pkl`
- **LRP**: Enabled (cocoapi-aitod)

## Detection Metrics

| Metric | Value |
| --- | --- |
| mAP (0.50:0.95) | 0.289 |
| mAP@0.50 | 0.539 |
| mAP@0.75 | 0.229 |
| mAP_vt | 0.283 |
| mAP_t | 0.366 |
| mAP_s | 0.548 |
| mAP_m | 0.209 |

## Recall Metrics

| Metric | Value |
| --- | --- |
| AR@100 | 0.338 |
| AR@300 | 0.356 |
| AR@1500 | 0.357 |
| AR_vt@1500 | 0.334 |
| AR_t@1500 | 0.459 |
| AR_s@1500 | 0.571 |
| AR_m@1500 | 0.215 |

## LRP Metrics

| Metric | Value |
| --- | --- |
| oLRP | 0.710 |
| oLRP_Localisation | 0.214 |
| oLRP_false_positive | 0.140 |
| oLRP_false_negative | 0.443 |

