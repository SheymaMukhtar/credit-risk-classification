# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
The analysis aims to develop and evaluate machine learning models to predict the likelihood of a loan being high-risk (denoted by 1) or healthy (denoted by 0). This is crucial for financial institutions to manage credit risk effectively.

Financial Information:
The dataset consists of financial data related to loans, including variables such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.

Variables to Predict:
The primary variable to predict is loan_status, where 0 indicates a healthy loan and 1 indicates a high-risk loan. Below is the distribution of the target variable:

python
Copy code
df['loan_status'].value_counts()
Machine Learning Process Stages:

Data Reading and Preprocessing:
Loading the dataset and examining its structure.
Splitting Data:
Dividing the data into training and testing sets.
Model Training:
Training a Logistic Regression model on the training data.
Model Evaluation:
Evaluating the model using metrics such as balanced accuracy, precision, recall, and generating a confusion matrix.
Methods Used:

Logistic Regression was used as the primary algorithm for this classification task.
Results
Machine Learning Model 1: Logistic Regression

Accuracy: The balanced accuracy score of the model is approximately 95.20%.
Precision and Recall:
For class 0 (healthy loan):
Precision: 1.00
Recall: 0.99
F1-score: 1.00
For class 1 (high-risk loan):
Precision: 0.85
Recall: 0.91
F1-score: 0.88
Confusion Matrix:
True Positives: 563
True Negatives: 18663
False Positives: 102
False Negatives: 56

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Model Performance:

The Logistic Regression model performs exceptionally well, achieving a balanced accuracy score of over 95%.
The precision and recall scores indicate that the model is highly effective at identifying both healthy and high-risk loans, with particularly strong performance on healthy loans (class 0).
Recommendation:

The Logistic Regression model is recommended for this task due to its high accuracy and balanced performance across both classes.
Depending on the business requirement, if predicting high-risk loans (1s) is more critical, focus on recall for class 1. The current model shows good performance in this aspect with a recall of 0.91, indicating it correctly identifies 91% of high-risk loans.








