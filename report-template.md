# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of the analysis is to use the LogisticRegression model in Machine Leaning to train and test the existing dataset to make a prediction on the "loan_status" 
whether is healthy or high-risk.
* Explain what financial information the data was on, and what you needed to predict.
The prediction is based on parameters such as loan_size, interest_rate, borrower_income, etc. All the data is given from the csv named lending_data.
The prediction outcocme is binary (i.e, healthy as 0 or high risk as 1)
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
These following variables are used for training and testing the prediction:
1. loan_size: the amount of the current loan (likely in USD). The higher it i, the higher the risk of default.
2. interest_rate: the annual interest rate (%). The higher it is, the higher the risk of default.
3. borrower_income: the annual income of the borrower (likely in USD). The higher it is, the lower the risk of default.
4. debt_to_income: the current debt over the annual income of the borrower.The higher it is, the higher the risk of default.
5. number_of_account: the number of active accounts of the borrower. The correlation to the risk of default is more complicated (like its impact on the credit score).
6. derogatory_marks:  refer to negative information on a person's credit report that indicates past financial difficulties or failures to meet credit obligations. The higher the number, 
the higher the risk of default.
7. total_debt: current outstanding debt of the borrower. This is not an independent variable since it equals to the debt_to_income*income.We can exclude this parameter from our prediction model.

* Describe the stages of the machine learning process you went through as part of this analysis.
Splitting the data into two parts: part X with all the independent parameters as discussed above, part Y as the outcome of the prediction model (i.e, the loan status: zero as healthy, 1 as high-risk)
The prediction model is LogisticRegression from sklearn.linear_model
The default ratio between the training and testing from the original population is 75% over 25%.
Evaluate the model's performance by using the training population (which consists 25% of the original population), and print out the confusion matrix.


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
LogisticRegression is used. The explanation is above.

## Results
On the testing population (25% of the original population), the prediction for a healthy loan is very accurate (18667/(18667+76) or 99.60), the prediction for a high-risk loan is less accurate but still acceptable (569/(569+63) or 90.03%). The overall accuracy for both predictions is very high (above 99%) still.
It is also note-worthy that retaining or removing the independent parameter (such as the total_debt) does not affect much the performance of the model.
Here is the confusion matrix result 
            precision    recall  f1-score   support

           0       1.00      1.00      1.00     18752
           1       0.88      0.90      0.89       632

    accuracy                           0.99     19384
   macro avg       0.94      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
Accuracy:
Measures the overall correctness of a model
Calculated as (true positives + true negatives) / total predictions
Good for balanced datasets, but can be misleading for imbalanced ones

Precision:
Measures the accuracy of positive predictions
Calculated as true positives / (true positives + false positives)
Important when the cost of false positives is high

Recall:
Measures the ability to find all positive instances
Calculated as true positives / (true positives + false negatives)
Important when the cost of false negatives is high

## Summary
The Logistic Regression model is appropriate for binary outcomes, and is proven in this case as shown in the testing's confusion matrix.

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
The prediction for the healthy loan is more accurate than for the high risk loan based on the result of the confusion matrix.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
It is more important in this case to minimize the false negative (meaning the loan is predicted healthy while it is not just because the high consequence of this false prediction i.e, the loan can be defaulted and bank loses all the money.)

If you do not recommend any of the models, please justify your reasoning.
This model serves us well. Other models such as Decision Trees or Random Forests can be used for this application too.