# Multilayer Neural Networks: Depth, Width, and Activation Functions

## Overview

This project presents a structured experimental analysis of how architectural choices in **Multilayer Perceptrons (MLPs)** affect model performance.

The study focuses on three key factors:

* **Depth** — number of hidden layers
* **Width** — number of neurons per layer
* **Activation functions** — ReLU, Tanh, and Sigmoid

The objective is to understand how these components influence:

* Model capacity
* Learning dynamics
* Generalisation performance

This work is designed as a **tutorial-style resource**, enabling others to apply these insights in their own machine learning tasks.

---

## Motivation

While neural networks are theoretically capable of approximating complex functions, their practical performance depends heavily on architectural design choices.

This project bridges the gap between:

* **Theory** (e.g., Universal Approximation Theorem)
* **Practice** (training stability, overfitting, efficiency)

---

## Dataset

A synthetic dataset was generated using `make_moons` from `scikit-learn`.

**Characteristics:**

* 1000 samples
* Non-linearly separable
* Two input features
* 80/20 train-test split
* Standardised features

This dataset was chosen to clearly demonstrate how neural networks learn nonlinear decision boundaries.

---

## Methodology

### 1. Depth Analysis

Models with varying numbers of hidden layers were trained:

* 1 hidden layer
* 2 hidden layers
* 3 hidden layers

**Observation:**

* Increasing depth improves representation
* Performance saturates beyond optimal depth

---

### 2. Width Analysis

The number of neurons per layer was varied:

* 16 neurons
* 64 neurons
* 128 neurons

**Observation:**

* Small models underfit
* Moderate width performs best
* Larger widths yield diminishing returns

---

### 3. Activation Function Analysis

Different activation functions were compared:

* **ReLU** — strong gradient flow, fast convergence
* **Tanh** — zero-centred, moderate performance
* **Sigmoid** — prone to vanishing gradients

**Observation:**
ReLU consistently provides the most stable and efficient training.

---

## Results and Key Insights

* Increasing **depth** enables hierarchical feature learning but shows diminishing returns
* Increasing **width** improves capacity up to a threshold
* **ReLU activation** significantly improves optimisation stability
* Model performance depends on balancing **capacity and generalisation**

---

## Visualisation

The experiment includes decision boundary plots to illustrate how model complexity changes with architecture.

These plots demonstrate:

* Simple boundaries for shallow networks
* More flexible boundaries for deeper/wider models

---

## Accessibility

This project incorporates accessibility best practices:

* Colour-blind friendly visualisations using the **cividis** colormap
* Clear axis labels and descriptive titles
* Readable font sizes
* Structured, well-documented code

These measures ensure the tutorial is usable by a wide audience.

---

## Repository Structure

```
mlp-depth-width-analysis/
│
├── mlp_experiment_explained.ipynb   # Main tutorial notebook
├── mlp_experiment_final.py          # Script version of experiment
├── README.md                        # Project documentation
├── requirements.txt                # Dependencies
└── LICENSE                         # Usage permissions
```

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/mlp-depth-width-analysis.git
cd mlp-depth-width-analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

```bash
jupyter notebook mlp_experiment_explained.ipynb
```

---

## Reproducibility

* Fixed random seed ensures consistent results
* Full implementation provided
* All experiments can be reproduced directly from the notebook

---

## Limitations and Future Work

* Experiments are conducted on a synthetic dataset
* Results may differ on high-dimensional or real-world data

Future work could include:

* Testing on real datasets
* Exploring regularisation techniques (dropout, L2)
* Extending to deeper architectures

---

## Ethical Considerations

Although this study uses synthetic data, real-world neural networks may:

* Learn biased patterns from data
* Lack interpretability
* Be sensitive to overfitting

Responsible model design requires:

* Careful dataset selection
* Evaluation on unseen data
* Consideration of fairness and transparency

---

## References

* Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*
* Bishop, C. M. (2006). *Pattern Recognition and Machine Learning*
* Nielsen, M. A. (2015). *Neural Networks and Deep Learning*
* Stanford CS231n: Convolutional Neural Networks

---

## License

This project is licensed under the MIT License.
