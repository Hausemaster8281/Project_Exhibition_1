# Blood Cancer Detection & Classification (Explainable AI)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white)](https://pytorch.org/)

## Project Overview
[cite_start]This repository contains a comprehensive deep learning pipeline designed to detect and classify various types of blood cancer from microscopic cell imagery[cite: 25, 28]. [cite_start]Beyond just raw classification, this project integrates **Explainable AI (XAI)** techniques to provide visual justifications for model predictions, making it a viable tool for clinical decision support[cite: 25, 30].

## Key Features
* [cite_start]**Multi-Model Benchmarking:** Implemented and compared several SOTA architectures including **VGG16, VGG19, ResNet50, and DenseNet-121**[cite: 26, 29].
* [cite_start]**High Precision:** Achieved a peak testing accuracy of **96%** using a fine-tuned VGG16 backbone[cite: 29].
* [cite_start]**Visual Interpretability:** Integrated **Grad-CAM** (Gradient-weighted Class Activation Mapping) to highlight the specific regions of a cell that influenced the model's classification[cite: 26, 30].
* [cite_start]**Robust Evaluation:** Benchmarked performance using precision, recall, and F1-score to ensure reliability in medical contexts[cite: 30].

## Tech Stack
* [cite_start]**Deep Learning:** PyTorch[cite: 26].
* [cite_start]**Architectures:** VGG16, VGG19, ResNet50, DenseNet-121[cite: 26].
* [cite_start]**Explainability:** Grad-CAM[cite: 26].
* [cite_start]**Machine Learning:** XGBoost[cite: 26].
* [cite_start]**Languages:** Python[cite: 26].

## Performance Summary
[cite_start]The models were trained on a massive dataset of **25,000 images**[cite: 28]. Through transfer learning, the following results were achieved:

| Model | Accuracy | Status |
| :--- | :--- | :--- |
| **VGG16** | **96%** | [cite_start]Peak Performance [cite: 29] |
| **ResNet50** | Benchmarked | [cite_start]Supported [cite: 26] |
| **DenseNet-121** | Benchmarked | [cite_start]Supported [cite: 26] |

## 🔬 Explainable AI (XAI) Implementation
In medical diagnostics, "Black Box" models are difficult to trust. [cite_start]This project solves this by using **Grad-CAM** to generate heatmaps on the original input images, providing visual explainability of CNN predictions[cite: 25, 30].

## 📂 Repository Structure
```text
├── data/               # Dataset directory (25,000 images)
├── notebooks/          # Training and Grad-CAM visualization notebooks
├── models/             # Saved model weights (.pth)
├── src/
│   ├── preprocess.py   # Image augmentation and normalization
│   ├── train.py        # Model training and transfer learning script
│   └── explain.py      # Grad-CAM heatmap generation
└── requirements.txt    # Project dependencies
