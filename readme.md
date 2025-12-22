# Sleep Stage Classification Using Single-Channel EEG

## Project Title
Sleep Stage Classification Using Single-Channel EEG with Machine Learning and Deep Learning Models

---

## Overview
This project implements an **end-to-end sleep stage classification system** using **single-channel EEG data** stored in EDF (European Data Format) files. The system preprocesses raw EEG signals, extracts meaningful features, applies multiple **machine learning (ML)** and **deep learning (DL)** models, generates **sleep stage predictions**, and visualizes results using **hypnogram plots**.

The project is designed to work in **Google Colab**, making it easy to upload EEG files and run the complete pipeline without additional setup.

---

## Objectives
- To preprocess single-channel EEG data from EDF files
- To extract statistical and frequency-domain features from EEG epochs
- To implement and compare multiple ML and DL models
- To generate sleep stage predictions
- To visualize predicted sleep stages using hypnograms
- To compare model performance using graphs and charts

---

## Sleep Stages
The system predicts the following standard sleep stages:
- Wake (W)
- N1 (Light Sleep)
- N2 (Intermediate Sleep)
- N3 (Deep Sleep)
- REM (Rapid Eye Movement)

---

## Models Implemented
The following models are implemented and compared:

### Machine Learning Models
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest (RF)
- Decision Tree (DT)

### Deep Learning Models
- Deep Neural Network (DNN / MLP)
- Convolutional Neural Network (CNN)

---

## Dataset
- Input format: **EDF (European Data Format)**
- Signal type: **Single-channel EEG**
- Source example: Sleep-EDF dataset
- Labels:  
  - If hypnogram labels are unavailable, **pseudo-labels are generated using clustering** for demonstration and comparison purposes.

> Note: In real-world deployment, trained models would be used to predict sleep stages for unseen EEG data.

---

## System Workflow
1. Upload EEG EDF file in Google Colab
2. Load and select a single EEG channel
3. Band-pass filtering (0.3–35 Hz)
4. Segment EEG into 30-second epochs
5. Normalize epochs
6. Extract EEG features
7. Train ML and DL models
8. Generate sleep stage predictions
9. Plot hypnogram
10. Compare models using graphs

---

## Features Extracted
- Mean
- Standard deviation
- Skewness
- Kurtosis
- Delta band power (0.5–4 Hz)
- Theta band power (4–8 Hz)
- Alpha band power (8–13 Hz)
- Beta band power (13–30 Hz)

---

## Visualizations
- Predicted hypnogram for each model
- Accuracy comparison bar chart
- Model-wise prediction distribution
- Training time comparison (optional)

---

## Tools & Technologies Used
- Python
- Google Colab
- NumPy
- SciPy
- MNE-Python
- Scikit-learn
- PyTorch
- Matplotlib

---

## How to Run (Google Colab)

### Step 1: Install Dependencies
```bash
pip install mne scipy scikit-learn torch matplotlib
