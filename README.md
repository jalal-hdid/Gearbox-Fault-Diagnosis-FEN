# Gearbox Fault Diagnosis using Feature Engineering and Machine Learning
Python implementation of the proposed feature engineering (FEN) and machine learning framework for gearbox fault diagnosis using vibration signals.

## Overview
This repository contains the complete implementation of the proposed framework developed for binary gearbox fault diagnosis under ten different operating load conditions (0%–90%). The methodology includes vibration signal processing, feature extraction, feature selection, stability analysis, redundancy filtering, and machine learning classification. The implementation corresponds to the workflow described in the research article:
"Feature Engineering and Machine Learning for Gearbox Fault Diagnosis and Classification"

## Repository Content
- `Gearbox_Fault_Diagnosis_FEN.ipynb`: Complete Google Colab notebook implementing the proposed methodology.

## Notebook Organization
The notebook is structured into the following main stages:

**Libraries importation**
   - Importing the necessary libraries and modules

**I. Data Splitting (75% Train / 25% Test)**
   - Loading raw vibration datasets
   - Training/hold-out testing separation
   - Data saving for subsequent processing

**II. Feature extraction and datasets preparation**
   - II-1. Raw data loading (Training and Testing)
   - II-2. Feature extraction function (using 13 time- and frequency-domain descriptors)
   - II-3. Raw data segmentation and feature extraction
   - II-4. Extracted data loading
   - II-5. Interleaving extracted data (parallel interleaved method)
   - II-6. Interleaving raw data (parallel interleaved method)

**III. Hyperparameter optimization and feature selection**
   - III-1. Interleaved datasets loading
   - III-2. Preprocessing: detecting and removing constant features (Variance = 0)
   - III-3. Pipeline and GridSearchCV-based cross-validation
   - III-4. Grid results and metrics displaying
   - III-5. Stability (Feature frequency voting)
   - III-6. Feature correlation (stable features filtering)

**IV. Statistical and frequency analysis of the raw vibration signals**
   - Raw vibration signals loading
   - Statistical and frequency-domain descriptor computation of raw signals (a1–a4)
   - Saving the results

**V. Final Machine Learning Classification**
   - V-1. Datasets loading
   - V-2. ML Prediction for raw and all extracted data (no feature selection)
   - V-3. ML Prediction for the selected, stable, and final retained features
   - V-4. Classification reports and confusion matrices results displaying

## Dataset Availability
The original gearbox vibration dataset used in this study is publicly available through Kaggle:

[Gearbox Fault Diagnosis Dataset](https://www.kaggle.com/datasets/brjapon/gearbox-fault-diagnosis)

https://www.kaggle.com/datasets/brjapon/gearbox-fault-diagnosis

## Requirements
The implementation requires Python 3 and the following libraries:

- numpy
- pandas
- scipy
- scikit-learn
- imbalanced-learn
- matplotlib
- seaborn

## How to Run
The notebook can be executed directly using Google Colab or a local Jupyter Notebook environment.
