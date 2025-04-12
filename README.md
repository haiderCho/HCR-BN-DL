<h1 align="center"> Comparative Analysis of CNN and RNN Architectures for Bangla Handwritten Character Recognition </h1>
<!-- <p align="center">
 <img alt="Languages" src="https://img.shields.io/github/languages/count/haiderCho/">
 <img alt="Repository size" src="https://img.shields.io/github/repo-size/haiderCho/">
 <img alt="Contributors" src="https://img.shields.io/github/contributors/haiderCho/">
 <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/haiderCho/">
</p> -->

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)


## 🔍 Overview

Bangla is the 5th most spoken language globally, yet the field of Bangla Handwritten Character Recognition (HCR) remains underexplored. This project presents a comparative study of two deep learning architectures — Convolutional Neural Networks (CNN) and Bidirectional Long Short-Term Memory (BLSTM) — specifically designed to recognize Bangla handwritten characters.

## 🎯 Objectives

- Evaluate the performance of CNN vs. RNN for Bangla HCR.
- Understand architectural strengths in handling script complexities like modifiers, compound characters, and cursive writing.
- Propose enhancements for future OCR systems using hybrid models or transformers.

## 🧠 Key Contributions

- Implemented CNN and BLSTM architectures using Keras.
- Achieved **97% accuracy** with CNN and **87% accuracy** with BLSTM.
- Analyzed misclassification patterns via confusion matrices.
- Proposed future directions including hybrid CNN-RNN and Vision Transformers.

## 🧱 Model Architectures

### CNN (Convolutional Neural Network)
- 3 Convolutional Blocks: 64 → 128 → 256 filters
- Kernel Size: (3x3), Activation: ReLU
- MaxPooling & Dropout for regularization
- Dense Layers: 128 → Softmax output (50 classes)

### BLSTM (Bidirectional LSTM)
- Input reshaped as (28, 28) sequences
- 2 BLSTM Layers (128 units each)
- Dropout and Fully Connected Dense Layer
- Output: Softmax over 50 classes

## 📊 Dataset

- **Name:** [BanglaLekha-Isolated](https://doi.org/10.1016/j.dib.2017.03.035)
- **Total Samples:** ~166,105 handwritten images
- **Classes:** 84 (numerals, vowels, consonants, compound characters)
- **Used Samples:** 15,000
- **Image Format:** Grayscale, 28x28 pixels

## ⚙️ Training Details

- Optimizer: Adam
- Loss: Categorical Cross-Entropy
- Epochs: Max 100 (EarlyStopping used)
- Batch Size: 32
- Augmentations: Rotation, scaling, flipping, zoom

## 📈 Results

| Metric         | CNN  | RNN (BLSTM) |
|----------------|------|-------------|
| Accuracy       | 97%  | 87%         |
| Execution Time | Fast | Slower      |

- CNN outperformed RNN in spatial recognition, generalization, and efficiency.
- RNN showed strength in cursive and sequential strokes but suffered from higher computational cost.

## 🔮 Future Work

- Explore **Hybrid CNN-RNN** architectures.
- Integrate **Vision Transformers** for enhanced global spatial understanding.
- Develop **real-time OCR** solutions for mobile/edge devices.
- Expand dataset with more compound characters and writer diversity.
