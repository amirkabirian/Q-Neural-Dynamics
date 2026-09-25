# Q-Neural-Dynamics: Quantum-Inspired Neural Framework

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amirkabirian/Q-Neural-Dynamics/blob/main/main.ipynb)
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-CPU-orange.svg)
![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red.svg)

## Overview
**Q-Neural-Dynamics** is a lightweight, CPU-optimized computational framework designed for advanced biological and neural time-series analysis. By bridging principles from quantum mechanics and recurrent neural dynamics, this project introduces a **Quantum-Inspired Orthogonal Reservoir** to process sequential data with high stability and computational efficiency.

---

## Core Scientific Principles
1. **Unitary-Inspired Dynamics:** Standard recurrent neural networks often suffer from gradient instability over long sequences. This framework utilizes **QR Decomposition** on raw weight matrices to construct strictly orthogonal recurrent and input projections ($W_{in}, W_{rec}$), mimicking unitary operators found in quantum mechanics.
2. **Fixed Reservoir Computing:** The recurrent reservoir weights are frozen during training (`requires_grad=False`), drastically reducing training overhead while leveraging rich nonlinear fading-memory dynamics through the $\tanh$ activation function.
3. **Robust Sequence Pooling:** Temporal states extracted from the reservoir pass through a global temporal average pooling layer followed by a feed-forward classifier to yield precise binary classifications.

---

## Key Features
* **Zero External Hardware Conflicts:** Fully optimized for stable execution on standard CPU environments using native PyTorch and NumPy.
* **End-to-End Pipeline:** Includes automated data standardization, sliding-window sequence generation, training loops with cross-entropy loss tracking, and advanced clinical/performance metric evaluations (Accuracy, Precision, Recall, and F1-Score).
* **Built-in Visualization:** Generates clean optimization trajectory and training convergence curves.

---

## Performance & Evaluation Metrics
The pipeline natively computes essential classification metrics:
* **Test Accuracy**
* **Precision & Recall (Sensitivity)**
* **F1-Score**

---

## Requirements
To run this project locally, ensure you have the following packages installed:
```text
torch>=2.0.0
numpy>=1.20.0
pandas>=1.3.0
matplotlib>=3.4.0
