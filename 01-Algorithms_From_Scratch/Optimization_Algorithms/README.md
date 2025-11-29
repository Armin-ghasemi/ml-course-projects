# Optimization Algorithms: Steepest Descent vs. Newton's Method


![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Assignment](https://img.shields.io/badge/Assignment-HW3%20--%20Question%204-green)

This folder contains a manual implementation of fundamental optimization algorithms to find the global minimum of the **Rosenbrock Function** (also known as the Banana function).

## Project Overview
The Rosenbrock function is a famous non-convex function used as a performance test problem for optimization algorithms. The global minimum is inside a long, narrow, parabolic valley, which makes it challenging for algorithms to converge efficiently.

$$f(x) = 100(x_2 - x_1^2)^2 + (1 - x_1)^2$$

**Algorithms Implemented (From Scratch):**
1.  **Steepest Descent (Gradient Descent):** Uses the first-order derivative ($\nabla f$) to move towards the minimum.
2.  **Newton's Method:** Uses second-order information (Hessian matrix $H$) for faster convergence.
3.  **Hybrid Approach:** A strategic combination of both methods to leverage the stability of Gradient Descent in early stages and the speed of Newton's Method near the minimum.

## Files
* `Rosenbrock_Optimization_Newton_vs_GD.ipynb`: The main notebook containing the mathematical derivations, implementation loops, and comparison plots.

## Key Features
* **Symbolic Computation:** Using `SymPy` to derive Gradient and Hessian formulas.
* **Manual Optimization Loops:** Implementing the update rules $x_{k+1} = x_k - \alpha \nabla f(x_k)$ and $x_{k+1} = x_k - H^{-1}\nabla f(x_k)$ using `NumPy`.
* **Visualization:** Plotting the convergence path and function values over iterations to compare the efficiency of each method.

## How to run
1.  Open the notebook.
2.  Run all cells to see the optimization process step-by-step.
3.  Compare the final results and the number of iterations required by each method.
