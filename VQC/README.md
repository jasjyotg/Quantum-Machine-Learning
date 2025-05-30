# Variational Quantum Classifier (VQC) using Qiskit

### 1. Dataset Preparation
- Loads the **MNIST** dataset using `sklearn.datasets`.
- Filters the dataset to include only the digits `0` and `1` for binary classification.
- Applies **Principal Component Analysis (PCA)** to reduce the image data to 2 dimensions, suitable for encoding into a quantum circuit.
- Splits the data into training and testing sets.

### 2. Quantum Feature Map
- Transforms classical features into quantum states using `ZFeatureMap`, which applies parameterized Z-rotations to encode the input features into a quantum circuit.

### 3. Variational Ansatz
- Defines a parameterized quantum circuit using `RealAmplitudes`, which introduces trainable parameters into the quantum model.
- This circuit serves as the variational ansatz to be optimized during training.

### 4. Variational Quantum Classifier (VQC) Model
- Constructs the `VQC` model using Qiskit's `VQC` class.
- Combines the feature map, ansatz, and a classical optimizer (COBYLA) to train the model.
- Uses `StatevectorSimulator` for noiseless simulation of the quantum circuit.

### 5. Training
- Trains the VQC on the MNIST binary classification subset.
- Monitors the optimization progress through the loss value.
- Can use multiple optimizers (Copybla , ADAM etc)

### 6. Evaluation
- Evaluates the trained model on the test set.
- Calculates and prints classification accuracy to assess model performance.
