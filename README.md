# credit-risk-classification
Module 20 Challenge
PLEASE VIEW REPORT IN 'RAW' VIEW MODE - NOTES ARE CORRECTLY OUTLINED AND STRUCTURED IN A CLEAR READABLE FORMAT. THANK YOU!

# Module 20 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

1.) The purpose of this analysis is to develop a method/model to accurately and correctly identifies low-risk loans vs high-risk loans, using historical data
    from prior loans.
2.) The financial information the data was on, or used, was historical data from a peer-to-peer lending services company that had the total loan amount,
    interest rate of the loan, income of the borrower, debt to income ratio, number of accounts, derogatory marks, borrowers’ total debit, and a loan status binary
    indicator, 0 for low-risk and 1 for high-risk. All of the listed data was used for prediction, using the numerical values to establish train and test groups, insuring
    that the different train and test groups were evenly distributed by using stratify.
3.) The basic information about the variables that I was attempting to predict are:
	  Total value counts for each class
  	The precision, recall, f1-score, support, and accuracy for each class
  	Correctly identifying whether the loans in the test samples were low-risk or high-risk.
4.) The stages of the machine learning process I went through as part of this analysis are as follows:
	1.) Import the data and create a dataframe using Pandas.
	2.) Establish the 'loan_status' column as the y-variable, and all other columns the x-variable, remembering to drop 'loan_status' from the x-variable.
	3.) Establish the various training and testing groups: a training and test groups for the x-variable, and training and test groups for the y-variable.
	4.) Using the Logistic Regression model, establishing a random_state for consistency and then fitting the training models to the newly established Logistic Regression module.
	5.) Reviewing the testing data scores for both the x-variable and y-variable training sets.
	6.) Creating a prediction from the test samples using the .predict() method.
	7.) Evaluate the model's performance using the Confusion Matrix.
	8.) Evaluate the model's performance using the Classification Report, allowing for an easy-to-read report that clearly shows the precision, recall, f1-score, support (value count), accuracy, macro average, and weighted average.
5.) The methods used are:
	  Test Train Split
  	Logistic Regression
  	Confusion Matrix
  	Classification Report

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

Machine Learning Model - Logistic Regression

•	Precision
  o	Healthy Loan: 1.00 - The module is showing that it accurately predicts Healthy Loans when comparing the ration of correctly predicted positive observations to total predicted positive observations 100% of the time.
  o	High-Risk Loan 0.87 - The module is showing that it accurately predicts High-Risk Loans when comparing the ration of correctly predicted positive observations to total predicted positive observations 87% of the time.
•	Recall
  o	Healthy Loan: 1.00 - The module is showing that it correctly predictive positive observations in comparison to all predicted positive observations for Healthy Loans at 100%.
  o	High-Risk Loan: 0.89 - The module is showing that it correctly predictive positive observations in comparison to all predicted positive observations for High-Risk Loans at 89%.
•	F1-score
  o	Healthy Loan: 1.00 - The module is showing the balance between precision and recall is 100%.
  o	High-Risk Loan: .88 - The module is showing the balance between precision and recall is 88%.

•	Accuracy - The module is showing that it is accuracy score is 99%, showing that we have a high ration of correctly prediction observations to the total value count of observations.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any:


After processing the Logistic Regression model, it appears to process quite well. Overall the accuracy is high, but the f1-score allows to see that we have a healthy balance between the precision and recall for both classes. The high precision and recall values show that we have a low false negative rate which is a desired outcome. The performance does depend on the type of problem we're attempting to solve. In this scenario, we are attempting to identify potentially High-Risk loans based on historical data of Healthy and High Risk Loans. Based on this, it is more important to predict 1s to flag and review loans that have the potential for loss. I would suggest a Logistical Regression module for this task/scenario.
