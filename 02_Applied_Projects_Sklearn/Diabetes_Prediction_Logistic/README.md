# Diabetes Prediction Analysis using Logistic Regression

## Project Overview
This project focuses on the binary classification problem of predicting diabetes onset in patients using the Pima Indians Diabetes Dataset. The primary objective is to implement a Logistic Regression model while critically analyzing data preprocessing strategies. A significant portion of this analysis is dedicated to investigating the impact of different missing value handling techniques—specifically median imputation versus feature selection—on the model's decision boundary and overall performance.

## Dataset
The analysis utilizes the Pima Indians Diabetes Database.
* **Source:** National Institute of Diabetes and Digestive and Kidney Diseases.
* **Features:** The dataset includes medical predictor variables such as Glucose level, BMI, Insulin, Age, and Blood Pressure.
* **Target Variable:** `Outcome` (0 or 1), indicating the diagnosis of diabetes.

## Methodology

### 1. Exploratory Data Analysis (EDA)
The project begins with a statistical examination of the dataset to understand feature distributions and correlations. Key steps include:
* Analysis of feature correlation to identify predictors with the highest impact on the target variable.
* Identification of missing values encoded as zeros (0) in biologically impossible contexts (e.g., zero Insulin or Skin Thickness).

### 2. Preprocessing Experiment: Imputation vs. Feature Dropping
A critical finding of this project involves the handling of missing data. Two distinct approaches were evaluated:

* **Approach A: Median Imputation**
    Missing values in the `Insulin` and `SkinThickness` columns were initially replaced with the median of the respective features. Analysis of the resulting Kernel Density Estimation (KDE) plots revealed that this method introduced significant bias. The imputation created artificial peaks in the data distribution, causing the feature distributions of positive and negative classes to overlap, thereby reducing model separability.

* **Approach B: Feature Selection (Adopted Strategy)**
    Given the distortion caused by imputation, the final strategy involved removing features with excessive missing data. This approach preserved the natural distribution of the remaining high-quality features, leading to a more robust model.

### 3. Model Implementation
A Logistic Regression model was trained on the cleaned dataset. The implementation utilizes the Scikit-Learn library with the following specifications:
* **Solver:** lbfgs (Limited-memory Broyden–Fletcher–Goldfarb–Shanno algorithm).
* **Regularization:** L2 penalty (default).
* **Optimization:** Increased maximum iterations to ensure convergence.

## Results and Evaluation
The model performance is evaluated using standard classification metrics:
* **Confusion Matrix:** To visualize true positives, true negatives, false positives, and false negatives.
* **Classification Report:** Providing Precision, Recall, and F1-Score for both classes.

## Technologies Used
* **Python 3.x**
* **Scikit-Learn:** For model implementation and metrics.
* **Pandas & NumPy:** For data manipulation and vectorization.
* **Matplotlib & Seaborn:** For data visualization and distribution analysis.

## Usage
To replicate the analysis, ensure the required dependencies are installed and run the Jupyter Notebook:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook diabetes_prediction.ipynb