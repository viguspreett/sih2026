# AI-Based Gait Analysis for Knee Osteoarthritis Detection

## Overview

This project aims to detect Knee Osteoarthritis (KOA) from gait videos using computer vision and machine learning.

Human gait contains subtle biomechanical patterns that can indicate joint abnormalities. By extracting body landmarks from walking videos and engineering gait-related features, this system classifies subjects as:

- KOA (Knee Osteoarthritis)
- NM (Normal)

The project was developed as part of Smart India Hackathon (SIH) 2026.

---

## Problem Statement

Traditional diagnosis of Knee Osteoarthritis often requires clinical examination and imaging techniques such as X-rays or MRI scans.

This project explores a non-invasive alternative by analyzing walking patterns from videos and identifying gait characteristics associated with KOA.

---

## Installation

```bash
git clone https://github.com/viguspreett/sih2026.git
cd sih2026
pip install -r requirements.txt
```

## Dataset

**KOA-PD-NM Gait Dataset**

Source:
https://data.mendeley.com/datasets/44pfnysy89/1

The dataset contains gait videos from Knee Osteoarthritis (KOA) and Normal (NM) subjects and is used for feature extraction and classification in this
 project.

> Note: The dataset is not included in this repository due to size and licensing considerations. Please download it from the official source.

## Methodology

### 1. Video Processing

- OpenCV used for video handling
- Frame-by-frame processing

### 2. Pose Estimation

- MediaPipe Pose used to extract body landmarks
- Key joints tracked:
  - Hip
  - Knee
  - Ankle

### 3. Feature Engineering

A total of 25 gait features were extracted, including:

- Hip motion range
- Knee motion range
- Ankle motion range
- Joint variability
- Horizontal movement patterns
- Pose detection reliability metrics

### 4. Machine Learning Models

The following classifiers were trained and evaluated:

- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest

### 5. Evaluation

Subject-level train-test splitting was used to reduce data leakage.

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1 Score

---


### Current Best Experimental Result

**Logistic Regression**

Accuracy: **81.25%**

---

## Project Structure

```text
sih2026/
│
├── Gait.ipynb
├── README.md
├── results/
│   ├── final_model_results.csv
│   └── reproducibility_results.csv
│
└── models/
```

---

## Technologies Used

- Python
- Google Colab
- OpenCV
- MediaPipe
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## Future Improvements

- Improved gait feature engineering
- Hyperparameter tuning
- Deep learning approaches
- Real-time gait analysis
- Multi-class severity prediction
- Clinical deployment pipeline

---

## Authors

Developed for Smart India Hackathon (SIH) 2026.


---

## License

This project is intended for academic and research purposes.
