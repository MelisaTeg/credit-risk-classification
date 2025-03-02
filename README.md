# credit-risk-classification
DA Bootcamp Challenge 20

## Overview of Analysis
* The purpose of this analysis was to predict the creditworthiness of borrowers, specifically loan risk, by a peer-to-peer lending services company.
* The financial information in the dataset included:
  *  The size of the loan('loan_size'),
  *  The interest rate ('interest_rate'),
  *  The borrower's income ('borrower_income'),
  *  The borrower's debt-to-income ratio ('debt_to_income'),
  *  The number of accounts the borrower has ('num_of_accounts'),
  *  The number of derogatory marks on their credit report ('derogatory_marks'),
  *  The borrower's total debt ('total_debt'), and
  *  The loan status ('loan_status'): 0 = healthy, 1 = high risk or defaulting.
      * The ML task was to predict whether a borrower's profile would indicate whether they have a healthy loan risk vs. a high risk of         defaulting on a loan.
* This ML project was trying to predict the borrower's loan status--whether they are at a normal risk or a high risk to lend to--from     their financial profile.
* The stages of the ML process:
  *  After importing the libraries and loading the csv file into a DataFrame, the data were separated into labels (y variables) and          features (x variables). The 'loan_status' column was separated from the other columns within the dataset.
  *  Then, the data were split into a training dataset and a testing dataset by using the train_test_split function.
  *  Next, a logistic regression model was created and fitted with the original data.
  *  Predictions were made based on the original testing data and placed into a DataFrame with the rows ordered by the index.
  *  A confusion matrix was then generated to identify the number of true and false positives and negatives.
  *  Finally, the classification report function was used to show how accurate the predictions are compared to the original data.
* Logistic regression was used because the values within the dataset were continuous (as opposed to categorical). The goal was to         predict the creditworthiness of a borrower based on the inputted financial data.

## Results
* The *accuracy score* measures how many of the predictions were correct out of all the predictions made. In terms of this project, the accuracy score was very high, at about 99.3%. This indicates that about 99.3% of the predictions are accurate.
* The *precision score* measures how many of the predicted positives were actually correct. In this case, the likelihood that a borrower's creditworthiness was predicted to be healthy was about 99.8%; however, the likelihood that the borrower's creditworthiness was predicted to be high risk was about 84.5%.
* The *recall score* refers to how many of the actual positives were detected. For this project, about 99.4% of actual individuals with healthy creditworthiness vs. about 94.5% of actual individuals with highly risky creditworthiness. 

## Summary
* Supervised Machine Learning was used for this project because the dataset that was provided was labeled. Logistic Regression was used since the values within the dataset were considered to be continuous (as opposed to categorical). This was the best option for this project because the goal was to make predictions on new data based on the relationship between data inputs (x) and outputs (y) within a dataset of actual content.
* In this situation, it seems to make more sense to focus on the precision score, as opposed to the recall score, because a higher precision score indicates fewer false positives. If the lending company inadvertently incorrectly predicts a borrower as having a healthy credit rating, for example, it could actually be financially risky to loan to such a borrower and there could be a loss. It does not make sense, in this case, to focus on the recall score. Because a higher recall score indicates that there are fewer false negatives, this is less concerning in this scenario because a borrower could accidentally be identified as not being credit worthy when they actually are. While this may be disappointing to the borrower, they have the option to seek a loan from another company. The only risk to the company is to potentially lose borrowers.
* In this scenario, it seems more important to correctly predict those whose data indicate a high risk of defaulting ('0's'). It seems that misidentifying a borrower as having healthy creditworthiness, when they actually don't, puts the lending company at risk of financial loss. 
