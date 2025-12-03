# Diabetes Prediction with Logistic Regression

![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Assignment](https://img.shields.io/badge/Assignment-HW1%20--%20Question%206-green)

## Project Overview
A binary classification project to predict diabetes using the **Pima Indians Diabetes Dataset**.
The main focus is not just applying a model, but critically analyzing **preprocessing strategies**—specifically comparing *Mean Imputation* vs. *Feature Dropping* for handling missing data.

## Dataset
* **Source:** Standard Pima Indians Diabetes Dataset.
* **Features:** Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age.
* **Target:** `Outcome` (0: Healthy, 1: Diabetic).

## Methodology

### 1. Exploratory Data Analysis (EDA)
* Analyzed feature correlations to find strong predictors (e.g., Glucose).
* Identified missing values encoded as `0` in biologically impossible contexts (e.g., 0 for Insulin or SkinThickness).

### 2. The "Imputation Trap" Experiment
I evaluated two approaches for handling missing values in `Insulin` and `SkinThickness`:

**Approach A: Mean Imputation (Failed)**
  Replacing missing values with the **Global Mean** created artificial peaks in the data distribution. This caused the Positive and Negative classes to overlap significantly, reducing model accuracy.

**Approach B: Feature Selection (Adopted)**
  Dropping features with excessive missing data proved to be more effective. This preserved the natural data distribution and led to a robust decision boundary.

### 3. Model Implementation
* **Algorithm:** Logistic Regression (Scikit-Learn).
* **Settings:** Optimized `max_iter` for convergence and used default L2 regularization.

## Results
The model was evaluated using:
* **Confusion Matrix:** To analyze misclassifications.
* **Classification Report:** Precision, Recall, and F1-Score.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn.
