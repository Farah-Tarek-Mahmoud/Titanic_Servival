# Titanic Survival Prediction - README

## Project Overview
This project leverages the Titanic dataset to predict the likelihood of survival for passengers based on various features such as age, gender, passenger class, and more. The analysis combines data preprocessing, feature engineering, and machine learning to draw meaningful insights and create accurate predictive models.

---

### Key Features of the Dataset
- **Passenger Information**: Name, Age, Gender, Ticket Class.
- **Travel Details**: Fare, Cabin, Embarked Location.
- **Outcome**: Survival (1: Survived, 0: Did not survive).

---

## Project Workflow

### 1. Data Preprocessing
- **Handling Missing Values**:
  - Imputed missing `Age` values using median based on passenger class.
  - Replaced missing `Cabin` values with "Unknown" and engineered a cabin section feature.
  - Filled missing `Embarked` values with the most frequent port.
- **Feature Transformation**:
  - Converted categorical variables like `Sex` and `Embarked` into numerical values using one-hot encoding.

### 2. Feature Engineering
- Created new features such as:
  - **Family Size**: Combined `SibSp` and `Parch`.
  - **Title Extraction**: Extracted titles (e.g., Mr., Mrs.) from names to capture social hierarchy.

### 3. Model Training
- Models Used:
  - Logistic Regression
  - Random Forest Classifier
- **Cross-Validation**:
  - Employed **StratifiedKFold** to validate model performance across balanced subsets.

### 4. Addressing Class Imbalance
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to ensure equal representation of survival classes.

### 5. Model Evaluation
- Performance Metrics:
  - Accuracy
  - Precision, Recall, F1-Score
  - ROC-AUC Curve
- Outcome: Random Forest achieved the highest AUC score of ~0.87.

---

## Conclusion
This project highlights the importance of domain-specific feature engineering and handling class imbalance for robust predictive modeling. The combination of Logistic Regression and Random Forest provided actionable insights into survival probabilities.
