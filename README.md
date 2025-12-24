# AdaBoost vs Neural Networks

A practical comparison of **AdaBoost** and **Neural Network (MLP)** regression models on tabular data, with a focus on performance, interpretability, and model behavior.  
The analysis is conducted using the California Housing dataset and presented as a fully documented, end-to-end notebook.

---

## Overview

This project compares two fundamentally different regression approaches:

- **AdaBoost Regressor** — a tree-based boosting method  
- **Neural Network Regressor (Multi-Layer Perceptron)** — a gradient-based, flexible function approximator  

Rather than focusing only on predictive accuracy, the project emphasizes:
- fair and consistent evaluation,
- understanding model behavior,
- and explaining results using interpretable diagnostics.

The notebook is written to be readable by both technical and non-technical audiences.

---

## Key Questions

- How much improvement do learning-based models provide over a simple baseline?
- How does a tree-based boosting model compare to a neural network on tabular data?
- What tradeoffs exist between predictive performance and interpretability?
- How do explainability tools help understand complex models?

---

## Dataset

The analysis uses the **California Housing dataset**, derived from the 1990 U.S. census.

- Each row represents a geographic block group  
- The target variable is median house value (in hundreds of thousands of USD)  
- All features are numerical and describe demographic, housing, and geographic characteristics  

A known upper cap in the target variable is explicitly explored and discussed in the analysis.

---

## Methodology

The notebook follows a clear, reproducible workflow:

1. Problem setup and evaluation metrics  
2. Exploratory data analysis  
3. Model-specific preprocessing pipelines  
4. Baseline model (mean predictor)  
5. AdaBoost regression with hyperparameter tuning  
6. Neural Network regression with scaling, regularization, and early stopping  
7. Model comparison using RMSE, MAE, and R²  
8. Model interpretation using:
   - residual analysis  
   - permutation feature importance  
   - partial dependence plots  
9. Conclusions and next steps  

All models are evaluated on the same train/test split to ensure a fair comparison.

---

## Results (Summary)

- The **baseline model** performs poorly, confirming that meaningful structure exists in the data.
- **AdaBoost** provides a strong improvement by capturing non-linear relationships and feature interactions.
- The **Neural Network** achieves the best overall performance, substantially reducing prediction error and explaining nearly **80% of the variance** in house values.

Interpretability analysis shows that:
- geographic location is a dominant driver of predictions,
- median income exhibits strong non-linear effects,
- some features contribute primarily through interactions rather than linear relationships.

---

## Repository Contents

- `adaboost_vs_neural_network_regression.ipynb`  
  Main notebook containing the full analysis, explanations, and results.

---

## How to Run

1. Clone the repository  
2. Open the notebook in Jupyter or VS Code  
3. Run cells sequentially from top to bottom  

The project relies on standard Python data science libraries:
- NumPy  
- pandas  
- matplotlib / seaborn  
- scikit-learn  

---

## Notes on Interpretability

Explainability tools are used to support understanding rather than claim causality.  
Permutation importance and partial dependence plots are interpreted carefully, with explicit discussion of their assumptions and limitations.

---

## Future Work

Possible extensions include:
- ensemble combinations of tree-based and neural models,
- additional geographic feature engineering,
- uncertainty estimation for predictions,
- comparison with linear and regularized regression models.

---

## License

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this code with attribution.
