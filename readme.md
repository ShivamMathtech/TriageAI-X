# TriageAI-X
## AI-Based Emergency Department Triage Prediction System

---

# Problem Statement

Emergency departments are often overcrowded and understaffed. Doctors and triage nurses must quickly decide which patients need urgent treatment. Incorrect triage decisions can lead to delayed care, severe complications, or even death.

Traditional triage systems mainly depend on human judgment, which may vary between clinicians. The goal of this project is to develop an AI-powered triage assistance system that can predict patient acuity levels using clinical data and chief complaint text.

The proposed system aims to:
- improve triage accuracy,
- identify high-risk patients earlier,
- reduce undertriage,
- and provide interpretable AI-based clinical support.

---

# Dataset Used

The project uses the synthetic emergency department triage dataset provided in the Triagegeist Hackathon.

## Dataset Files

| File Name | Description |
|---|---|
| train.csv | Training data with triage labels |
| test.csv | Test dataset without labels |
| chief_complaints.csv | Free-text patient complaints |
| patient_history.csv | Patient comorbidity information |
| sample_submission.csv | Submission format |

---

# Features Used

## Clinical Features
- Age
- Sex
- Blood Pressure
- Heart Rate
- Respiratory Rate
- Temperature
- Oxygen Saturation
- Glasgow Coma Scale
- Pain Score

## Historical Features
- Prior ED visits
- Prior admissions
- Comorbidities

## Text Features
- Chief complaint narratives

---

# Proposed Solution

The system combines:
- Machine Learning
- Natural Language Processing (NLP)
- Explainable AI

to predict emergency triage acuity levels.

---

# Methodology

## Step 1 — Data Collection
Load and merge all dataset files using `patient_id`.

---

## Step 2 — Data Preprocessing
- Handle missing values
- Encode categorical variables
- Clean text complaints
- Normalize numerical features

---

## Step 3 — Feature Engineering
Generate medical features such as:
- Shock Index
- Pulse Pressure
- Fever indicator
- Hypoxia indicator

---

## Step 4 — NLP Processing
Process chief complaints using:
- TF-IDF Vectorization
- Text cleaning
- Risk phrase extraction

---

## Step 5 — Model Training
Train machine learning models such as:
- LightGBM
- CatBoost
- XGBoost

---

## Step 6 — Explainable AI
Use SHAP to explain:
- important features,
- prediction confidence,
- patient risk factors.

---

## Step 7 — Fairness Analysis
Analyze model performance across:
- age groups,
- sex,
- language groups.

---

# Implementation

The project is implemented using:
- Python
- VS Code
- Jupyter Notebook

## Libraries Used

```python
pandas
numpy
scikit-learn
lightgbm
xgboost
catboost
shap
matplotlib
plotly
nltk