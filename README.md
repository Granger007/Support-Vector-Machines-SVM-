# Support Vector Machines (SVM) for Linear & Non-linear Classification

## Overview

This project demonstrates the use of **Support Vector Machines (SVM)** for binary classification using both **linear** and **RBF (Radial Basis Function)** kernels. The workflow includes data generation, model training, decision boundary visualization, hyperparameter tuning, and model evaluation.

## Objectives

* Load and prepare a binary classification dataset.
* Train SVM models with **linear** and **RBF** kernels.
* Visualize decision boundaries in 2D.
* Tune hyperparameters such as `C` and `gamma` using grid search.
* Evaluate performance using cross-validation.

## Tools & Libraries

* **Python 3**
* **NumPy** – numerical computations
* **Matplotlib** – plotting decision boundaries
* **Scikit-learn** – dataset generation, SVM implementation, model evaluation

## Dataset

We use `make_moons` from Scikit-learn to generate a 2D binary classification dataset with slight noise for a more realistic challenge.

## Steps

### 1. Load and Prepare Data

* Use `make_moons` to generate two classes.
* Split data into training (80%) and testing (20%) sets.

### 2. Train SVM Models

* **Linear kernel:** Good for linearly separable data.
* **RBF kernel:** Handles non-linear decision boundaries.

### 3. Visualize Decision Boundaries

* Generate a mesh grid over the feature space.
* Predict over the grid to plot the decision surface.
* Overlay training data points.

### 4. Hyperparameter Tuning

* Use `GridSearchCV` to find the best `C` and `gamma` values for the RBF kernel.
* Perform 5-fold cross-validation.

### 5. Evaluate Performance

* Test the best model on the hold-out test set.
* Print **accuracy**.

## Example Results

* Linear kernel may struggle with moon-shaped data.
* RBF kernel typically achieves higher accuracy.
* Best parameters often depend on dataset noise and complexity.

## Next Steps

* Try different datasets (`make_circles`, `classification datasets` from sklearn).
* Experiment with polynomial kernels.
* Compare SVM with other classifiers like logistic regression or random forests.
