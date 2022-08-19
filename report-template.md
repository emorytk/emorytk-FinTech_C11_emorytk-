# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).The purpose of the analysis was to build a model to predict if an loan application would end up healthy - that is paid back, or high risk - not paid back. This analysis used financial data from a peer-to-peer lending services company, real life loans that included loans paid back and loans that were not. 

______________________________
The financial information included loan size, interest rate, borrower income, debt to income ratio, the number of accounts for each loan size, derogatory marks, total debt, and loan status. The point of the analysis was to determine which of these were more critical to predict if a loan would be healthy or high risk. 

Scikit-learn is a company that provides algorithmic models to classify data into further subsets and determine which better predicted healthy and high risk loans. The variables used to classify the loan information and data included value counts, features, and targets. Value counts were the total of healthy and high risk loans, features the financial information for each loan, and targets determined the weight of each feature in the predicting what would be healthy or high risk. 

First the original data was split into two subsets based on the loan status, healthy and high risk loans. This data is then split further into training and test subsets. The training subset gives a base to learn about the features, and the testing subset is used to test what is learned about the features. 

Logistic regression models were used with the training data, then prediction models with the testing data. To evaluate if these models worked the same data was put through further tests using accuracy scores, confusion matrix, and a classification report. Using these three to evaluate the data determined the precision and accuracy of the predictive model. 

Next, logistic regression model was used again to take a different sample of the data and test the accuracy of the first. If the predictive model is successful, then the accuracy score and classification report will move closer to 100%. If these move away from 100%, the predictive model is less accurate and not a good means of predicting healthy or high risk loans. 

In this case, the original accuracy score was 95%, and the resampled data was 99%. this is a good predictive model for determining if a loan application will end up healthy, or high risk.


Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

______________________________
* Machine Learning Model 1:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
  -Original accuracy score was 0.9520479254722232
  -Original precision score for healthy loans was 1.0, high risk loans was 0.85
  -Original recall score for healthy loans was 0.99, high risk loans was 0.91


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

  -Resampled accuracy score was 0.9936781215845847
  -Resampled precision score for healthy loans was 1.0, high risk loans was 0.84
  -Resampled recall score for healthy loans was 0.99, high risk loans was 0.99  
  
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

______________________________
The second machine learning model is recommended. 

Anyone lending money wants to have the money paid back, every time. The 5% default rate for the first machine learning model may seem workable in many areas, in money lending it is not. having the accuracy scores rise from 0.95 to 0.99 is excellent. The consistency of the precision score means the data subsets consistently had the data needed for the predictive model. The recall score for the resampled data rose from 0.91 to 0.99, and means the predictive model is highly accurate. 