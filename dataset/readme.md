# Kvasir-v2 Dataset

## Overview

This project uses the **Kvasir-v2** dataset for multi-class gastrointestinal (GI) disease classification from endoscopic images.

The dataset is **not included** in this repository because of its large size and to respect the original dataset distribution policy. Users must download the dataset from the official source before running the project.

---

# Dataset Information

| Attribute | Details |
|-----------|---------|
| Dataset Name | Kvasir-v2 |
| Domain | Gastrointestinal Endoscopy |
| Total Images | 8,000 |
| Number of Classes | 8 |
| Input Image Size Used | 224 × 224 pixels |
| Dataset Type | RGB Endoscopic Images |
| Task | Multi-class Image Classification |

---

# Disease Classes

The dataset contains eight balanced gastrointestinal disease classes:

1. Dyed Lifted Polyps
2. Dyed Resection Margins
3. Esophagitis
4. Normal Cecum
5. Normal Pylorus
6. Normal Z-Line
7. Polyps
8. Ulcerative Colitis

---

# Official Dataset Download

Download the dataset only from the official website:

**Dataset Website**

https://datasets.simula.no/kvasir/

**Direct Download Page**

https://datasets.simula.no/kvasir/

---

# Official Dataset Publication

K. Pogorelov, K. R. Randel, C. Griwodz, S. L. Eskeland, T. de Lange, D. Johansen, C. Spampinato, D. T. Dang-Nguyen, M. Lux, P. T. Schmidt, M. Riegler, and P. Halvorsen,

**"Kvasir: A Multi-Class Image Dataset for Computer Aided Gastrointestinal Disease Detection,"**

Proceedings of the 8th ACM Multimedia Systems Conference (MMSys),

Taipei, Taiwan,

2017,

pp. 164–169.

DOI:

https://doi.org/10.1145/3083187.3083212

---

# How the Dataset is Used in This Project

The downloaded dataset is used throughout the proposed framework as follows:

- Training the EfficientNetB0-based classification model.
- Learning edge-aware lesion features using the Sobel-Guided Edge Attention (SGEA) module.
- Fine-tuning the proposed model through transfer learning.
- Evaluating the trained model using the independent test set.
- Generating Grad-CAM++ visual explanations.
- Refining explainability using Local Feature Entropy Masking (LFEM).

The dataset is divided into training, validation, and testing subsets during model development.

---

# Dataset Preparation

After downloading, extract the dataset and place it inside the `dataset/` directory.

The folder structure should look like:

```
dataset/
│
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

Do **not** rename the class folders, as the notebook expects the original class names.

---

# Running the Project

1. Download the Kvasir-v2 dataset from the official website.
2. Extract the downloaded archive.
3. Place the extracted folder inside the `dataset/` directory as shown above.
4. Open the notebook from the `notebooks/` folder.
5. Execute all notebook cells sequentially.

---

# Dataset Citation

If you use this project or the dataset in academic research, please cite the original Kvasir-v2 publication:

```
K. Pogorelov, K. R. Randel, C. Griwodz, S. L. Eskeland,
T. de Lange, D. Johansen, C. Spampinato,
D. T. Dang-Nguyen, M. Lux, P. T. Schmidt,
M. Riegler, and P. Halvorsen,

"Kvasir: A Multi-Class Image Dataset for Computer
Aided Gastrointestinal Disease Detection,"

Proceedings of the 8th ACM Multimedia Systems Conference (MMSys),

2017,

pp. 164–169.

DOI: https://doi.org/10.1145/3083187.3083212
```

---

# Notes

- The dataset is **not redistributed** in this repository.
- Please use the official download source to obtain the dataset.
- Ensure that the directory structure remains unchanged before running the notebook.
- The implementation was developed and evaluated using the Kvasir-v2 dataset with an input image size of **224 × 224** pixels.

---

# Acknowledgements

The author gratefully acknowledges **Simula Research Laboratory** and the creators of the **Kvasir-v2** dataset for making this valuable benchmark publicly available to support research in computer-aided gastrointestinal disease diagnosis.
