# Gaussian Discriminant Analysis (GDA) Simulation

![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Assignment](https://img.shields.io/badge/Assignment-HW2%20--%20Question%205-green)

This folder contains a manual implementation and simulation of a **Gaussian Discriminant Analysis (GDA)** classifier without using high-level libraries like scikit-learn.

## Project Overview
In this project, we generate synthetic data from two distinct Gaussian distributions to simulate a binary classification problem. The goal is to build a Bayes Classifier from scratch by mathematically deriving the discriminant functions and the optimal decision boundary.

**Key Concepts Implemented:**
* **Synthetic Data Generation:** Sampling from Normal Distributions $N(\mu, \sigma)$.
* **Discriminant Function:** Manual implementation of $g(x) = \ln P(x|C_k) + \ln P(C_k)$.
* **Decision Boundary:** Analytical calculation of the boundary where $g_1(x) = g_2(x)$.
* **Sensitivity Analysis:** Visualizing how changing Prior Probabilities ($\pi$) shifts the boundary.
* **Evaluation Metrics:** Calculation of Confusion Matrix, Precision, Recall, and F1-Score from scratch.
* **ROC Curve:** Plotting the Receiver Operating Characteristic curve and calculating AUROC by sweeping the threshold $\tau$.

## Files
* `GDA_Simulation_From_Scratch.ipynb`: The main notebook containing the mathematical derivations, simulation code, and visualizations.
* *(Note: No external CSV dataset is required. All data is generated synthetically within the notebook.)*

## How to run
1.  Open the notebook.
2.  Run all cells sequentially.
3.  Observe the plots for PDF distributions, Histograms, and the ROC curve.
