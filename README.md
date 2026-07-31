# Gastrointestinal Tract Anomalies Detection using Sobel-Guided Edge Attention (SGEA), EfficientNetB0 and Local Feature Entropy Masking (LFEM)

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.10-orange.svg)](https://www.tensorflow.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Project Overview

This repository contains the implementation of an **Explainable Artificial Intelligence (XAI)** framework for **automated gastrointestinal (GI) disease classification** using endoscopic images.

The proposed framework integrates **EfficientNetB0** with a **Sobel-Guided Edge Attention (SGEA)** module to improve lesion feature extraction while employing **Grad-CAM++** and **Local Feature Entropy Masking (LFEM)** to generate refined visual explanations, enhancing model transparency and interpretability.

The project was developed as part of the **Internship** research work for **IEEE CIS Kolkata Chapter Summer Internship 2026**.

---

# Highlights

- Deep Learning based GI disease classification
- EfficientNetB0 transfer learning backbone
- Sobel-Guided Edge Attention (SGEA)
- Explainable AI using Grad-CAM++
- Local Feature Entropy Masking (LFEM)
- Multi-class gastrointestinal disease detection
- TensorFlow–Keras implementation
- Transfer learning and fine-tuning
- Comprehensive evaluation using standard classification metrics

---

# Proposed Framework

The proposed workflow consists of the following stages:

1. Input Endoscopic Image
2. Image Preprocessing
3. EfficientNetB0 Feature Extraction
4. Sobel-Guided Edge Attention (SGEA)
5. Global Average Pooling
6. Fully Connected Classification Layers
7. Softmax Classification
8. Grad-CAM++ Explanation
9. Local Feature Entropy Masking (LFEM)
10. Final Disease Prediction with Refined Visual Explanation

---

# Dataset

This project uses the **Kvasir-v2** dataset.

> **Note:** The dataset is **NOT included** in this repository due to its large size and the dataset distribution policy.

## Dataset Statistics

| Parameter | Value |
|-----------|-------|
| Dataset | Kvasir-v2 |
| Total Images | 8,000 |
| Number of Classes | 8 |
| Image Size Used | 224 × 224 |

## Disease Classes

- Dyed Lifted Polyps
- Dyed Resection Margins
- Esophagitis
- Normal Cecum
- Normal Pylorus
- Normal Z-Line
- Polyps
- Ulcerative Colitis

## Official Dataset

**Dataset Website**

https://datasets.simula.no/kvasir/

**Official Paper**

K. Pogorelov et al., *Kvasir: A Multi-Class Image Dataset for Computer Aided Gastrointestinal Disease Detection*, ACM Multimedia Systems Conference (MMSys), 2017.

**DOI**

https://doi.org/10.1145/3083187.3083212

Please download the dataset from the official website and place it inside the `dataset/` directory before running the notebook.

---

# Repository Structure

```
Gastrointestinal_Tract_Anomalies_Detection_RupamNag
│
├── dataset/
│   └── README.md
│
├── figures/
│
├── models/
│
├── notebooks/
│
├── outputs/
│
├── reports/
│
├── sample_images/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# Experimental Configuration

| Parameter | Value |
|-----------|-------|
| Framework | TensorFlow–Keras |
| Backbone | EfficientNetB0 |
| Image Size | 224 × 224 |
| Batch Size | 32 |
| Optimizer | Adam |
| Initial Learning Rate | 0.0001 |
| Fine-tuning Learning Rate | 0.00001 |
| Loss Function | Sparse Categorical Cross-Entropy |
| Maximum Epochs | 20 |
| Fine-tuning | Last 30 Layers |

---

# Performance Evaluation

The proposed framework is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Grad-CAM++ Visualization
- Local Feature Entropy Masking (LFEM)

---

# Requirements

- Python 3.10
- TensorFlow 2.10
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn
- Pandas

Install all required packages using:

```bash
pip install -r requirements.txt
```

---

# Running the Project

## Step 1

Clone the repository.

```bash
git clone https://github.com/rupamnag/Gastrointestinal_Tract_Anomalies_Detection_RupamNag.git
```

---

## Step 2

Download the Kvasir-v2 dataset.

https://datasets.simula.no/kvasir/

---

## Step 3

Place the downloaded dataset inside

```
dataset/
```

Example

```
dataset/

└── kvasir-dataset-v2/

    ├── dyed-lifted-polyps/

    ├── dyed-resection-margins/

    ├── esophagitis/

    ├── normal-cecum/

    ├── normal-pylorus/

    ├── normal-z-line/

    ├── polyps/

    └── ulcerative-colitis/
```

---

## Step 4

Open the notebook inside the `notebooks` directory.

Run all cells sequentially.

---

# Repository Contents

| Folder | Description |
|----------|-------------|
| dataset | Dataset download instructions only |
| notebooks | Training and evaluation notebooks |
| models | Trained model checkpoints |
| figures | Figures used in the report |
| outputs | Prediction and Grad-CAM outputs |
| reports | Evaluation reports and metrics |
| sample_images | Sample images for testing |

---

# Results

The repository includes:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Fine-tuning Results
- Confusion Matrix
- Classification Metrics
- Grad-CAM++ Visualizations
- LFEM Refined Heatmaps
- Sample Predictions

---

# Code Availability

The complete implementation of the proposed framework is available in this repository.

The dataset is distributed separately by its original authors and must be downloaded from the official website.

---

# Citation

If you use this work in your research, please cite the corresponding project report and the Kvasir-v2 dataset.

---

# Author

**Rupam Nag**

M.Tech (Computer Science & Engineering)

Aliah University, Kolkata

West Bengal, India

GitHub

https://github.com/rupamnag


---

# Acknowledgements

The author gratefully acknowledges:

- The creators of the **Kvasir-v2** dataset for providing a publicly available benchmark dataset for gastrointestinal disease research.
- The TensorFlow and Keras development teams for their open-source deep learning framework.
- IEEE CIS Kolkata Chapter Summer Internship 2026 for providing academic guidance and research support.

---

# License

This project is released under the **MIT License**.

See the `LICENSE` file for details.
