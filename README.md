# Module 12 Report Template

## Overview of the Analysis

The purpose of this repository is to train and evaluate a supervised Machine Learning Model for the classification of loan risk based on financial data such as borrower income, interest rate, loan size, etc... 

The dataset contains the information for 77,536 borrowers, and it is alredy labeled, with 75,036 cases of "healthy loan" `0` and 2500 cases of "high-risk loan" `1`.

A logistic regression model was used given that the outcome we want to predict is binary, either it is a "healthy loan" or a "high-risk loan", to be able to evaluate the model the data was split into train data and test data, the train data was used to fit the model and then some metrics were calculated using the test data.

It was necessary to train a second version of the model given that the cases for "high-risk loan" scenarios were too few, to correct this the oversampler method was used in the train dataset, the model was retrained with this data and the metrics were calculated again obtaining better results with this version of the model


## Results

* Machine Learning Model 1:
  * Balanced accuracy score: 95.2%
  * Confusion matrix:

    |         | Predicted `0` | Predicted `1` |
    |---------|-------------|-------------|
    | Actual `0`|    18663    |     102     |
    | Actual `1`|     56      |     563     |
  
  * Classification report:

    |           | Precision | Recall | F1-Score | Support |
    |-----------|-----------|--------|----------|---------|
    | Class `0`   |   1.00    |  0.99  |   1.00   |  18765  |
    | Class `1`   |   0.85    |  0.91  |   0.88   |   619   |
    | Accuracy  |     |        |       0.99     |  19384  |
    | Macro Avg |   0.92    |  0.99  |   0.94   |  19384  |
    | Weighted Avg | 0.99   |  0.99  |   0.99   |  19384  |

* Machine Learning Model 2:
  * Balanced accuracy score: 99.3%
  * Confusion matrix:

    |         | Predicted `0` | Predicted `1` |
    |---------|-------------|-------------|
    | Actual `0`|    18649    |     116     |
    | Actual `1`|     4      |     615     |
  
  * Classification report:

    |           | Precision | Recall | F1-Score | Support |
    |-----------|-----------|--------|----------|---------|
    | Class `0`   |   1.00    |  0.99  |   1.00   |  18765  |
    | Class `1`   |   0.84    |  0.99  |   0.91   |   619   |
    | Accuracy  |     |        |       0.99     |  19384  |
    | Macro Avg |   0.92    |  0.99  |   0.95   |  19384  |
    | Weighted Avg | 0.99   |  0.99  |   0.99   |  19384  |
  

## Summary

The second model has an overall better performance, while it is predicting more `1` scenarios than the first model, the first model was making more errors assigning a `0` label to "high-risk loans" which in return could cause an inpayment in this loans, therefore in this case is better to have a conservative approach beacuse of the nature of the problem analyzed.


