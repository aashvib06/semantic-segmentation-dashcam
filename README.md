# Semantic Segmentation for Autonomous Driving

## Overview
This project implements a pixel-level semantic segmentation pipeline for understanding road scenes in autonomous driving scenarios. Each pixel in a dashcam image is classified into semantic categories such as lanes, vehicles, pedestrians, and background, enabling fine-grained scene understanding beyond object detection.

The focus of this project is to understand semantic segmentation models from first principles rather than relying on pretrained pipelines.

---

## Key Concepts
- Convolutional Neural Networks (CNNs)
- Encoder–decoder architectures
- Skip connections and feature reuse
- Pixel-wise classification
- Loss functions and evaluation metrics

---

## Model Architecture
A U-Net–style encoder–decoder architecture is implemented:
- The encoder progressively downsamples the input to extract hierarchical features
- The decoder upsamples feature maps to recover spatial resolution
- Skip connections preserve spatial detail and improve boundary accuracy

---

## Training Pipeline
- Implemented custom training and evaluation loops in PyTorch
- Used pixel-wise loss functions suitable for dense prediction tasks
- Evaluated performance using metrics such as pixel accuracy and Intersection over Union (IoU)
- Analyzed the impact of class imbalance and input resolution on segmentation quality

---

## Dataset
- Dashcam images with pixel-level annotations
- Preprocessing included resizing, normalization, and label encoding

---

## Results & Observations
- Skip connections significantly improve boundary localization
- Model performance is sensitive to class imbalance
- There is a clear trade-off between model complexity and inference cost

---

## Technologies Used
- Python
- PyTorch
- NumPy, OpenCV, Matplotlib

---

## Motivation
This project was undertaken to build a deep understanding of semantic segmentation and dense prediction tasks, with applications in autonomous driving and scene understanding.

---

## Future Work
- Explore deeper encoder backbones
- Improve class imbalance handling
- Extend to real-time inference settings
