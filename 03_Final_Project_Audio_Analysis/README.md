# Audio Signal Processing and Analysis Capstone

![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Assignment](https://img.shields.io/badge/Assignment-Final%20%20Project%20-green)
![Stack](https://img.shields.io/badge/Stack-PyTorch%20%7C%20Librosa%20%7C%20Scikit--Learn-orange)

This directory hosts a comprehensive end-to-end pipeline for audio signal processing. The project bridges the gap between raw signal analysis and advanced machine learning, demonstrating how to transform unstructured audio data into meaningful insights using both unsupervised and supervised techniques.

---

## Project Abstract
The primary objective of this project is to implement a full audio analysis pipeline. Unlike standard datasets where features are provided, here we start from **raw audio waveforms**. We perform Digital Signal Processing (DSP) to extract relevant features and then apply machine learning algorithms for three distinct tasks:
1.  **Unsupervised Clustering:** Discovering latent patterns and grouping speakers without labels.
2.  **Gender Classification:** Binary classification to distinguish between male and female speakers.
3.  **Speaker Identification:** Biometric recognition of specific individuals.

---

## Algorithms and Techniques

To ensure robust performance and valid comparisons, we implemented and benchmarked a wide range of algorithms across different modules:

| Domain | Algorithms and Methods Implemented |
| :--- | :--- |
| **Preprocessing** | VAD (Voice Activity Detection), Butterworth Low-Pass Filter, Z-Score Normalization, Signal Segmentation. |
| **Feature Extraction** | MFCCs (20 Coefficients), Fundamental Frequency ($F_0$), Zero-Crossing Rate (ZCR). |
| **Clustering** | **PCA** (Dimensionality Reduction), **K-Means**, **DBSCAN** (Density-Based), **Hierarchical Clustering** (Agglomerative). |
| **Classification** | **SVM** (Linear, RBF, Polynomial kernels), **KNN**, **Logistic Regression**, **Random Forest**, **MLP** (Deep Neural Network). |

---

## Project Methodology and Analysis

### 1. Preprocessing Pipeline
**File:** `notebooks/01_Preprocessing_Pipeline.ipynb`

This module handles the cleaning and transformation of raw audio data. Since audio signals often contain silence or background noise, rigorous preprocessing is essential before feature extraction.

**Key Steps:**
* **Voice Activity Detection (VAD):** Removing silent parts of the audio to focus only on speech.
* **Noise Reduction:** Applying a Butterworth Low-Pass filter to eliminate high-frequency noise.
* **Segmentation:** Splitting long audio files into fixed 0.5-second segments to augment the dataset.
* **Feature Extraction:** Generating a 23-dimensional feature vector for each segment (20 MFCCs, Pitch, and ZCR).

---

### 2. Unsupervised Clustering
**File:** `notebooks/02_Unsupervised_Clustering.ipynb`

In this section, we explore the structure of the data without using any labels. We utilized dimensionality reduction and density-based clustering to verify if voice samples naturally segregate.

**Visual Analysis (PCA):**
We used **PCA** to reduce the 23-dimensional features into 2 dimensions. As seen in **Figure 1**, the data forms two distinct clusters naturally.

**Clustering Algorithm (DBSCAN):**
Instead of relying solely on centroid-based methods like K-Means, we applied **DBSCAN (Density-Based Spatial Clustering)**.
* **Advantage:** DBSCAN does not require specifying the number of clusters beforehand and is robust against outliers.
* **Result:** The algorithm successfully identified the dense regions corresponding to different voice types while marking ambiguous samples as noise.

| PCA Projection | DBSCAN Results |
| :---: | :---: |
| ![PCA Projection](/03_Final_Project_Audio_Analysis/results/figures/pca_2d_projection.png) | ![DBSCAN Clusters](/03_Final_Project_Audio_Analysis/results/figures/DBSCAN_final_clusters.png) |
| *Figure 1: Natural Data Separation* | *Figure 2: Density-Based Clustering* |

---

### 3. Gender Classification
**File:** `notebooks/03_Gender_Classification.ipynb`

In this supervised learning task, we trained models to classify speakers as Male or Female. We benchmarked traditional models (SVM, KNN) against a Deep Learning approach.

**Model Architecture:**
We designed a custom **Multi-Layer Perceptron (MLP)** using PyTorch with the following specifications:
* **Input Layer:** 23 neurons (Audio Features).
* **Hidden Layers:** 3 Fully Connected layers with ReLU activation and Dropout (p=0.3) for regularization.
* **Output Layer:** 2 neurons (Binary Class).

**Performance:**
The MLP model demonstrated stable learning dynamics (Figure 3) and achieved high accuracy on the test set. The confusion matrix (Figure 4) shows minimal misclassification.

| Training Dynamics | Confusion Matrix |
| :---: | :---: |
| ![Loss Curve](/03_Final_Project_Audio_Analysis/results/figures/mlp_training_dynamics.png) | ![Confusion Matrix](/03_Final_Project_Audio_Analysis/results/figures/mlp_final_confusion_matrix.png) |
| *Figure 3: Training Loss and Accuracy* | *Figure 4: Final Test Results* |

---

### 4. Speaker Identification (Biometrics)
**File:** `notebooks/04_Speaker_Identification.ipynb`

This is the most complex task: identifying **who** is speaking among a pool of 6 individuals (N-way classification). This simulates a biometric security system.

**Feature Importance Analysis:**
To understand how the model distinguishes people, we used **Random Forest** feature importance. The results show that **Fundamental Frequency (F0)** is the specific "fingerprint" of a speaker.

![Voice Print KDE](/03_Final_Project_Audio_Analysis/results/figures/speaker_voice_print_F0.png)
*Figure 5: Voice Prints - Distinct pitch distributions for different speakers.*

**Final Results:**
The multi-class MLP model was optimized for this task, achieving high precision across all 6 classes.

![Speaker ID Matrix](/03_Final_Project_Audio_Analysis/results/figures/mlp_speaker_id_confusion_matrix_standardized.png)
*Figure 6: Confusion Matrix for 6-Way Speaker Identification.*

---

## How to run

1.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

2.  **Run the Notebooks:**
    Navigate to the `notebooks/` directory. It is recommended to run the notebooks in order (02 to 04), as they rely on the datasets provided in the `data/` folder.

> **Note on Data Privacy:**
> The raw audio recordings are not included in this repository to protect student privacy. However, the **extracted feature datasets (.csv)** are included in `data/feature_stores/`, allowing full reproducibility of all machine learning and analysis steps (Notebooks 02, 03, and 04).
