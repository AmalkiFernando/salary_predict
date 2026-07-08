# 💼 Salary Prediction Using Linear Regression

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange?logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 📌 Project Overview

This project develops **Linear Regression** models to predict employee salaries based on demographic and professional information.

Two models were trained and evaluated:

- **Single Feature Linear Regression** (Years of Experience only)
- **Multiple Feature Linear Regression** (All available features)

The project includes:

- Data preprocessing
- Feature engineering
- Model training
- Model evaluation
- Model comparison
- Saving the best-performing model for future predictions

---

## 📂 Dataset

| Property | Details |
|----------|----------|
| Dataset | Salary_Data.csv |
| Target Variable | `Salary` |
| Missing Values | Removed before training |

## Features

| Feature | Type | Description |
|----------|------|-------------|
| `Age` | Numeric | Employee age |
| `Gender` | Categorical | Encoded using Label Encoding |
| `Education Level` | Categorical | Employee education |
| `Job Title` | Categorical | Employee occupation |
| `Years of Experience` | Numeric | Total years of experience |
| `Salary` | Numeric | **Target variable** |

---

## 🛠 Technologies Used

| Library | Purpose |
|----------|----------|
| `pandas` | Data loading & preprocessing |
| `numpy` | Numerical operations |
| `matplotlib` | Data visualization |
| `seaborn` | Statistical visualization |
| `scikit-learn` | Machine learning pipeline |
| `joblib` | Save trained models |

---

## 🤖 Machine Learning Model

Two models were developed.

### Model 1
**Single Feature Linear Regression**

Input Feature: Years of Experience

### Model 2
**Multiple Feature Linear Regression**

Input Features:

- Age
- Gender
- Education Level
- Job Title
- Years of Experience
- Engineered Features

---

## ⚙️ Data Processing Pipeline

1. Load dataset
2. Remove missing values
3. Encode categorical variables
4. Create engineered features
5. Split dataset (80% Training / 20% Testing)
6. Standardize features using StandardScaler
7. Train Linear Regression models

---

## 🔧 Feature Engineering

Three additional features were created.

```text
Experience_Squared   = Years of Experience²
Age_Experience_Ratio = Age / (Years of Experience + 1)
Age_Experience       = Age × Years of Experience
```

These engineered features were added to determine whether they could improve prediction performance.

---

## 📊 Evaluation Metrics

The models were evaluated using:

| Metric | Description |
|----------|-------------|
| **RMSE** | Root Mean Squared Error |
| **R² Score** | Coefficient of Determination |

---

## 📈 Model Performance

| Model | RMSE | R² Score |
|------|-------:|---------:|
| ✅ Single Feature Linear Regression | **15,551.04** | **0.8991** |
| Multiple Feature Linear Regression | 16,873.18 | 0.8813 |

---

## 🎯 Key Findings

- The **Single Feature Linear Regression** model achieved the best performance.
- **Years of Experience** alone is a strong predictor of employee salary.
- The model explains approximately **90% of the variance** in salary values (R² ≈ 0.90).
- Adding additional variables slightly reduced prediction accuracy.
- The best-performing model was saved using **Joblib** for future predictions.

---

## 📊 Sample Predictions

| Actual Salary | Predicted Salary |
|---------------:|----------------:|
| 95,000 | 92,843 |
| 120,000 | 118,701 |
| 75,000 | 78,214 |

*(Example predictions from the trained model.)*

---

## 📁 Project Structure

```
salary-prediction/
│
├── notebook.ipynb          # Main Jupyter Notebook
├── Salary_Data.csv         # Dataset
├── salary_model.pkl        # Saved trained model
├── salary_scaler.pkl       # Saved StandardScaler
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## 👩‍💻 Author

**Amalki Fernando**
BSc (Hons) in IT Specialising in Artificial Intelligence
[SLIIT] — [2026]