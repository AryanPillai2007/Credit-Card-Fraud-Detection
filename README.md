# Credit Card Fraud Detection

The primary goal of this project is to develop a comprehensive fraud detection system that enhances the security and trustworthiness of financial transactions. 


![GitHub](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/Python-3.12.0-green)

## Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The dataset used is highly imbalanced, with a very small percentage of transactions being fraudulent. The goal is to build a model that can accurately identify these fraudulent transactions.

## Dataset

The dataset contains transactions made by credit cards in September 2013 by European cardholders. It includes 284,807 transactions, with 492 of them being fraudulent. The dataset is highly imbalanced, with frauds accounting for only 0.17% of all transactions.

### Features

- **Time**: Number of seconds elapsed between this transaction and the first transaction in the dataset.
- **Amount**: Transaction amount.
- **V1-V28**: Principal components obtained with PCA (due to confidentiality issues, the original features are not provided).
- **Class**: Target variable, where 1 indicates fraud and 0 indicates no fraud.

## Project Structure

1. **Data Exploration and Visualization**:
   - Class distribution analysis.
   - Transaction amount and time distribution.
   - Correlation matrix for imbalanced and balanced datasets.

2. **Data Preprocessing**:
   - Scaling of the 'Amount' and 'Time' features using `RobustScaler`.
   - Handling class imbalance by creating a balanced subsample.
   - Outlier removal for features with high negative correlation to the target variable.

3. **Model Training and Evaluation**:
   - Training multiple classifiers including Logistic Regression, K-Nearest Neighbors, Support Vector Classifier, and Decision Tree.
   - Cross-validation and hyperparameter tuning using `GridSearchCV`.
   - Evaluation of models using ROC-AUC score, precision, recall, and F1-score.

4. **Visualization of Results**:
   - Learning curves for different models.
   - ROC curves for model comparison.
   - Confusion matrix for final model evaluation.

## Key Findings

- The dataset is highly imbalanced, with frauds accounting for only 0.17% of transactions.
- Features like V14, V12, and V10 have high negative correlations with the target variable and were used for outlier removal.
- Logistic Regression and Support Vector Classifier performed the best with an ROC-AUC score of around 0.97.
- The final model achieved a sensitivity (true positive rate) of 88.89% and a specificity of 96.97%.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/AryanPillai2007/Credit-Card-Fraud-Detection.git
   cd credit-card-fraud-detection
