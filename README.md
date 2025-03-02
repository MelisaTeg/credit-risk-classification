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
* Logistic regression was used because the values within the dataset were continuous (as opposed to categorical). The goal was to     
  predict the creditworthiness of a borrower based on the inputted financial data.
