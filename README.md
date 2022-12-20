# Module 12 Report


## Overview of the Analysis

The purpose of this analysis is to train and evaluate models with imbalanced classes to accurately predict which borrowers will default on their loans. 

The financial information we used was historical lending activity from a peer-to-peer lending services company that gave us data about lenders and their loan status (default or good standing). Based on information provided, we are trying to use our models to determine if the borrower will default on their loan, or not, and since we have the information, test it against whether they actually did default.

Using the 'value_counts' function, we know that out of 77,536 loans, 2,500 borrowers defaulted, leaving 75,036 in good standing. 

After getting the counts, we use a logistic regression model to compare two versions of the data, the first is the orginal data, the second is oversampled data.

For each analysis, after preparing the data, we split the data into training and testing sets, model and fit the data into a logistic regression, predit the testing labels and calculate performance metrics. 

To split and data into training and testing sets, we use sklearn 'train_test_split' function. We also use sklearn 'LogisticRegression' to model and fit the data. Performance metrics are calculated by evaluating 'testing_targets' vs. 'testing_predictions'. 'RandomOverSampler' is used to instantiate the oversampled model.


## Results

* Machine Learning Model 1:
  
  * Balanced accuracy score of 95.2%
  * Precision for predicting defaults 85% 
  * Recall for predicting defaults 91%



* Machine Learning Model 2:
  
  * Balanced accuracy score of 99.4%
  * Precision for predicting defaults 84% 
  * Recall for predicting defaults 99%

## Summary

Machine Learning Model 1 works best. It predicts defaults more accurately, with a higher precision score for predicting defaults. Performance depends on the problem we are trying to solve and here, it is more important to predict defaults than it is to predict loans of good standing. 


