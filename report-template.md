# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of the analysis is to use the LogisticRegression model in Machine Leaning to train and test the existing dataset to make a prediction on the "loan_status" 
whether is healthy or high-risk.
* Explain what financial information the data was on, and what you needed to predict.
The prediction is based on parameters such as loan_size, interest_rate, borrower_income, etc. All the data is given from the csv named lending_data.
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

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
