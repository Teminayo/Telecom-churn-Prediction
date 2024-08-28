
# Telcom Customer Churn Prediction

This repository contains the analysis and model performance metrics for predicting customer churn using the Telco customer churn dataset. The model's performance metrics, key findings, and actionable insights are detailed below.

## Model Performance Metrics

### 1. Accuracy
**Value**: 0.9829666430092264  
**Definition**: Accuracy is the ratio of correctly predicted instances (both positive and negative) to the total instances.  
**Interpretation**: An accuracy of 0.9829666430092264 means that 98.30% of the predictions made by the model are correct, indicating that the model performs very well on this dataset.

### 2. ROC-AUC
**Value**: 0.9964618434093162  
**Definition**: ROC-AUC (Receiver Operating Characteristic - Area Under the Curve) measures the ability of the model to distinguish between classes. It plots the true positive rate against the false positive rate.  
**Interpretation**: A ROC-AUC score of 0.9964618434093162 indicates that the model is very good at distinguishing between churn and non-churn customers. The closer the score is to 1, the better the model is at making this distinction.

### 3. Classification Report
The classification report includes precision, recall, and F1-score for both classes (Non-Churn and Churn).

#### Precision
- **Class 0 (Non-Churn)**: 0.98
- **Class 1 (Churn)**: 0.99

#### Recall
- **Class 0 (Non-Churn)**: 1.00
- **Class 1 (Churn)**: 0.94

#### F1-Score
- **Class 0 (Non-Churn)**: 0.99
- **Class 1 (Churn)**: 0.97

#### Support
- **Class 0 (Non-Churn)**: 1009 instances
- **Class 1 (Churn)**: 400 instances

### Summary Metrics
- **Accuracy**: 0.98 (Overall accuracy of the model)
- **Macro Avg**:
  - Precision: 0.99
  - Recall: 0.97
  - F1-Score: 0.98
- **Weighted Avg**:
  - Precision: 0.98
  - Recall: 0.98
  - F1-Score: 0.98

**Interpretation**:
- **High Precision for Class 1**: The model correctly predicts churn 99% of the time.
- **High Recall for Class 0**: The model successfully identifies almost all non-churn customers.
- **F1-Score Balance**: The F1-scores of 0.99 for non-churn and 0.97 for churn indicate that the model balances precision and recall well.

Overall, these metrics suggest that the model performs exceptionally well, with high accuracy and excellent ability to distinguish between churn and non-churn customers. The precision, recall, and F1-scores also indicate that the model makes very few errors in its predictions.

## Principal Component Analysis (PCA) and Logistic Regression

In this analysis, Principal Component Analysis (PCA) was implemented to reduce dimensionality, followed by Logistic Regression to predict customer churn.

- **Maximum Accuracy**: Achieved with the first 25 features, with an accuracy of 0.9517.
- **Variance Explained**: Approximately 90% of variance is explained by the first 25 components.

## Key Findings

### Significant Features
- **Tenure Months**
- **Monthly Charges**
- **Total Charges**
- **Churn Score**
- **CLTV**

These features have very low p-values, indicating a strong association with churn behavior.

### Non-Significant Features
- **Zip Code**
- **Latitude**
- **Longitude**

These features have high p-values, indicating they are not significantly associated with churn.

## Explanation of Feature Importance

### 1. Churn Reason
**Importance**: Most significant factor in predicting churn.
**Action**: Address specific reasons for churn to improve retention.

### 2. Churn Score
**Importance**: Quantitative measure of the likelihood of churn.
**Action**: Use churn score to prioritize retention efforts.

### 3. Contract
**Importance**: Type of contract affects likelihood of churn.
**Action**: Encourage long-term contracts with incentives.

### 4. Tenure Months
**Importance**: Longer tenure decreases likelihood of churn.
**Action**: Focus on retention strategies for new customers.

### 5. Total Charges
**Importance**: High total charges can lead to dissatisfaction.
**Action**: Ensure billing transparency and offer rewards for long-term customers.

## Summary of Actions Based on Feature Importance

1. **Address Churn Reasons Directly**: Mitigate common reasons for churn.
2. **Utilize Churn Scores for Proactive Retention**: Implement tailored retention strategies for high-risk customers.
3. **Encourage Long-Term Contracts**: Provide incentives for longer-term contracts.
4. **Focus on New Customer Retention**: Develop onboarding and retention programs for new customers.
5. **Ensure Billing Transparency and Value**: Maintain transparency in billing and offer rewards for long-term customers.

By focusing on these key factors, a comprehensive strategy to reduce churn and improve overall customer retention can be developed.

