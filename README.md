# credit-risk-classification
Challenge 20

# Module 12 Report 

## Overview of the Analysis

This Challenge uses various techniques to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company is used to build a model that can identify the creditworthiness of borrowers.

The learning model was based on financial data including the following features:

-  the size of the loan
-  the interest rate of the loan
-  the income of the borrower
-  the ratio of the borrower's debt-to-income
-  the number of accounts of the borrower
-  any financial derogatory marks
-  the total debt of the borrower

The variable "loan_status" indicates if the loan is healthy (loan_status = "0") or high_risk (loan_statu = "1").

The data set consists of 75036 healthy loans (96.8% of the data set) and 2500 unhealthy loans (3.2% of the data set).

The following steps describe the methodology of the model training and testing:

- After reading the lending data csv into a dataframe, the labels set (y) from the loan status column is created. 
- The features (X) are created from the remaining columns.
- Using train_test_split from sklearn, the data is split into training and testing samples.
- The regression model is fitted by using the training data ("X_train and y_train).
- The predictions on the testing data by using the testing feature data and the fitted model are saved.
- Finally, evaluation the model's performanceis done using a confusion matrix and a classification table.

The LogisticRegression model was used for this analysis.

## Results

  - Accuracy: 0.992 

      The regression model has a very high overall accuracy score at over 0.992, meaning the model correctly predicts the loan classification of healthy ("0") or high-risk ("1") over 99% of the time. 

  - Precision of a healthy loan: 1.00
  - Recall of a healthy loan: 0.99

      When observing the precision and recall scores, it can be see that when the regression model predicts a loan as healthy, it is correct 100% (precision score) of the time, and correctly identifies healthy loans 99% (recall score) of the time.

  - Precision of a high-risk loan: 0.84
  - Recall of a high-risk loan: 0.94

      When the model predicts a loan as high-risk, it is correct only 84% (precision score) of the time, and correctly identifies healthy loans 94% (recall score) of the time.


## Summary

When determining loan risk, it is important to observe the healthy loans and the high-risk loans. However, it is a priority to identify those loans that are high-risk in order to minimize financial loss through payment fault. Since this model can identify only 84% of high-risk loans, it is not recommended. However, it may serve well as an initial parsing of borrowers, followed by a more rigorous evaluation.

