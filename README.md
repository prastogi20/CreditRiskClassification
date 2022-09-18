# Credit Risk Classification
Prediction using Logistic Regression Model 

## Overview of the Analysis

Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans.

### Purpose

The purpose of analysis is to identify the creditworthinees of borrowers and classify loan as healthy or risky.

### Data used of Analysis
 We have historical lending data, that identify loan as healthy if loan_status is 0 and risky if loan_status is 1. This value depends on various features like loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, 	derogatory_marks and total_debt. 
 
    loan_status values_counts suggests that the historical data is imbalanced

    0    75036
    1     2500
    Name: loan_status, dtype: int64
 
  
### Stages of machine learning process 

* Split the data into training and testing datasets
* Create Logistic Regression model using original data, make predictions using test data 
* Evaluate model performance by
    * Calculating the accuracy score of the model.
    * Generating a confusion matrix.
    * Printing the classification report.
* As the given data is imbalanced, create logistic regression model using resample data, make predictions using test data and than Evaluate the performance.
* Compare the performance of both models, and make recommendations on the basis of the results.

## Results

To view the results and detailed analysis please refer jupyter notebook "credit_risk_resampling.ipynb"

### Machine Learning Model 1
  * Logistic Regression Model - using given lending historical data 
  * Accuracy: 95.2%
  * Precision: 100%
  * Recall: 91% 



### Machine Learning Model 2
  * Logistic Regression Model - using resample lending data, in this scenario over sampling data technique is used 
  * Accuracy: 99.3%
  * Precision: 100%
  * Recall: 99% 

## Summary
Since the historical lending data is imbalanced it is recommended to resample data before applying Logistic Regression model to predict loan_status. Resampling of data provided more accuracy for risky loan predictions, though it is less important for healthy loans.

Note: loan_status is the variable that classify loan as healthy or risky.

