# Pure-MNIST: MNIST from Scratch

A modular, dependency-free Deep Neural Network (DNN) implemented in pure Python and NumPy. This project deconstructs the "black box" of modern AI frameworks by manually implementing backpropagation, matrix-based weight updates, and activation gradients.

## Overview
The goal of this repository is to demonstrate the fundamental calculus and linear algebra that powers Deep Learning. By avoiding high-level libraries like PyTorch or TensorFlow, this implementation handles the raw "dirty work" of:
* **He Initialization** for stable starting weights.
* **Manual Backpropagation** using the Chain Rule.
* **Vectorized Matrix Operations** for high-performance training on CPUs.
* **Softmax & Cross-Entropy** integration for multi-class classification.

## Architecture
The network is designed with a modular "Layer" API, allowing for easily swappable architectures:
1. **Input Layer**: 784 neurons (flattened 28x28 MNIST images).
2. **Hidden Layer**: 128 neurons with **ReLU** activation.
3. **Output Layer**: 10 neurons with **Softmax** activation.



## Components
| Module | Responsibility |
| :--- | :--- |
| `DenseLayer` | Manages weights/biases and performs $Y = XW + b$. |
| `ReLU` | Introduces non-linearity; handles the "dead neuron" gradient mask. |
| `Softmax` | Converts raw logits into stable probabilities. |
| `NeuralNetwork` | A container class that orchestrates the forward and backward flow. |

## Performance
<img width="373" height="217" alt="image" src="https://github.com/user-attachments/assets/640c8d46-dcaf-49a2-8334-04de85e3f370" />



## Installation & Usage
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/aditya-ravi11/Pure-MNIST.git](https://github.com/aditya-ravi11/Pure-MNIST.git)
2. **Run the code:**
   ```bash
   python main.py
