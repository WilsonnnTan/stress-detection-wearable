# Emotion Recognition Using Wearable Devices - EmoWear Dataset

## Overview

This project focuses on **emotion recognition** (specifically Valence and Arousal) using physiological signals from wearable devices, leveraging the **EmoWear dataset**. This dataset provides multimodal data suitable for understanding and predicting emotional states.

The current implementation provides:

-   **Data Loading and Windowing:** Efficiently loads and segments physiological signals (EDA, Temperature, Heart Rate, Accelerometer) into time windows.
-   **Statistical Feature Extraction:** Extracts basic statistical features (mean, standard deviation, min, max) from each time window.
-   **Emotion Label Integration:** Integrates Valence and Arousal labels from survey data, aligning them with the extracted features.
-   **Robust Model Training:** Implements machine learning models (`StackingClassifier` for Valence, `StackingRegressor` for Arousal) with `GroupKFold` cross-validation to ensure reliable performance evaluation on unseen subjects.
-   **Visualizations:** Includes visualizations for model evaluation, such as Confusion Matrices for Valence classification and Scatter Plots for Arousal regression.

---

## EmoWear Dataset

Due to potential licensing restrictions and the nature of the dataset, the EmoWear dataset is **not included** in this repository.
You must download it manually here:
[EmoWear Dataset Download](https://zenodo.org/records/10407279)

You can also obtain the EmoWear dataset independently. Ensure your dataset includes:
-   Physiological sensor data (e.g., EDA, Temperature, HR, Accelerometer)
-   Survey data containing Valence and Arousal labels
-   Marker files indicating stimulus start/end times.

---

## Setup Instructions

1.  **Obtain the EmoWear Dataset:** Download or acquire the EmoWear dataset.
2.  **Extract and Organize Data:** Ensure your EmoWear data (CSV files for signals, surveys, and markers) is organized into subject-specific folders.
    * Each subject's data should be in its own sub-folder.
    * Inside each subject's folder, there should be `signals-e4-eda.csv`, `signals-e4-temp.csv`, `signals-e4-hr.csv`, `signals-e4-acc.csv`, `surveys.csv`, and `markers-phase2.csv`. (Adjust these filenames if your dataset uses different conventions).

3.  **Place Data and Configure `BASE_DIR`:**
    * Place the **root folder containing all your subject data** (e.g., `emoWear/csv_features/csv`) anywhere on your system.
    * **Crucially, update the `BASE_DIR` variable in your Jupyter Notebook (`model.ipynb` or equivalent) to correctly point to this root folder.**

    **Example `BASE_DIR` configurations:**

    * **If your data is in the same directory as your notebook (or a subfolder of it):**
        ```python
        # Assuming your 'model.ipynb' is in 'your_project_root/notebook/'
        # and your EmoWear data is in 'your_project_root/data/emoWear_processed/'
        BASE_DIR = "../data/emoWear_processed/"
        # Or if it's directly in 'your_project_root/emoWear_processed/'
        # BASE_DIR = "../../emoWear_processed/"
        ```

    * **Absolute path (Windows):**
        ```python
        BASE_DIR = "C:/Users/YourUser/Documents/EmoWear/csv_features/csv"
        # or if the path has spaces, use raw string or double backslashes
        # BASE_DIR = r"D:\My Documents\EmoWear Dataset\processed_csvs"
        # BASE_DIR = "D:\\My Documents\\EmoWear Dataset\\processed_csvs"
        ```

    * **Absolute path (macOS/Linux):**
        ```python
        BASE_DIR = "/home/youruser/datasets/emoWear/csv_features/csv"
        # or if the data is in your current user's Downloads folder
        # BASE_DIR = os.path.expanduser("~/Downloads/emoWear_data")
        ```

    * **Current code's example:**
        ```python
        BASE_DIR = "H:/emoWear/csv_features/csv"
        ```
    * **Verify:** After setting `BASE_DIR`, ensure that `os.path.join(BASE_DIR, "01-9TZK", "signals-e4-eda.csv")` (or a similar path to one of your subject's files) points to an existing file.

---

## How to Run

The entire analysis pipeline is contained within a single Jupyter Notebook.

1.  **Open the Main Notebook:** Open `model.ipynb` (or the name of your main analysis notebook) in Jupyter Lab or Jupyter Notebook.
2.  **Run Cells Sequentially:** Execute all cells in the notebook sequentially from top to bottom. 

---

## Notes

-   Ensure all necessary Python libraries (e.g., `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`) are installed in your environment.
-   The code utilizes `GroupKFold` for cross-validation, which is crucial for evaluating models on subject-independent data to avoid data leakage.
-   If you encounter any issues or have questions, feel free to open an issue or consult the provided code comments.

---

Thank you for using this project!