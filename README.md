# 🫀 Heart Disease - Data Cleaning, Preprocessing & EDA

This repository contains the **data preparation phase** of a Heart Disease Prediction project.

Currently completed:
- ✅ Data Cleaning
- ✅ Data Preprocessing
- ✅ Exploratory Data Analysis (EDA)
- ⏳ Model Training — Planned for Future

---

## 📌 Project Objective

The goal of this project is to prepare a heart disease dataset for machine learning
and later build a predictive model to classify whether a patient has heart disease or not.

**Target Column:** `has_heart_disease`

| Value | Meaning |
|-------|---------|
| 0 | No Heart Disease |
| 1 | Has Heart Disease |

---

## 📁 Repository Structure

├── README.md
├── heart_disease_risk_2026.csv # Original raw dataset
├── heart_disease_cleaned.csv # Cleaned & preprocessed dataset
└── heart_disease_analysis.ipynb # Jupyter Notebook (cleaning + EDA)


---

## 📄 Files Description

| File | Description |
|------|-------------|
| `heart_disease_risk_2026.csv` | Original raw dataset before any preprocessing |
| `heart_disease_cleaned.csv` | Final cleaned dataset ready for model training |
| `heart_disease_analysis.ipynb` | Complete Jupyter Notebook containing data cleaning, preprocessing, and EDA |

---

## 🔧 Data Preprocessing Steps

The following steps were performed in `heart_disease_analysis.ipynb`:

### Column Conversions
| Original Column | New Column Name | Encoding |
|-----------------|----------------|----------|
| `sex` | `is_male` | Male = 1, Female = 0 |
| `family_history` | `has_family_history` | True = 1, False = 0 |
| `wearable_owner` | `has_wearable` | True = 1, False = 0 |
| `exercise_induced_angina` | `has_exercise_induced_angina` | True = 1, False = 0 |

### Categorical Encoding (One-Hot)
| Original Column | New Columns Created |
|-----------------|-------------------|
| `chest_pain_type` | `cp_asymptomatic`, `cp_atypical_angina`, `cp_non_anginal_pain`, `cp_typical_angina` |
| `smoker_status` | `smoker_status_Former`, `smoker_status_Never` |

### Other Steps
- Removed `patient_id` column
- Handled `bmi_category` column
- Verified no null values exist
- Ensured all columns are numeric (int / float)

---

## 📊 Exploratory Data Analysis (EDA)

The following visualizations were created:

- 📌 Heart Disease distribution (target variable)
- 🔥 Correlation heatmap
- 📈 Feature correlation with heart disease
- 👤 Age distribution by heart disease
- ⚖️ BMI distribution by heart disease
- 🚻 Gender vs Heart Disease
- 💔 Chest Pain Types vs Heart Disease
- 😰 Stress Score vs Heart Disease
- 🏃 Exercise Minutes vs Heart Disease
- 🔗 Feature relationship scatter plots

---

## 📋 Final Dataset Overview (`heart_disease_cleaned.csv`)

| # | Column | Type |
|---|--------|------|
| 1 | age | int |
| 2 | is_male | int |
| 3 | resting_bp_systolic | int |
| 4 | resting_bp_diastolic | int |
| 5 | cholesterol_total | int |
| 6 | hdl | int |
| 7 | ldl | int |
| 8 | triglycerides | int |
| 9 | fasting_blood_sugar | int |
| 10 | hba1c | float |
| 11 | bmi | float |
| 12 | resting_heart_rate | int |
| 13 | max_heart_rate_achieved | int |
| 14 | has_exercise_induced_angina | int |
| 15 | st_depression | float |
| 16 | has_family_history | int |
| 17 | alcohol_units_per_week | float |
| 18 | exercise_minutes_per_week | int |
| 19 | sleep_hours | float |
| 20 | stress_score | float |
| 21 | has_wearable | int |
| 22 | daily_steps | int |
| 23 | diet_quality_score | float |
| 24 | has_heart_disease | int |
| 25 | smoker_status_Former | int |
| 26 | smoker_status_Never | int |
| 27 | cp_asymptomatic | int |
| 28 | cp_atypical_angina | int |
| 29 | cp_non_anginal_pain | int |
| 30 | cp_typical_angina | int |

**Total Rows:** 9000  
**Total Columns:** 30  
**Missing Values:** None

---

## 🔮 Future Work

In the next phase, this project will include:

- [ ] Train-Test Split
- [ ] Feature Scaling (StandardScaler)
- [ ] Model Training
  - Logistic Regression
  - Random Forest
  - Decision Tree
  - XGBoost
- [ ] Model Evaluation (Accuracy, ROC-AUC, Confusion Matrix)
- [ ] Best Model Selection
- [ ] Model Saving / Deployment

---

## 🛠️ Technologies Used

| Technology | Purpose |
|-----------|---------|
| Python | Programming Language |
| Pandas | Data Manipulation |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| Seaborn | Statistical Visualization |
| Jupyter Notebook | Interactive Development |

---

## 🚀 How to Use

1. Clone this repository:
```bash
git clone https://github.com/zeeshan2007/ML-Project-Heart-Disease-Data-Cleaned-.git
Install dependencies:
Bash

pip install pandas numpy matplotlib seaborn scikit-learn jupyter
Open and run the notebook:
Bash

jupyter notebook heart_disease_analysis.ipynb
📝 Notes
This repository currently focuses only on data preparation and analysis
Model training is not included yet
The cleaned dataset (heart_disease_cleaned.csv) is ready for future ML experiments
Original dataset (heart_disease_risk_2026.csv) is preserved for reference
👤 Author
Zeeshan Shaukat
