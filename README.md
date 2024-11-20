# Credit Card Fraud Detection with PySpark and Databricks

This project demonstrates the use of PySpark and Databricks for detecting fraudulent credit card transactions. The goal is to identify fraudulent transactions (`Class = 1`) from non-fraudulent transactions (`Class = 0`) using machine learning models like Logistic Regression and Random Forest.

---

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Project Workflow](#project-workflow)
4. [Key Results](#key-results)
5. [Skills Demonstrated](#skills-demonstrated)

---

## Overview
- **Problem**: Fraudulent transactions pose a significant risk to financial institutions. This project predicts fraud using labeled transaction data.
- **Tools Used**: 
  - **PySpark**: Data preprocessing, model training, and evaluation.
  - **Databricks**: Collaborative platform for big data processing.
  - **Visualization Libraries**: Matplotlib and Seaborn for visualizations.

---

## Dataset
The dataset used is the [Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud), available on Kaggle.

- **Columns**:
  - `Time`: Seconds elapsed between the transaction and the first transaction in the dataset.
  - `Amount`: Transaction amount.
  - `Class`: Label (0 = non-fraudulent, 1 = fraudulent).
  - `V1` to `V28`: Principal components from PCA.

- **Class Distribution**:
  - Non-fraudulent transactions: 284,315
  - Fraudulent transactions: 492

---

## Project Workflow
1. **Data Preprocessing**:
   - Handled missing values (if any).
   - Scaled the `Amount` column.
   - Binned the `Time` column for visualization.
   - Split the data into training, validation, and test sets.

2. **Model Training**:
   - Trained **Logistic Regression** and **Random Forest** models using PySpark MLlib.
   - Used the training dataset for model fitting.

3. **Model Evaluation**:
   - Evaluated both models on the validation and test datasets.
   - Metrics: ROC AUC, Precision, Recall, and F1 Score.
   - Visualizations: ROC curve, feature importance, confusion matrix.

---

## Key Results
- **Random Forest** outperformed Logistic Regression:
  - **Validation Metrics**:
    - ROC AUC: 0.98
    - Precision: 0.78
    - Recall: 0.85
    - F1 Score: 0.81
  - **Test Metrics**:
    - ROC AUC: 0.97
    - Precision: 0.80
    - Recall: 0.88
    - F1 Score: 0.84

- **Visualizations**:
  - **Feature Importance**: Highlights which features (like `V17`, `V14`, `Amount`) contribute most to the model.
  - **Confusion Matrix**: Demonstrates the model's ability to detect fraudulent transactions.

---

## Skills Demonstrated
- Data preprocessing and visualization using PySpark and Databricks.
- Training and evaluating machine learning models (Logistic Regression, Random Forest).
- Handling class imbalance in datasets.
- Using key evaluation metrics (ROC AUC, Precision, Recall, F1 Score).
- Collaborative workflows with Databricks.
