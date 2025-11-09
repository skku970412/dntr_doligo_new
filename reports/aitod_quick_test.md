# AITOD Quick Smoke Test (AI-TODv1_map_27.2.pth)

- **Date**: 2025-11-10 04:38:12 
- **Env**: python3.10 venv at `~/llama_young/dntr_new/venv` with PyTorch 1.11.0+cu113, mmcv-full 1.6.0, mmdet 2.24.1
- **Data root**: `~/llama_young/dntr_new/DNTR/mmdet-dntr/data/aitod`
- **Checkpoint**: `work_dirs/aitod_DNTR_mask/AI-TODv1_map_27.2.pth`
- **Subset used**: `annotations/aitod_test_v1_1.0_first10.json` (10 test images) to validate the pipeline before full test run.

## Command

```bash
source ~/llama_young/dntr_new/venv/bin/activate
cd ~/llama_young/dntr_new/DNTR/mmdet-dntr
CUDA_VISIBLE_DEVICES=0 python tools/test.py   configs/aitod-dntr/aitod_DNTR_mask.py   work_dirs/aitod_DNTR_mask/AI-TODv1_map_27.2.pth   --cfg-options     data.test.ann_file=data/aitod/annotations/aitod_test_v1_1.0_first10.json     data.test.img_prefix=data/aitod/images/test/     data.samples_per_gpu=1     data.workers_per_gpu=2   --eval bbox   --eval-options with_lrp=False classwise=False classwise_lrp=False metric_items="['mAP']"   --out work_dirs/aitod_DNTR_mask/quick_first10.pkl
```

## Result (10-image subset)

| Metric | Value |
|--------|-------|
| bbox_mAP | 0.405 |
| bbox_mAP_copypaste | `0.405 0.603 0.436 0.547 0.275 -1.000` |

- Raw detections were serialized to `work_dirs/aitod_DNTR_mask/quick_first10.pkl`.
- LRP metrics were skipped because the standard COCO API was used (custom `aitodpycocotools` not present).

## Next Steps
1. For the full AITOD test evaluation, remove the `_first10` override and rerun the same command without `--cfg-options data.test.ann_file=...first10.json`.
2. To export visual examples, rerun with `--show-dir work_dirs/aitod_DNTR_mask/full_test_vis` once the tensor-to-image issue is resolved (keep `samples_per_gpu=1`).
3. Optional: build and install `cocoapi-aitod` to enable custom LRP metrics if those scores are required.
