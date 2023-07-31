# credit-risk-classification
 Module 20 Challenge
 Machine learning techniques have been used to analyze a dataset of historical lending activity from a peer-to-peer lending services company. This, in turn,  built a model that can identify the creditworthiness of borrowers.

 ## Overview of the Analysis
 Factors considered in the analysis included data on:
* the size of the loan
* its interest rate
* the borrower's income
* the debt to income ratio
* the number of accounts the borrower held
* derogatory marks against the borrower
* the total debt

The dataset (77,536 data points) is divided into training and test sets. The training set is used to build the initial logistic regression model (Logistic Regression Model 1) using the scikit-learning “LogisticRegression” module. Logistic regression model 1 was then applied to the test data set. The purpose of the model is to determine whether a loan to a borrower in the test set would be low or high risk, and the results are summarized below. 

This initial model is based on a dataset containing 75,036 data points for low-risk loans and 2,500 data points for high-risk loans. To resample the training data and ensure that the logistic regression model has an equal number of data points, the training set data is resampled with the `RandomOverSampler` module from <a href=https://imbalanced-learn.org/dev/index.html>imbalanced-learn</a>. This generates 56,277 data points for low-risk (0) and high-risk (1) loans, based on the original dataset. 

The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). The objective of Logistic Regression Model 2 is to determine whether a loan to a borrower in the test set will be low risk or high risk. The results are summarized below. 

## Results

<strong>Logistic Regression Model 1:</strong>

* Precision: 93% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans)
* Accuracy: 94% 
* Recall: 95% (an average--the model had 100% recall in predicting low-risk loans, but 89% recall in predicting high-risk loans)

<strong>Logistic Regression Model 2:</strong>

* Precision: 93% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans)
* Accuracy: 100% 
* Recall: 100%

## Summary

Logistic Regression Model 2 is less likely to predict false negative results. However, based on the confusion matrices for each model, Logistic Regression Model 2 predicted slightly more false positives (low-risk when the actual was high-risk). 

If the goal of the model is to determine the probabilities of high-risk loans, neither model will achieve greater than 90% accuracy. Logistic Regression Model 2 has fewer false predictions about the testing data population as a whole and would be the best model to use based on its high accuracy and recall ability. 
