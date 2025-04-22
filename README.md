# Fire / Smoke detection using YOLOv11

FSD is a well-known object detection task. To solve the problem we propose modern YOLOv11n (nano) version pre-trained on COCO dataset.

We aimed to measure mainly 3 metrics: precision, recall and mAP-50.

We aimed next numbers:
- precision (fire) ~ 0.7
- precision (smoke) ~ 0.8
- recall (fire) ~ 0.6
- recall (smoke) ~ 0.8
- mAP-50 (fire) ~ 0.6
- mAP-50 (smoke) ~ 0.8

However, we did not manage to attain such metric values so far and finally we have:
- precision (fire) ~ 0.62
- precision (smoke) ~ 0.63
- recall (fire) ~ 0.51
- recall (smoke) ~ 0.34
- mAP-50 (fire) ~ 0.55
- mAP-50 (smoke) ~ 0.38

The reason why we think we were not successful at attaining lower threshold for metrics is:
- imbalanced dataset (approximately twice less smoke detections in training set)
- small dataset size (we tries augmentations techniques but it did not help; we could not find a way to upsample using vendor library ultralytics)
- not enough computational resources (30 epochs is our maximum since more epochs leads to overheating of GPU)
