# Module 12 Report Template

## Overview of the Analysis

* The purpose of the analysis was to identify the credit worthiness of people borrowing money.
* The data used was a dataset of historical lending activity from a peer to peer lending services company to see if there was any patterns that the model could use to predict whether or not a loan would default.
* `loan_size` was the amount of money being borrowed, `interest_rate` was the rate at which the money that needed to be paid back grew, `borrower_income` is the yearly income of the person taking out the loan, `debt_to_income` is the ratio of how much money the borrower owes (mostly bills) monthly to how much they earn a month, `num_of_accounts` is the number of credit card accounts the borrower has, `derogatory_marks` is the number of loans that the borrower has took out without paying back, `total_debt` is the sum of all of the borrowers debts and `loan_status` is whether or not this loan was successful (1 is yes, 0 is no).
* Firstly I imported the data to a pandas dataframe, then I got the variables needed for the model (`X`) and seperated them from the values I was trying to predict (`loan_status` or `y`), then I split the data into training and test data (this is because if the data is just left as is, it may only work for the data collected and not most cases), then I created a Logistic Regression model and fit it to the `training` data, and finally I used the model created to make predictions using the `test` data to test the accuracy of the model.
* `LogisticRegression` is a model used for classification that tries to tries to find the probability of the data being one thing or another based on the data given.

## Results

* Accuracy score: 94.4%
* Precision score: 94%(macro), 99%(weighted)
* Recall score: 94%(macro), 99%(weighted)
* F1-score (`0`): 100%(rounded)
* F1-score (`1`): 88%

## Summary

* The model generally performs well and can predict the outcome of a loan to a very good level, however the model struggles much more with predicting `1`s. 88% is a good accuracy score, but is not really high enough to justify recommending the model as loans typically deal with a high amount money and one failed loan could result in more money lost for the company than money gained from 3 successful loans. The most probable reason for this is the lack of data for the `1` result.
