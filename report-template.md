# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
Using machine learning techniques to evaluate credit risk and predict whether a loan falls into the category of "healthy loan" (0) or "high-risk loan" (1).

* Explain what financial information the data was on, and what you needed to predict.
The dataset includes columns such as `loan_size`, `interest_rate`, `borrower_income`, `debt_to_income`, `num_of_accounts`, `derogatory_marks`, `total_debt`, and `loan_status`. The target variable to predict is `loan_status`.

* Provide basic information about the variables you were trying to predict (e.g., value_counts).
The target variable, `loan_status`, is distributed as follows: 0 (Healthy Loan) and 1 (High-Risk Loan).

* Describe the stages of the machine learning process you went through as part of this analysis.
Data Preparation: The dataset was split into training and testing sets using the `train_test_split` function.  
Model Building: A logistic regression (`LogisticRegression`) model was trained on the data.  
Model Prediction: Predictions were made using the test dataset.  
Performance Evaluation: A confusion matrix and classification report were generated, including metrics such as accuracy, precision, recall, and F1 score.


* Briefly touch on any methods you used (e.g., LogisticRegression, or any other algorithms).
We used logistic regression, a machine learning algorithm designed for binary classification problems. It calculates a weighted sum of input features using a linear regression model and applies a sigmoid function to map the result to a range of [0,1], representing the probability of belonging to a specific class.
Prediction is based on probability values:
- Probability ≥ 0.5: Predicted as the positive class (e.g., High-Risk Loan, 1).  
- Probability < 0.5: Predicted as the negative class (e.g., Healthy Loan, 0).  
Logistic regression is simple, efficient, and interpretable, making it particularly well-suited for classification tasks like credit risk assessment.


## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
 Accuracy : 0.99,  Precision: 0.93 ,Recall:0.97
  
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the 1's, or predict the 0's? )

If you do not recommend any of the models, please justify your reasoning.

The logistic regression model performed exceptionally well in predicting both healthy loans and high-risk loans. For healthy loans (class 0), the model's performance was nearly perfect, with precision and F1 scores both reaching 1.00.  

For high-risk loans (class 1), the model achieved a high recall of 0.94 but had a relatively lower precision of 0.86, indicating that some healthy loans were misclassified as high-risk loans.  

In our business context, however, accurate prediction of class 1 (high-risk loans) is more critical, as our goal in the credit business is to identify risky loans effectively and reduce credit risk.  

Overall, the logistic regression model demonstrated strong performance for this credit risk assessment task. It is recommended as the model of choice due to its high precision and accuracy in identifying high-risk loans.