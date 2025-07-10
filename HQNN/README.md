# Hybrid Quantum Neural Network (HQNN) for MNIST Classification

This notebook implements a **Hybrid Quantum Neural Network (HQNN)** to perform digit classification on the MNIST dataset using a combination of classical neural network layers and quantum circuits. The hybrid architecture leverages the expressive power of parameterized quantum circuits alongside classical deep learning layers.

## What This Notebook Covers

### 1. Dataset Preparation
- Loads the **MNIST dataset** using `torchvision.datasets`.
- Converts image data to tensors and normalizes them.
- Filters the dataset to include only a binary subset (e.g., digits `0` and `1`) or selects a limited number of classes for demonstration.
- Batches and shuffles the data using PyTorch `DataLoader`.

### 2. Classical Neural Network Layers
- Defines the classical part of the hybrid model using PyTorch.
- Includes layers such as fully connected (dense) layers for preprocessing before quantum interaction.

### 3. Quantum Circuit Definition
- Constructs a parameterized quantum circuit (PQC) using Qiskit or PennyLane.
- Encodes classical features into quantum states via data encoding (angle encoding).
- Uses parameterized gates and measurements to allow training via gradient-based optimization.

### 4. Hybrid Model Construction
- Combines the classical and quantum components into a single model using PyTorch.
- Implements the forward pass such that classical features are passed to the quantum circuit and the result is returned to the classical layers.

### 5. Training
- Trains the hybrid model using binary or multiclass cross-entropy loss.
- Optimizes both quantum and classical parameters using an the COPYBLA optimizer.
- Tracks loss and accuracy over epochs.

### 6. Evaluation
- Evaluates the trained model on the test dataset.
- Computes accuracy and optionally displays classification results or confusion matrix.
