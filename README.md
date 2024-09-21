# Module 12 Report

## Overview of the Analysis

The purpose of this analysis is to train and a machine learning model based on loan risk. The model utilized a dataset of historical lending activiity from a peer-to-peer lending services company in order to identiify the creditworthiness of borrowers.

The dataset included variables such as loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatroy marks, and total debt. The purpose of the model was to predict loan status of either 0 (a healthly loan) or 1 (a high-risk loan).

The process of developing this model began with importing the data. Then, the variables were split from the target column (i.e., all aforementioned variables were split from loan status) to create the X variable (all variables) and the y variable (the target column: loan status). These variables were then split inito training and testing datasets using train_test_split. Once these steps were completed, then I created the logistic regression model. This model was created using the LogisticRegression module from SKLearn (see https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html#sklearn.linear_model.LogisticRegression for documentation). The model was then trained on the previously split training data, and then predictions were generated using the testing data.

## Results

* Model 1 Accuracy: 99%
* Precisions:
    * 0 - Healthly Loans: 100%
    * 1 - High-Risk Loans: 84%
* Recall Scores:
    * 0 - Healthly Loans: 99%
    * 1 - High-Risk Loans: 94%

## Summary

The model does a relatively good job in accurately identifying loan status. However, given the nature of the problem (identifying high-risk loans from healthly loans), this model may not be the best to use, as its resutls (precision and recall scores) in predicting high-risk loans is lower than that of healthly loans. It is more important to predict the 1s (high-risk loans), since that is where the most risk les.