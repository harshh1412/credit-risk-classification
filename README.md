# credit-risk-classification

## Overview of the Analysis

* Purpose of the analysis:
 To build a model that can identify the creditworthiness of borrowers.

* What financial information the data was on, and what I need to predict:
I have used a dataset of historical lending activity from a peer-to-peer lending services company to predict the creditworthiness of borrowers.

* Basic information about the variables I am trying to predict:
A value of 0 meaning that the loan is healthy; A value of 1 meaning that the loan has a high risk of defaulting.

* The stages of the machine learning process:
1. Split the Data into Training and Testing Sets.
2. Create a Logistic Regression Model with the Original Data.
3. Evaluate the model’s performance using confusion matrix and classification report.

* Methods used - `LogisticRegression` - Logistic regression is a statistical method for predicting binary outcomes from data. (In our case - whether the loan application is healthy or risky)

## Results

- Accuracy: (True Positives + True Negatives)/Total Predictions.
Our model has the accuracy of 99% which means our model is correct 99% of the time. But accuracy can be very susceptible to imbalanced classes.

- Precision: Correct Predictions/Total Predictions for each class.
Our model generates a precision of almost 100% (14926/(14926+46)) for the `0` (healthy loan) labels but only 86% (461/(461+75)) for the `1` (high-risk loan) labels.

- Recall: Correct Predictions/Total Actual Values for each class.
Our model generates a recall of almost 100% (14926/(14926+75)) for the `0` (healthy loan) labels but only 91% (461/(461+46)) for the `1` (high-risk loan) labels.

## Summary

Conclusion: Although the model is good at predicting the creditworthiness of borrowers, it is nowhere near perfect as the precision and recall scores for the `1` (high-risk loan) labels are lower than expected. This means our model, if deployed, can possibly reject a good loan application and we might lose that particular customer.