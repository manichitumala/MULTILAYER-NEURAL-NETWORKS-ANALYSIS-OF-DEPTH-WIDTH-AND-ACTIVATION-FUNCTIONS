# Multilayer Neural Networks: Depth, Width, and Activation Analysis

## Overview
This project investigates how architectural choices in Multilayer Perceptrons (MLPs) affect model performance.

The study focuses on:
- Depth (number of hidden layers)
- Width (number of neurons per layer)
- Activation functions (ReLU, Tanh, Sigmoid)

The goal is to understand how these factors influence learning behaviour, model capacity, and generalisation.

---

## Dataset
A synthetic non-linear dataset was generated using `make_moons` from scikit-learn.

- 1000 samples
- Non-linearly separable
- 80/20 train-test split
- Standardised features

---

## Experiments

### 1. Depth
- Compared 1, 2, and 3 hidden layers
- Observed improved performance with increasing depth
- Diminishing returns beyond optimal depth

### 2. Width
- Tested 16, 64, and 128 neurons
- Larger width improved performance initially
- Minimal gains after sufficient capacity

### 3. Activation Functions
- ReLU: Best performance and stability
- Tanh: Moderate performance
- Sigmoid: Slower learning due to vanishing gradients

---

## Accessibility
This project includes accessibility considerations:

- Colour-blind friendly visualisations (cividis colormap)
- Clear axis labels and titles
- Readable font sizes
- Structured and documented code

---

## How to Run

1. Install dependencies:
```bash
pip install -r requirements.txt
