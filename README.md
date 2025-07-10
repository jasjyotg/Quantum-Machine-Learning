# Hybrid and Variational Quantum Models for MNIST Classification

This repository contains implementations of two quantum-enhanced models for digit classification on the MNIST dataset:

- **Hybrid Quantum Neural Network (HQNN)** using PyTorch and Qiskit/PennyLane
- **Variational Quantum Classifier (VQC)** using Qiskit

Both models explore the integration of classical machine learning with quantum computing for supervised learning tasks.

---

## Contents

### `Hybrid-QNN/`
- Hybrid Quantum-Classical Architecture combining classical fully connected layers with a Parameterized Quantum Circuit (PQC).
- Uses angle encoding to map classical features to quantum states.
- Trained end-to-end using PyTorch optimizers (e.g., COBYLA, Adam).
- Achieves high accuracy (up to 96% on MNIST with 20 qubits).

### `VQC-Qiskit/`
- Implements a Variational Quantum Classifier using Qiskit's `VQC` class.
- Reduces MNIST data to 2D via PCA, suitable for quantum input.
- Uses `ZFeatureMap` and `RealAmplitudes` circuits.
- Trained using Qiskit's built-in optimizers (COBYLA, Adam).
- Evaluated using the `StatevectorSimulator`.
