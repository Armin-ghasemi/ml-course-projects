# Multilayer Perceptron (MLP) Implementation

![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![Assignment](https://img.shields.io/badge/Assignment-HW5%20--%20Question%205-green)

This folder contains a manual implementation of a **Feed-Forward Neural Network (Multilayer Perceptron)** designed to solve a regression problem using **PyTorch**.

## Project Overview
In this project, we address the **House Price Prediction** problem. 

While this project resides in the *Applied Frameworks* category, we deliberately avoid using high-level abstraction wrappers (like Scikit-Learn's `MLPRegressor`). Instead, we leverage **PyTorch's fundamental building blocks** (such as `nn.Module` and the Autograd engine) to implement the architecture, forward propagation, and optimization loop manually. This approach provides a deeper understanding of the underlying mechanics of Deep Learning frameworks.

**Key Concepts Implemented:**
* **Advanced Preprocessing:**
    * **Missing Value Imputation:** Strategic filling of numerical gaps with median and categorical gaps with a 'Zero' token.
    * **Target Encoding:** Converting categorical features into numerical values based on the target variable average.
    * **Normalization:** Standardizing numerical features ($Z = \frac{X - \mu}{\sigma}$) for stable convergence.
* **Manual Network Design:**
    * Defining a deep architecture with **3 Hidden Layers** (64 neurons each).
    * Using **ReLU** activation functions.
* **Custom Training Loop:**
    * Manually computing the **Forward Pass**.
    * Calculating **MSE Loss**.
    * Performing **Backpropagation** (`loss.backward()`).
    * Updating weights using the **Adam Optimizer**.

## Results & Performance
The model was trained for **1000 Epochs**. The evaluation metrics on the test set demonstrate strong predictive performance:

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **MAPE** | **14.86%** | On average, the prediction error is less than 15%. |
| **RMSLE** | **0.194** | Indicates the model handles price scaling well. |
| **RMSE** | **36,644** | Standard deviation of the prediction errors. |
| **MAE** | **25,485** | Average absolute difference between predicted and actual prices. |

## Files
* `MLP_Manual_Implementation_PyTorch.ipynb`: The main notebook containing preprocessing, model definition, and training loop.
* `train.csv`: The training dataset (House Prices).
* `test.csv`: The test dataset (House Prices).

## How to run
1.  Open the notebook `MLP_Manual_Implementation_PyTorch.ipynb`.
2.  Ensure you have the required libraries installed:
    ```bash
    pip install torch pandas numpy category_encoders matplotlib
    ```
3.  Run all cells to preprocess data, train the MLP, and view the loss plots and final metrics.
