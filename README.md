# LFAT: Deepfake Detection using Frequency-Aware Lightweight Transformer

## Overview
This repository presents the implementation of **LFAT (Frequency-Aware Lightweight Transformer)**, a deepfake detection framework designed to achieve strong generalization and computational efficiency. The model integrates frequency-domain representations with a lightweight attention-based architecture to overcome the limitations of conventional CNN-based deepfake detectors.

The primary objective of this project is to develop a robust and efficient deepfake detection system suitable for real-world deployment scenarios.

---

## Motivation
Recent advancements in generative models have enabled the creation of highly realistic deepfake media, making traditional visual artifact-based detection approaches increasingly unreliable. Conventional CNN-based methods often overfit spatial features and fail to generalize across datasets.

This project addresses these challenges by:
- Leveraging frequency-domain information to capture manipulation artifacts that are less sensitive to visual appearance.
- Employing a lightweight transformer-based attention mechanism to enhance discriminative feature learning.
- Balancing detection accuracy with computational efficiency.

---

## Methodology
The LFAT framework consists of the following key components:

### Frequency-Domain Feature Extraction
Input facial frames are transformed into the frequency domain to highlight manipulation traces that are not easily observable in the spatial domain.

### Lightweight CNN Backbone
A MobileNet-based backbone is used for efficient spatial feature extraction while maintaining low computational overhead.

### Attention / Transformer Module
An attention-based transformer encoder refines extracted features by modeling long-range dependencies and improving robustness against overfitting.

### Binary Classification Head
The refined feature representations are used to classify inputs as either real or fake.

---

## Datasets
The model has been evaluated on widely used deepfake benchmarks, including:
- Celeb-DF
- DFDC (subset)
- FaceForensics++

Due to dataset licensing restrictions and size constraints, datasets are not included in this repository.

---

## Evaluation Metrics
The performance of the proposed method is evaluated using the following metrics:
- Accuracy
- Precision
- Recall
- F1-score
- AUC-ROC
- Inference latency

These metrics are chosen to assess both detection effectiveness and practical deployability.

---

## Results
Experimental results demonstrate that LFAT achieves improved cross-dataset generalization compared to baseline CNN-based models, while maintaining lightweight inference suitable for resource-constrained environments.

Quantitative comparisons, ROC curves, and performance plots are provided in the `assets/` and `results/` directories.

---

## Project Structure
LFAT-Deepfake-Detection/
│
├── notebooks/
│ └── lfat_training_evaluation.ipynb
│
├── models/
│ └── lfat_best_model.h5
│
├── results/
│ ├── metrics.txt
│ └── evaluation_plots/
│
├── assets/
│ ├── lfat_architecture.png
│ ├── model_comparison.png
│ ├── model_size_comparison.png
│ ├── roc_combined.png
│ └── f1_comparison.png
│
├── requirements.txt
└── README.md

---

## How to Run

### Install dependencies
```bash

pip install -r requirements.txt

Run training and evaluation
Open the Jupyter notebook:
notebooks/lfat_training_evaluation.ipynb
Ensure that the required datasets are correctly configured before execution.

Limitations

Temporal video-level modeling is not included.

Performance depends on dataset quality and preprocessing.

The system is not intended for forensic or legal decision-making without human verification.

Related Publication

This project is associated with the manuscript:

“Deepfake Detection using Frequency-Aware Lightweight Transformer (LFAT) Model”

Submitted to peer-reviewed journals (Springer / Elsevier).
The manuscript is currently under review.

Future Work

Integration of temporal modeling for video-level detection.

Explainable AI techniques for improved interpretability.

Multimodal fusion using audio-visual cues.

Robustness analysis against adversarial attacks.

Author

Adhiswauran V
B.Tech (Computer Science / Artificial Intelligence)
