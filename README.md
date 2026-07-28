# Customer Churn Prediction & Retention Optimization

## Overview

This project develops an end-to-end machine learning pipeline to predict customer churn using the IBM Telco Customer Churn dataset. Multiple classification algorithms are evaluated and compared to identify the model that best balances predictive performance and generalization. The project also extends beyond prediction by proposing a budget-constrained customer retention strategy to maximize business value.

---

## Objectives

- Predict customers likely to churn.
- Compare multiple machine learning algorithms.
- Address class imbalance to improve minority class detection.
- Optimize customer retention under a fixed marketing budget.

---

## Dataset

- **Source:** IBM Telco Customer Churn Dataset
- **Task:** Binary Classification
- **Target Variable:** `Churn`

---

## Project Workflow

1. Exploratory Data Analysis (EDA)
2. Data Cleaning and Preprocessing
3. Feature Engineering
4. Class Imbalance Handling using SMOTE
5. Model Training and Evaluation
6. Model Comparison
7. Business-Oriented Retention Optimization

---

## Models Evaluated

- Logistic Regression
- Elastic Net Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

---

## Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

Since customer churn prediction is an imbalanced classification problem, greater emphasis was placed on **Recall** and **ROC-AUC** rather than overall Accuracy.

---

## Results

The best-performing model achieved:

- **ROC-AUC:** 0.84
- **Recall:** 79%
- Strong generalization on unseen test data

XGBoost demonstrated the best overall balance between predictive performance and robustness among the evaluated models.

---

## Retention Optimization

The predictive model was extended into a business decision framework by formulating a budget-constrained retention strategy.

Instead of targeting every customer predicted to churn, customers are ranked according to their expected business value, enabling marketing resources to be allocated where they maximize expected revenue saved under a fixed retention budget.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- imbalanced-learn

---

## Repository Structure

```
CustomerRetentionProject/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── eda.ipynb
│   └── modeling.ipynb
│
├── outputs/
│
├── src/
│
├── requirements.txt
└── README.md
```

---

## Future Improvements

- Hyperparameter optimization using GridSearchCV or Optuna
- Probability calibration
- SHAP-based model interpretability
- Deployment using FastAPI
- Interactive dashboard for churn analysis

---

## License

This project is intended for educational and portfolio purposes.
