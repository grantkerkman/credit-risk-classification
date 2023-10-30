# Module 20 Report

## Overview of the Analysis

The purpose of this analysis was to predict loan statuses based on financial data using machine learning models. The dataset contained information on loan sizes, interest rates, borrower incomes, and various other features. The main objective was to predict whether a loan is high-risk or healthy based on the provided data.

### Labels Data Overview

The labels 'loan_status' were binary: 0 represented 'healthy loan', and 1 represented 'high-risk loan'. The `value_counts` function revealed an imbalanced dataset, with a majority of healthy loans (0) compared to high-risk loans (1).

The analysis proceeded through various stages: 
1. Data loading and exploration.
2. Creation of labels and features.
3. Checking the balance of the labels variable.
4. Creation of a Logistic Regression model using the original data.
5. Evaluation of the model's performance via accuracy, confusion matrix, and classification report.
6. Oversampling the training data to balance the labels.
7. Creating and evaluating a Logistic Regression model using the oversampled data.

## Results

### Machine Learning Model 1: Logistic Regression with Original Data
**Accuracy:** 99.18%

**Confusion Matrix:**
|            | Predicted 0 | Predicted 1 |
|------------|-------------|-------------|
| Actual 0   | 18663       | 102         |
| Actual 1   | 56          | 563         |

**Classification Report:** 
|             | Precision | Recall | F1-Score | Support |
|-------------|-----------|--------|----------|---------|
| healthy_loan| 1.00      | 0.99   | 1.00     | 18765   |
| high_risk_loan| 0.85     | 0.91   | 0.88     | 619     |
| Accuracy    |           |        |          | 0.99    |


### Machine Learning Model 2: Logistic Regression with Resampled Data
**Accuracy:** 99.38%

**Confusion Matrix:**
|             | Predicted 0 | Predicted 1 |
|-------------|-------------|-------------|
| Actual 0    | 18649       | 116         |
| Actual 1    | 4           | 615         |

**Classification Report:** 
|             | Precision | Recall | F1-Score | Support |
|-------------|-----------|--------|----------|---------|
| healthy_loan| 1.00      | 0.99   | 1.00     | 18765   |
| high_risk_loan| 0.84     | 0.99   | 0.91     | 619     |
| Accuracy    |           |        |          | 0.99    |


## Summary

The logistic regression models performed exceptionally well for both healthy and high-risk loans. However, the model trained with resampled data exhibited slightly better performance in predicting high-risk loans. If the focus is equally on predicting both classes, the resampled model might be preferable due to its higher recall for high-risk loans.

Performance depends on the problem at hand; in this case, correctly identifying high-risk loans might be of paramount importance. As both models performed well, the choice could depend on the emphasis on correctly identifying high-risk loans.

Therefore, it is recommended to utilize the model trained with the resampled data if balanced prediction of both healthy and high-risk loans is the primary concern.

