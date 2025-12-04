# Applied Machine Learning & Frameworks

![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Stack](https://img.shields.io/badge/Stack-PyTorch%20%7C%20Scikit--Learn-orange)

This directory demonstrates the application of machine learning frameworks to solve real-world problems. Unlike the "Algorithms From Scratch" section, the focus here shifts towards end-to-end model development, including advanced data preprocessing, architecture selection, hyperparameter tuning, and comprehensive performance evaluation.

## Directory Contents

The projects in this section utilize industry-standard libraries such as **PyTorch** and **Scikit-Learn** to address regression, classification, and clustering tasks.

| Project | Domain | Key Techniques & Frameworks |
| :--- | :--- | :--- |
| **[Multilayer Perceptron (MLP)](./Multilayer_Perceptron)** | Housing Price Regression | **PyTorch (Manual Loop)**, Custom `nn.Module` Architecture, Advanced Feature Engineering (Target Encoding, Imputation), Adam Optimizer. |
| **[MNIST Architecture Comparison](./MNIST_Architecture_Comparison)** | Image Classification | **Deep Learning (CNNs)**, Comparative Analysis (MLP vs. LeNet-5 vs. ResNet-18), Translation Invariance Testing, Robustness Evaluation. |
| **[K-Means Segmentation](./KMeans_Customer_Segmentation)** | Customer Clustering | **Unsupervised Learning**, Elbow Method, Cluster Visualization, Behavioral Analysis of Mall Customers. |
| **[Diabetes Prediction](./Diabetes_Prediction_Logistic)** | Medical Diagnosis (Binary Classification) | **Logistic Regression**, Critical Data Analysis (Imputation vs. Feature Dropping), Correlation Analysis, Scikit-Learn Pipeline. |

## Technical Focus Areas

The implementations in this directory highlight several critical aspects of applied machine learning:

### 1. Deep Learning Architecture (PyTorch)
* **Custom Implementations:** Instead of using high-level wrappers, the Neural Network projects utilize PyTorch's `autograd` engine and `nn.Module` to manually define forward passes and training loops.
* **Architecture Evolution:** The projects demonstrate a progression from simple Dense Networks (MLP) to Convolutional Networks (LeNet-5) and Residual Networks (ResNet-18).

### 2. Data Engineering & Preprocessing
* **Handling Missing Data:** A critical comparison between statistical imputation (Mean/Median) and feature selection/dropping is presented in the Diabetes project.
* **Feature Transformation:** Techniques such as Z-Score Normalization and Target Encoding are applied to prepare raw data for convergence.

### 3. Model Evaluation Beyond Accuracy
* **Regression Metrics:** Evaluation using MAPE, RMSLE, and MAE to understand error distribution in housing prices.
* **Stability Testing:** The Image Classification project includes a custom "Translation Invariance" experiment to test how spatial shifts affect model predictions.

## Academic Context

These projects were developed as part of the Machine Learning course assignments at the **University of Tehran**. They serve to bridge the gap between theoretical knowledge and practical application using modern software stacks.

---
*Please refer to the README file within each subdirectory for detailed methodology, architecture diagrams, and result analysis.*
