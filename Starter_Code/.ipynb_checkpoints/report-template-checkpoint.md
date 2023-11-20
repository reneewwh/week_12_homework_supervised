# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis. 
Answer:- To build a model that can identify the creditworthiness of borrowers based on a dataset of historical lending activity from a peer-to-peer lending services company.

* Explain what financial information the data was on, and what you needed to predict.
Answer:- Lending data that comprises of loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debts and loan_status that tells whether the loan was health ('0') or not ('1'). The prediction is based on whether a loan is healthy based on various different factors (loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt leve) of the customer. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
Answer:- value_counts - to determine the number of distinct values of each label data to evaluate the balance of target values.

* Describe the stages of the machine learning process you went through as part of this analysis.
Answer:- We started with splitting the data into training and testing. Training data means those data are used to build a report, that fits the right data pattern of the data provided. Testing data is not part of the data that helps to develop a model, hence the model won't be biased and tailored based on the testing data. As a result, the testing data is then used to check whether the model is populating as per expected based on the testing data. 

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
Answer:- `RandomOverSampler` is used as there's only a small number of high-risk loan labels comparing to the health loan labels. Hence, we believe that a model that is developed based on resampled training data will perform better.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
Answer:
Based on the first model, 87% of the high-risk loan is predicted as it's actually high-risk based on the Precision Ratio. In addition, the recall for high-risk loan is 0.91, indicating that the model correctly identified 91% of the actual high-risk loans. Based on the balance of both Precision and Recall, the F1-score for high-risk is 0.89 which is still consider as a pretty good model fitting. However, the precision and recall ratio would have improved if the number of actual occurences for high-risk loans (under 'Support') increases. On the other hand, for health loans, the metrics is shown to be 1, which is 100% accurate, as supported by the large number of data points. 


* Machine Learning Model 2:
Answer:
The second Model seems to have improved for high-risk loan data points. There are small comprimises under healthy loans, aka recall dropped from 1 to 0.99 in this model which could be deemed as negligble comparing with the larger magnitude impact for high-risk loans. The overall f1-score for high-risk loans has increased from 0.89 to 0.93 which is largely due to the increase under recall ratio,, increasing from 0.91 to 1.00, meaning 9% increase on correctly indentified instances.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
If you do not recommend any of the models, please justify your reasoning.

Answer:
If I were give more time to gather more data points and model evaluations, i may not fixated the ultimate model from the two models derived in this exercise.
However, if i were require to pick 1 model out of the two, i'd pick the second model (oversampled data), reasons as below:-
1. Reality doesnt always come with fairly distributed data points, hence we should highlight the importance of securing the accuracy of groups that have less data points available which is '1'. 
2. The metrics of macro, weighted average in the second model have improved across prevision, recall and f1-score, indiciating better fitting, better prediction and better accuracy in general.

