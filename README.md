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
  
  ![validation_metrics](https://github.com/darigain/cc_fraud_detection/blob/f368f96b8182c353efaa7c9a0bc0e133891614f1/visuals/validation_metrics.png)
  - **Test Metrics**:
  
  ![test_metrics](https://github.com/darigain/cc_fraud_detection/blob/f368f96b8182c353efaa7c9a0bc0e133891614f1/visuals/test_metrics.png)


- **Visualizations**:
  - **Feature Importance**: Highlights which features contribute most to the model.
  ![Feature Importance](https://github.com/darigain/cc_fraud_detection/blob/64c793516a1fa5c97a3149f459f9c0bedc1010aa/visuals/feature_importance.png)
  - **Confusion Matrix**: Demonstrates the model's ability to detect fraudulent transactions.
  ![Confusion Matrix](https://github.com/darigain/cc_fraud_detection/blob/64c793516a1fa5c97a3149f459f9c0bedc1010aa/visuals/confusion_matrix.png)

---

## Key Learnings
- Data preprocessing and visualization using PySpark and Databricks.
- Training and evaluating machine learning models (Logistic Regression, Random Forest).
- Handling class imbalance in datasets.
- Using key evaluation metrics (ROC AUC, Precision, Recall, F1 Score).
