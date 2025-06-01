# Stress Detection Using Wearable Devices - WESAD Dataset

## Overview

This project focuses on early stress detection using wearable devices by leveraging the WESAD dataset — a widely recognized multimodal dataset for wearable stress and affect detection.

The repository provides:

- Data preprocessing for raw physiological signals (ECG, EDA, etc.)
- Feature extraction using an Autoencoder approach
- Implementation of machine learning classifiers (SVM, MLP) to classify stress levels
- Scripts and notebooks for easy experimentation and reproducible research

---

## Downloading the WESAD Dataset

Due to the dataset size and licensing restrictions, the WESAD dataset is **not included** in this repository.  
You must download it manually here:  
[WESAD Dataset Download](https://uni-siegen.sciebo.de/s/HGdUkoNlW1Ub0Gx)

---

## Setup Instructions

1. Download and extract the WESAD dataset from the link above.  
2. Place the extracted folder inside this repository at:  
```bash
dataset/raw/WESAD
```

---

## How to Run

Run the following Jupyter notebooks **in this order**:

1. `merge_data.ipynb`  
- Preprocesses and merges the raw WESAD sensor data.

2. `ae_feature_extraction.ipynb`  
- Extracts features from the preprocessed data using an Autoencoder model.

3. `SVM_classifier.ipynb` or `MLP_classifier.ipynb`  
- Trains and evaluates stress detection models (choose one or try both).

---

## Notes

- Make sure your working directory is the `notebook/WESAD` of this repository when running notebooks.  
- If you encounter any issues or have questions, feel free to open an issue.

---

Thank you for using this project!