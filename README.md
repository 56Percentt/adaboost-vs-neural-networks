# AdaBoost vs Neural Networks

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A practical comparison of AdaBoost and Neural Network regression models on tabular data, with a focus on predictive performance, interpretability, and model behavior. The analysis is conducted using the California Housing dataset and presented as a fully documented, end-to-end notebook.

---

## Overview

This project compares two fundamentally different regression approaches:

* **AdaBoost Regressor** — a tree-based boosting method
* **Neural Network Regressor (Multi-Layer Perceptron)** — a gradient-based function approximator

Rather than focusing solely on predictive accuracy, the project emphasizes fair evaluation, understanding model behavior, and explaining results using interpretable diagnostics. The notebook is designed to be accessible to both technical and non-technical audiences.

---

## Key Questions

* How much improvement do learning-based models provide over a simple baseline?
* How does a tree-based boosting model compare to a neural network on tabular data?
* What tradeoffs exist between predictive performance and interpretability?
* How do explainability tools help us understand complex models?

---

## Dataset

The analysis uses the **California Housing dataset**, derived from the 1990 U.S. census.

* Each row represents a geographic block group
* The target variable is median house value
* All features are numerical and describe demographic, housing, and geographic characteristics

---

## Methodology

The notebook follows a clear, reproducible workflow:

1. Problem setup and evaluation metrics
2. Exploratory data analysis
3. Model-specific preprocessing pipelines
4. Baseline model (mean predictor)
5. AdaBoost regression
6. Neural Network regression
7. Model comparison using RMSE, MAE, and R²
8. Model interpretation using:
   * Residual analysis
   * Permutation feature importance
   * Partial dependence plots
9. Conclusions and next steps

All models are evaluated on the same train/test split to ensure a fair comparison.

---

## Results (Summary)

* The **baseline model** performs poorly, confirming that meaningful structure exists in the data
* **AdaBoost** provides a strong improvement by capturing non-linear relationships and feature interactions
* The **Neural Network** achieves the best overall performance, substantially reducing prediction error and explaining approximately **80% of the variance** in house values

Interpretability analysis shows that:

* Geographic location is a dominant driver of predictions
* Median income exhibits strong non-linear effects
* Some features contribute primarily through interactions rather than linear relationships

---

## Repository Contents

```
adaboost-vs-neural-networks/
├── adaboost_vs_neural_network_regression.ipynb
├── artifacts/
├── .gitignore
├── LICENSE
└── README.md
```

* `adaboost_vs_neural_network_regression.ipynb` — Main notebook containing the full analysis, explanations, and results
* `artifacts/` — Saved model artifacts produced by the notebook
* `LICENSE` — MIT License
* `README.md` — This file

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/56Percentt/adaboost-vs-neural-networks.git
cd adaboost-vs-neural-networks
```

Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

Run the notebook:

```bash
jupyter notebook adaboost_vs_neural_network_regression.ipynb
```

Execute cells sequentially from top to bottom.

---

## Notes on Interpretability

Explainability tools are used to support understanding rather than claim causality. Permutation importance and partial dependence plots are interpreted carefully, with explicit discussion of their assumptions and limitations.

---

## Future Work

Possible extensions include:

* Ensemble combinations of tree-based and neural models
* Additional geographic feature engineering
* Uncertainty estimation for predictions
* Comparison with linear and regularized regression models

---

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute this code with attribution. See the `LICENSE` file for details.
