# Cross-Model Generalization and Domain Shift in Video Deepfake Detection

## Overview

This repository contains the implementation and experimental analysis for evaluating the cross-model generalization capability of a video deepfake detection model. The objective is to study how well a detector trained on one dataset performs when tested on different datasets and under various domain shift conditions.

The experiments use an EfficientNet-B4 + BiLSTM architecture trained on the Celeb-DF v2 dataset and evaluated on unseen datasets to assess robustness against changes in manipulation techniques, video quality, and recording conditions.

---

## Objectives

- Evaluate cross-model generalization across different deepfake datasets.
- Study the effect of domain shift on detection performance.
- Analyze robustness under common real-world image degradations.
- Investigate methods to improve generalization across unseen domains.

---

## Repository Contents

```
Cross-model-generalization/
│
├── cross model 1.ipynb
├── cross model 2.ipynb
└── README.md
```

### Notebook Descriptions

### 1. cross model 1.ipynb

This notebook evaluates cross-model generalization using:

- Training Dataset: Celeb-DF v2
- Testing Dataset: FaceForensics++ (NeuralTextures)

The notebook includes:

- Cross-dataset evaluation
- Domain shift experiments
- JPEG compression analysis
- Gaussian blur analysis
- Image downscaling analysis
- Brightness variation analysis
- Robustness evaluation using augmentation-based fine-tuning
- Performance comparison and visualization

---

### 2. cross model 2.ipynb

This notebook evaluates the same trained model on the DFDC dataset.

The notebook includes:

- Cross-dataset evaluation on DFDC
- Classification report
- Confusion matrix
- ROC curve
- Domain shift experiments
- JPEG compression analysis
- Gaussian blur analysis
- Downscaling analysis
- Brightness variation analysis
- Test-Time Augmentation (TTA) robustness evaluation
- Performance visualization

---

## Model Architecture

The proposed detector consists of:

- EfficientNet-B4 for spatial feature extraction
- Bidirectional LSTM for temporal sequence modeling
- Fully connected classification layers
- Binary classification using BCEWithLogitsLoss

---

## Cross-Model Evaluation

### Model 1

Training Dataset

- Celeb-DF v2

Testing Dataset

- FaceForensics++ (NeuralTextures)

Objective

Evaluate whether a detector trained on Celeb-DF v2 can detect deepfakes generated using unseen manipulation techniques.

---

### Model 2

Training Dataset

- Celeb-DF v2

Testing Dataset

- DFDC

Objective

Evaluate detector performance on a large-scale real-world benchmark containing diverse identities, recording conditions, and manipulation methods.

---

## Domain Shift Experiments

The following degradation types were applied to evaluate detector robustness:

- JPEG Compression
- Gaussian Blur
- Image Downscaling
- Brightness Variation

These experiments simulate practical deployment scenarios such as:

- Social media compression
- Camera blur
- Low-resolution videos
- Illumination changes

---

## Robustness Strategies

### Model 1

- Augmentation-based fine-tuning
- Domain adaptation using degraded samples

### Model 2

- Test-Time Augmentation (TTA)
- Prediction averaging during inference

---

## Technologies Used

- Python
- PyTorch
- EfficientNet-B4
- BiLSTM
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## Evaluation Metrics

The experiments report:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- MCC
- Confusion Matrix
- ROC Curve

---

## Key Findings

- The proposed detector achieves strong performance on the training dataset.
- Cross-dataset performance decreases due to domain shift.
- JPEG compression has the largest impact on detection performance.
- Brightness variation has comparatively little effect.
- Domain adaptation remains an important challenge for practical deepfake detection systems.

---

## Future Work

Future improvements may include:

- Multi-dataset training
- Domain-adversarial learning
- Self-supervised pretraining
- Transformer-based temporal modeling
- Larger-scale cross-dataset benchmarking

---

## Author

**Varsha V P**

Bachelor of Technology (Computer Science and Engineering)

Research Area:
Deepfake Detection • Synthetic Media • Computer Vision • Deep Learning
