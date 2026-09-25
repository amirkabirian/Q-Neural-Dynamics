# Q-Neural-Dynamics 🧠⚛️

[![License: All Rights Reserved](https://img.shields.io/badge/License-All%20Rights%20Reserved-red.svg)](LICENSE)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AmirKabirian/Q-Neural-Dynamics/blob/main/notebooks/main.ipynb)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&to&logo=PyTorch&logoColor=white)](https://pytorch.org/)

## 🔬 Scientific Background & Core Hypothesis
Biological and neural time-series data (such as LFP, EEG, or non-linear molecular dynamics) are notoriously plagued by high levels of noise, non-stationarity, and complex high-dimensional temporal interactions. Traditional recurrent neural networks (RNNs) often suffer from vanishing/exploding gradients and high computational overhead when modeling these systems.

**Q-Neural-Dynamics** bridges **Quantum-Inspired Computing** with **Computational Neuroscience and Biology** by introducing a *Quantum-Inspired Orthogonal Reservoir Computing (QIRC)* architecture. Instead of relying on noisy, unscalable NISQ-era quantum hardware, this framework utilizes **energy-preserving orthogonal transformations** (inspired by quantum unitary operators via QR decomposition) to project complex biological time-series into high-dimensional Hilbert-equivalent feature spaces on standard CPU infrastructure.

---

## 🛠️ Mathematical Framework
1. **Quantum-Inspired State Transformation:** 
   The input weights ($W_{in}$) and recurrent transition weights ($W_{rec}$) are initialized using orthogonal matrices derived via QR decomposition, ensuring norm-preserving (unitary-like) dynamics that prevent chaotic blow-ups:
   $$W, R = \text{qr}(\mathcal{N}(0, 1))$$
2. **Non-linear Phase Activation:**
   Simulating quantum phase interference through trigonometric non-linearities:
   $$h(t) = \tanh(W_{in} x(t) + W_{rec} h(t-1))$$

---

## 📂 Repository Structure
```text
Q-Neural-Dynamics/
│
├── notebooks/
│   └── main.ipynb          # End-to-end execution notebook (CPU-optimized)
├── requirements.txt        # Project dependencies
└── LICENSE                 # Proprietary License (All Rights Reserved)
