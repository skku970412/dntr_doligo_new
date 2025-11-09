# AITOD Subset-50 Test (LRP Enabled)

- **Date**: 2025-11-10 04:59:17 KST
- **Command**: `./run.sh subset --limit 50 --tag aitod`
- **Checkpoint**: `work_dirs/aitod_DNTR_mask/AI-TODv1_map_27.2.pth`
- **Annotation**: `data/aitod/annotations/subsets/aitod_test_v1_1.0_first50.json`
- **Log**: `DNTR/mmdet-dntr/logs/20251110_045708_subset50_aitod/run.log`
- **LRP Metrics**: Enabled (cocoapi-aitod)

## Detection Metrics

| Metric | Value |
|--------|-------|
| mAP (0.50:0.95) | 0.287 |
| mAP@0.50 | 0.539 |
| mAP@0.75 | 0.224 |
| mAP_vt | 0.286 |
| mAP_t | 0.360 |
| mAP_s | 0.557 |
| mAP_m | 0.197 |

## Recall Metrics

| Metric | Value |
|--------|-------|
| AR@100 | 0.341 |
| AR@300 | 0.359 |
| AR@1500 | 0.360 |
| AR_vt@1500 | 0.334 |
| AR_t@1500 | 0.463 |
| AR_s@1500 | 0.580 |
| AR_m@1500 | 0.205 |

## LRP Metrics

| Metric | Value |
|--------|-------|
| oLRP | 0.710 |
| oLRP_Localisation | 0.214 |
| oLRP_false_positive | 0.143 |
| oLRP_false_negative | 0.442 |

> Raw detections saved to `logs/20251110_045708_subset50_aitod/results.pkl`. To run on the full test set, call `./run.sh full --tag <name>` (LRP on by default).
