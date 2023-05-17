# Credit Risk Classification
## Overview:

The purpose of the analysis was to establish a robust Supervised Machine Learning model that can be used on additional datasets to predict/classify whether a loan is at risk or healthy, based on the features below.
We will be using this dataset to test two logistic regression models.
1. The size of the loan
2. The interest rate
3. The borrower's income
4. The ratio of debt to the borrower's income
5. The number of accounts the borrower has with the lending service
6. The number of derogatory marks for the borrower (negative information that appear on a borrower's credit report, indicating a history of delinquent payments or other defaults on a loan or credit account.)
7. The borrower's total debt which includes the loan status - whether the loan was 'Healthy' or 'High-Risk.'
The "target" variable (y) we're aiming at predicting for our analysis is the loan_status which can be classified as 0 or 1. All other data information are within the "features" variable (or X).

The stages used as part of the machine learning process analysis used are:

Create the model
Fit the model
Use the model
Credit risk poses a classification challenge that’s inherently imbalanced since healthy loans easily outnumber risky loans. A supervised machine learning classification model which categorize according to shared qualities and characteristics using a Logistic Regression technic was used.

To test the model a resampling of the dataset operation was and completed and re-test using the initial model to test the result and efficiency.

Results
Machine Learning Model 1 - Logistic Regression:

Accuracy: 0.9520479254722232
Precision: 1.0 / 0.85
Recall scores: 0.99 / 0.91
Machine Learning Model 2 - Logistic Regression w/ ReSampled Data:

Accuracy: 0.9950160462226244
Precision: 1.0 / 0.99
Recall scores: 0.99 / 1.0

Summary
Both precision for the logistic regression model, original and fit with oversampled data, were great at detecting healthy loans (1.0) and less accurate at detecting high-risk one (0.85 vs 0.84).

In terms of the recall, the model using resampled data returned higher result at detecting healthy loan and high-risk loan alike (0.91 vs 0.99).

To summarize, the model using resampled data as showed an overall increase in accuracy at detecting high-risk loan.

As a side note, the balanced accuracy score was higher for the resampled data (0.9950 vs 0.9520), which echoes the classification report.

To summarize, our model using the resampled data performs slightly better after comparing the accuracy score and classification report.

Because of the nature of Credit risk which is inherently imbalanced since healthy loans easily outnumber risky loans it is imperative that our final model predict accuratly the "high-risk loan" or 0.

At this preliminary stage of this tool and after analysing the results it would be our recommandation to continue our exploration of different supervised machine learning classification techniques such as "Support Vector Machines", "Decision Tree Based Algorithms" or "K-Nearest Neighbors" to name a few in order to increase the prediction accuracy level to 0.97 or higher.



## Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
### Instructions
The instructions for this Challenge are divided into the following subsections:

- Split the Data into Training and Testing Sets

- Create a Logistic Regression Model with the Original Data

- Predict a Logistic Regression Model with Resampled Training Data

- Write a Credit Risk Analysis Report

### Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:

1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

### NOTE
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

3. Split the data into training and testing datasets by using train_test_split.

### Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:

1. Fit a logistic regression model by using the training data (X_train and y_train).

2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

3. Evaluate the model’s performance by doing the following:

  - Calculate the accuracy score of the model.

  - Generate a confusion matrix.

  - Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Write a Credit Risk Analysis Report
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

1. An overview of the analysis: Explain the purpose of this analysis.

2. The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

3. A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
