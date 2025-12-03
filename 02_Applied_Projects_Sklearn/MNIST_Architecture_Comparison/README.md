# Image Classification & Translation Invariance Analysis

![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Assignment](https://img.shields.io/badge/Assignment-HW5%20--%20Question%206-green)

This project implements and compares three neural network architectures (**MLP**, **LeNet-5**, **ResNet-18**) to classify handwritten digits from the **MNIST** dataset and investigates their **Translation Invariance** capabilities.

## Project Overview
The goal is to move beyond simple classification accuracy and analyze how different architectures handle spatial variations. We train three distinct models and conduct a controlled experiment where input images are shifted (translated) to test prediction stability.

**Architectures & Techniques:**
* **Multilayer Perceptron (MLP):** A deep fully connected network acting as a baseline.
* **LeNet-5:** Implementation of the classic CNN architecture using Sigmoid activations and Average Pooling.
* **ResNet-18:** Adaptation of a modern Residual Network for single-channel (grayscale) MNIST inputs (without resizing images).
* **Translation Invariance Test:** A custom experiment that artificially shifts test images to evaluate model robustness.

## Files
* `MNIST_Analysis.ipynb`: The main notebook containing data loading, model definitions, training loops, and the invariance experiment.
* *Note: The MNIST dataset is downloaded automatically via `torchvision` within the notebook.*

## Key Results
* **Accuracy:** Both CNN-based models (LeNet-5 and ResNet-18) achieved superior accuracy (>98%) compared to the MLP.
* **Translation Invariance:**
    1.  **MLP:** Lacks spatial awareness; predictions fail even with small shifts (e.g., 3 pixels).
    2.  **CNNs:** Demonstrate robustness against small translations due to convolution and pooling layers.
    3.  **Limitations:** Significant shifts (>6 pixels) cause failure in all models, indicating the need for Data Augmentation for extreme robustness.

## How to run
1.  Install the required libraries: `torch`, `torchvision`, `matplotlib`, `seaborn`, `tqdm`.
2.  Run the notebook. The dataset will be downloaded to a `./data` folder automatically.
3.  Execute the final cells to visualize the Translation Invariance experiment results.
