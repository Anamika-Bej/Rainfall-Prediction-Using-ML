# Rainfall Prediction Using Machine Learning 🌧️

## 1. Project Overview

This project focuses on predicting next-day rainfall using historical weather data through Machine Learning techniques.

The problem is formulated as a supervised binary classification task. The model predicts whether rainfall will occur on the following day.

- **1 – Rain:** Rainfall is expected on the next day.
- **0 – No Rain:** Rainfall is not expected on the next day.

The project implements and compares different classification algorithms and identifies the most suitable model based on performance evaluation.

## 2. Objectives

- To analyse historical weather data.
- To perform data preprocessing and exploratory data analysis.
- To construct a next-day rainfall target variable.
- To perform feature engineering using historical weather observations.
- To implement and compare different Machine Learning algorithms.
- To optimize model performance through hyperparameter tuning.
- To evaluate the final model using appropriate classification metrics.

## 3. Dataset Description

**Dataset File:** `kolkata_weather_jan_june_2026.csv`

The dataset contains daily weather observations for Kolkata.

**Weather observation period:** 30 June 2021 – 30 June 2026.

**Total labelled observations:** 1,826

The dataset includes weather-related variables such as:

- Mean, maximum and minimum temperature
- Rainfall and precipitation
- Wind speed and wind gusts
- Wind direction
- Sunshine duration
- Weather code
- Precipitation hours

The target variable is constructed using the following day's rainfall information.

## 4. Technologies and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## 5. Machine Learning Algorithms

The following algorithms were implemented:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. Dummy Classifier (Baseline)

Random Forest was selected for further optimization and final evaluation.

## 6. Methodology

The project follows these major steps:

1. Data Collection
2. Data Preprocessing
3. Exploratory Data Analysis (EDA)
4. Target Variable Construction
5. Feature Engineering
6. Chronological Train-Test Splitting
7. Model Training and Comparison
8. Hyperparameter Tuning using GridSearchCV
9. Time-Series Cross-Validation
10. Final Model Evaluation
11. Next-Day Rainfall Prediction

### Feature Engineering

A total of 40 features were constructed, including:

- Cyclical month encoding
- Cyclical wind direction encoding
- Historical lag features (1, 2, 3 and 7 days)
- Rolling rainfall averages (3-day and 7-day windows)

### Data Splitting

The dataset was divided chronologically to preserve the temporal order of observations.

- Training samples: 1,454
- Testing samples: 364

## 7. Model Evaluation

The tuned Random Forest classifier achieved the following performance on the unseen test dataset:

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 90.66% |
| Precision | 89.81% |
| Recall | 94.17% |
| F1-Score | 91.94% |
| ROC-AUC | 96.32% |

The model was further evaluated using a confusion matrix, classification report and ROC curve.

### Cross-Validation

TimeSeriesSplit with three splits was used during model selection.

- Mean Cross-Validation Accuracy: 85.22%
- Mean Cross-Validation F1-Score: 0.8644

## 8. Hyperparameter Tuning

GridSearchCV was applied to optimize the Random Forest classifier.

The best parameters obtained were:

- `n_estimators = 100`
- `max_depth = 10`
- `max_features = sqrt`
- `min_samples_split = 2`
- `min_samples_leaf = 2`

## 9. Project Structure

```text
Rainfall-Prediction-Using-ML/
│
├── ML Project(Rainfall-Prediction-Using-ML).ipynb
├── README.md
└── kolkata_weather_jan_june_2026.csv
```

## 10. Future Scope

- Incorporating additional meteorological variables.
- Exploring advanced machine learning and deep learning algorithms.
- Extending rainfall prediction to multiple geographical locations.
- Predicting rainfall intensity and amount.
- Developing a user-friendly rainfall prediction application.

## 11. Conclusion

The project demonstrates the application of Machine Learning techniques for next-day rainfall prediction using historical weather observations.

Different classification algorithms were implemented and compared. Random Forest achieved the best overall test performance among the evaluated models, with an accuracy of 90.66% and an F1-score of 91.94%.

The study highlights the importance of feature engineering, chronological data splitting, cross-validation and hyperparameter optimization in developing a machine learning-based rainfall prediction system.

---

**Developed by:** Anamika Bej

**Registration Number:** B2530102
