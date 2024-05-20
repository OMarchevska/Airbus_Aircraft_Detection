# Airbus Aircraft Detection

This repository contains a set of notebooks dedicated to solving the object detection problem using the Airbus Aircraft sample dataset, available on the Kaggle platform. Both the data preparation and model training processes are conducted using Kaggle platform resources.

## Notebooks Overview

The data preparation process is consistent across all notebooks, with variations in the models used for training and inference. The specifics are as follows:

1. **retina-airbus.ipynb**:
   - Utilizes KerasCV for data manipulation and model training.
   - Model: RetinaNet with a ResNet50 backbone pretrained on the Pascal VOC dataset.

2. **yolo-airbus.ipynb**:
   - Involves bounding boxes transformation and a different training data setup.
   - Model: YOLOv8s (small) from the Ultralytics package.

## Results

Both models were trained on the same data and tested on two unlabeled full-size images. Below is a comparison of their performance:

- **RetinaNet**:
  - Pros: High confidence in predictions.
  - Cons: Slower inference speed.
  - Metrics:
    - mAP: 0.6686
    - mAP@[IoU=50]: 0.9445

- **YOLOv8s**:
  - Pros: Lightning-fast predictions.
  - Cons: Slightly lower confidence in predictions.
  - Metrics:
    - mAP: 0.75985
    - mAP@[IoU=50]: 0.987