# Machine Learning Algorithms: From Scratch

![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Language](https://img.shields.io/badge/Language-Python%20%7C%20NumPy-yellow)

This directory contains fundamental machine learning algorithms implemented manually using Python and NumPy. The primary objective is to demonstrate a mathematical understanding of optimization techniques, probabilistic modeling, and decision boundaries without reliance on high-level machine learning frameworks.

## Directory Contents

The following table provides an overview of the implementations included in this module. Each project focuses on the low-level derivation and coding of the algorithm mechanics.

| Project | Description | Key Methodologies |
| :--- | :--- | :--- |
| **[Optimization Algorithms](./Optimization_Algorithms)** | Minimization of the non-convex Rosenbrock function to compare convergence efficiency. | Steepest Descent, Newton's Method, Hybrid Approach, Symbolic Differentiation (SymPy) |
| **[Linear Regression](./Linear_Regression)** | Implementation of linear modeling for continuous target prediction. | Gradient Descent, Normal Equation, Cost Function Analysis |
| **[Gaussian Discriminant Analysis](./Gaussian_Discriminant_Analysis)** | A generative learning approach simulating a Bayes Classifier on synthetic Gaussian data. | Multivariate Gaussian Distribution, Decision Boundary Derivation, ROC/AUROC Analysis |
| **[Decision Tree (ID3)](./Decision_Tree_ID3_From_Scratch)** | Construction of a decision tree using entropy measures for classification. | Shannon Entropy, Information Gain, Recursive Splitting, Multi-way Branching (ID3) |

## Technical Implementation Details

To ensure transparency and educational value, the projects adhere to the following technical constraints:

* **Core Logic:** Implemented strictly in **Python 3.x**.
* **Numerical Operations:** **NumPy** is used for vectorization and matrix manipulation to ensure computational efficiency appropriate for manual implementations.
* **Symbolic Mathematics:** **SymPy** is utilized in optimization tasks to derive exact gradients and Hessians.
* **Visualization:** **Matplotlib** and **Seaborn** are used to plot decision boundaries, loss convergence curves, and data distributions.
* **Tree Visualization:** **Graphviz** is employed to render the structure of the generated decision trees.

## Academic Context

These implementations were developed as part of the Machine Learning course assignments at the **University of Tehran**. The focus is on translating theoretical mathematical formulas directly into executable code to verify the underlying logic of standard ML algorithms.

---
*Please refer to the README file within each subdirectory for mathematical derivations, usage instructions, and detailed analysis.*
