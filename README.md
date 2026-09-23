<div align="center">
    <table style="border: none; border-collapse: collapse;">
        <tr>
            <td align="center" width="20%" style="border: none;">
                <img src="https://i.ibb.co/yXKQmtZ/logo1.png" width="120" alt="University of Tehran Logo"/>
            </td>
            <td align="center" width="60%" style="border: none;">
                <h1>Machine Learning<br><small>Course Projects & Assignments</small></h1>
            </td>
            <td align="center" width="20%" style="border: none;">
                <img src="https://i.ibb.co/wLjqFkw/logo2.png" width="150" alt="ECE Faculty Logo"/>
            </td>
        </tr>
    </table>
</div>

---

<div align="center">

![Language](https://img.shields.io/badge/Language-Python%203.x-yellow)
![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![Semester](https://img.shields.io/badge/Semester-Fall%202024-orange)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)

</div>

## Overview

This repository contains a collection of assignments, projects, and a final capstone implemented for the Machine Learning course. The objective of this repository is to demonstrate a comprehensive understanding of machine learning principles, ranging from the mathematical derivation of core algorithms to the application of modern deep learning frameworks.

The projects are categorized into three distinct modules: manual implementation of algorithms, application of standard frameworks, and an end-to-end signal processing pipeline.

## Academic Context

* **Course:** Machine Learning
* **Institution:** University of Tehran, School of Electrical & Computer Engineering (ECE)
* **Semester:** Fall 2024
* **Level:** Undergraduate (B.Sc.) - 7th Semester

## Repository Structure

### 01. Algorithms From Scratch
**Focus: Mathematical Derivation & Low-Level Implementation**

This module focuses on the fundamental mechanics of machine learning algorithms. To ensure a thorough understanding of the underlying mathematics, the implementations in this section rely solely on **NumPy** for vectorization, avoiding high-level machine learning libraries.

* **Key Implementations:** Optimization Algorithms (Newton/Descent), Linear Regression, Gaussian Discriminant Analysis (GDA), Decision Trees (ID3).
* [View Directory](./01-Algorithms_From_Scratch)

### 02. Applied Projects & Frameworks
**Focus: Deep Learning, Architecture Design & Industry Tools**

This section transitions to solving practical problems using industry-standard frameworks such as **PyTorch** and **Scikit-Learn**. The primary emphasis is on data preprocessing, model architecture design, hyperparameter tuning, and performance evaluation.

* **Key Projects:** Housing Price Regression (MLP), MNIST Classification (CNNs/ResNet), Customer Segmentation (K-Means), Diabetes Prediction.
* [View Directory](./02-Applied_Projects_Frameworks)

### 03. Audio Analysis Capstone
**Focus: End-to-End Signal Processing Pipeline**

The final project presents a complete system for analyzing raw audio waveforms. It integrates Digital Signal Processing (DSP) techniques with machine learning models to extract semantic information from audio data.

* **Tasks:** Voice Activity Detection (VAD), Unsupervised Speaker Clustering, Gender Classification, and Biometric Speaker Identification.
* [View Directory](./03_Final_Project_Audio_Analysis)

## Tech Stack

The following libraries and tools were utilized across the projects:

| Category | Libraries & Tools |
| :--- | :--- |
| **Core & Math** | `NumPy`, `Pandas`, `SymPy` |
| **Machine Learning** | `Scikit-Learn`, `SciPy` |
| **Deep Learning** | `PyTorch` (Custom `nn.Module`, Autograd) |
| **Audio Processing** | `Librosa`, `SoundFile` |
| **Visualization** | `Matplotlib`, `Seaborn`, `Graphviz` |

## Getting Started

To access the code and notebooks, clone the repository using the following command:

```bash
git clone [https://github.com/Armin-ghasemi/ml-course-projects.git](https://github.com/Armin-ghasemi/ml-course-projects.git)
cd ml-course-projects
```

### Note on Dependencies

* **Standard Projects (01 & 02):** These directories rely on standard data science and machine learning libraries, including **NumPy**, **Pandas**, **Matplotlib**, **Scikit-Learn**, and **PyTorch**. No specific dependency file is provided for these modules, as they are compatible with standard pre-configured Python environments.
* **Capstone Project (03):** The Audio Analysis project requires specialized signal processing libraries. Please refer to `03_Final_Project_Audio_Analysis/requirements.txt` for the installation instructions specific to that module.

---
*For detailed mathematical derivations, architecture diagrams, and result analysis, please refer to the documentation within each subdirectory.*
