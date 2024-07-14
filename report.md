# Module 20 Report

## Overview of the Analysis

  The purpose of the analysis was to identify the creditworthiness of borrowers by training and evaluating a machine learning model.  The financial data used to train and evaluate the model was from a peer-to-peer lending services company. It had 77,536 rows, 58,152 of which were used for training the model and 19,384 of which were used to test the model and included features like: 
  * loan size
  * interest rate
  * borrower income
  * debt to income
  * derogatory marks
  * total debt
  
  The goal was to predict whether the loan was healthy (low-risk) or non-healthy (high-risk) based on loan status provided by the lending company. 

  First the data was split into training and testing sets. Then the logistic regression model was used on the training set of data. Finally the Logistic Regression Model was applied to the testing dataset. The LogisticRegression library from scikit-learn was used to both train and test the model. In addition a confusion matrix and classification report were generated in order to evaluate the logistic regression model.
## Results

* Logistic Regression Model:
  * Accuracy: 99%
  * Precision: 94% (an average, precision was 100% for predicting low-risk loans and 87% for predicting high-risk   loans)
  * Recall: 94% (an average, precision was again 100% for predicting low-risk loans but was 89% for predicting high-risk loans)


## Summary

The logistic regression model while it predicts well for healthy loans, does a poor job at predicting high risk loans. Our model correctly predicted healthy loans 18,679 times. The model incorrectly predicted that healthy loans were actually unhealthy 80 times. The model correctly predicted that high risk loans were high risk 558 times. The model incorrectly predicted that the loan was low risk when it was actually high risk 67 times. Our model has not seen as many high risk examples and as a result poorly predicts high risk(1s) loans and accurately predicts low risk (healthy - 0s) loans.

I would not recommend using this model unless humans are involved in the decision making for high risk loans because as a company we wouldn't want to risk losing money on loans to high risk individuals who dont end up paying back the loans. In addition I would use a re-sampling technique which would allow us to try to optimize the model and predict the high risk loans at a better rate.

