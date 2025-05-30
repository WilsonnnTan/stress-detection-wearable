# Stress Detection Using Wearable Devices - WESAD Dataset

## Overview

This repository presents a comprehensive approach to early stress detection using wearable devices, leveraging the WESAD dataset—a widely recognized multimodal dataset for wearable stress and affect detection.

The project includes:

- Data preprocessing pipelines to handle raw physiological signals such as ECG, EDA, etc.
- Implementation of machine learning models to classify stress levels based on sensor data.
- Experiments with different feature extraction methods and model architectures.
- Support for integration with additional datasets to enhance robustness and generalization.
- Tools to facilitate reproducible research and easy experimentation.

This work aims to provide a foundation for researchers and practitioners interested in stress monitoring through wearable technology and IoT-based solutions.

---

## Downloading the WESAD Dataset

To run the scripts and train or test the models, you need to download the WESAD dataset manually because of its size and licensing.

Please download the dataset from the following link:

[WESAD Dataset Download](https://uni-siegen.sciebo.de/s/HGdUkoNlW1Ub0Gx)

---

## Setup Instructions

1. Download and extract the datasets from the provided links.
2. Place the extracted folders inside the appropriate subfolders under `data/raw/` in this repository.
3. Run the preprocessing scripts for each dataset (e.g., `preprocess.py`) to prepare the data for training and evaluation.  
4. Use the provided notebooks or scripts to train or evaluate the models for each dataset.

---

## Notes

- The raw dataset is **not included** in this repository due to size and licensing restrictions.
- Please ensure you comply with the dataset's terms of use.
- If you have any questions or issues, feel free to open an issue in this repository.

---

Thank you for using this project!  