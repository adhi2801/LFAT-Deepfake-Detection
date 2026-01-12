# LFAT: Deepfake Detection using Frequency-Aware Lightweight Transformer

## Overview
This repository contains the implementation of **LFAT (Frequency-Aware Lightweight Transformer)**, a deepfake detection framework designed to improve robustness and generalization across diverse deepfake datasets. The approach integrates frequency-domain representations with a lightweight attention-based architecture to overcome the limitations of conventional CNN-based detectors.

The primary goal of this project is to build a computationally efficient and generalizable deepfake detection system suitable for real-world deployment scenarios.

---

## Motivation
Recent advances in generative models have led to highly realistic deepfakes, making visual artifact-based detection increasingly unreliable. Traditional CNN-based approaches often overfit spatial features and fail to generalize across datasets.

This project addresses these challenges by:
- Leveraging frequency-domain information to capture manipulation artifacts that are less sensitive to visual variations.
- Employing a lightweight transformer-based attention mechanism to enhance discriminative feature learning.
- Balancing detection performance with computational efficiency.

---

## Methodology
The LFAT framework consists of the following key components:

1. **Frequency-Domain Feature Extraction**  
   Input facial frames are transformed into the frequency domain to highlight manipulation traces that are not easily observable in the spatial domain.

2. **Lightweight CNN Backbone**  
   A MobileNet-based backbone is used for efficient spatial feature extraction while maintaining low computational overhead.

3. **Attention / Transformer Module**  
   An attention mechanism refines extracted features by modeling long-range dependencies and improving robustness against overfitting.

4. **Binary Classification Head**  
   The refined feature representation is used to classify inputs as real or fake.

---

## Datasets
The model has been evaluated on widely used deepfake benchmarks, including:
- Celeb-DF
- DFDC (subset)
- FaceForensics++

Due to dataset licensing and size constraints, datasets are not included in this repository.

---

## Evaluation Metrics
The performance of the proposed method is evaluated using:
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

Detailed quantitative results and evaluation plots are provided in the project report.

---

## Project Structure
LFAT-Deepfake-Detection/
│
├── notebooks/
│   └── lfat_training_evaluation.ipynb
│
├── models/
│   ├── lfat_best_model.h5
│   └── README.md
│
├── results/
│   ├── metrics.txt
│   └── evaluation_plots/
│
├── assets/
│   └── lfat_architecture.png
│
├── requirements.txt
└── README.md

---

## How to Run
1. Install dependencies:

pip install -r requirements.txt

2. Open the training and evaluation notebook:

notebooks/lfat_training_evaluation.ipynb

Ensure that the required datasets are properly configured before execution.

---

## Limitations
- Temporal video-level modeling is not included
- Performance depends on dataset quality and preprocessing
- The system is not intended for forensic or legal decision-making without human verification

---

## Related Publication
This project is associated with the manuscript:

**“Deepfake Detection using Frequency-Aware Lightweight Transformer (LFAT) Model”**

Submitted to peer-reviewed journals (Springer / Elsevier).  
The manuscript is currently under review.

---

## Future Work
- Integration of temporal modeling for video-level detection
- Explainable AI techniques for improved interpretability
- Multimodal fusion using audio-visual cues
- Robustness analysis against adversarial attacks

---

## Author
**Adhiswauran V**  
B.Tech (Computer Science / Artificial Intelligence)

