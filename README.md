# Titanic-Survival-Prediction
Titanic Survival Prediction using Exploratory Data Analysis and Random Forest Classification


## Overview
This project analyzes the Titanic dataset and builds a machine learning model to predict passenger survival.

The project includes:
- Exploratory Data Analysis (EDA)
- Missing Value Handling
- Feature Engineering
- Outlier Removal
- Feature Selection
- Random Forest Classification
- Model Evaluation using Accuracy, F1 Score, Precision, and Confusion Matrix

Dataset: Titanic - Machine Learning from Disaster (Kaggle)

---

## Dataset Information

### Training Data
- 891 passengers
- 12 features

### Test Data
- 418 passengers
- 11 features

Target Variable:
- Survived
  - 0 = Did Not Survive
  - 1 = Survived

---

## Exploratory Data Analysis

The following factors were analyzed:

- Passenger Class (Pclass)
- Gender (Sex)
- Age
- Fare
- Embarkation Port
- Number of Siblings/Spouses (SibSp)

### Key Observations

- First-class passengers had higher survival rates.
- Female passengers survived significantly more often than male passengers.
- Higher ticket fares were generally associated with better survival chances.
- Passengers with fewer family members onboard had better survival probabilities.

---

## Data Preprocessing

### Missing Value Handling

Columns containing missing values:
- Age
- Embarked
- Cabin

Approach:
- Cabin column removed due to a large percentage of missing values.
- Missing Age values imputed using Iterative Imputer and Random Forest Regression.
- Missing Embarked values imputed using Random Forest Classification.

### Outlier Handling

Removed:
- Age > 70
- Fare > 500

---

## Feature Selection

Removed features:
- Name
- Ticket
- AgeGroup

Selected features:
- Pclass
- Sex
- Age
- SibSp
- Parch
- Fare
- Embarked

Categorical features were encoded using Label Encoding.

---

## Machine Learning Model

### Random Forest Classifier

Hyperparameter tuning was performed using GridSearchCV.

Parameters:
- n_estimators = [100, 200, 300]
- max_depth = [10, 20, 30]

Pipeline:
- MinMaxScaler
- RandomForestClassifier

---

## Model Performance

### Evaluation Metrics

| Metric | Score |
|----------|----------|
| Accuracy | 82.98% |
| F1 Score | 0.76 |
| Precision | 0.84 |

### Confusion Matrix


[[79 7]
[17 38]]


---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-Learn

---

## Future Improvements

- XGBoost Implementation
- Feature Engineering Enhancements
- Cross Validation Improvements
- Model Deployment using Streamlit

---

## Author

Vyshnave Talabattula

B.Tech CSE (AI & ML)

Interested in Machine Learning, Data Science, and Artificial Intelligence.
