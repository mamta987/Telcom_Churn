# Telecom Churn Prediction

![Python](https://img.shields.io/badge/python-3670A0?style=plastic&logo=python&logoColor=yellow)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=plastic&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=plastic&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=plastic&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-%23ffffff.svg?style=plastic&logo=Matplotlib&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=plastic&logo=scikit-learn&logoColor=white)

## Introduction

Telecom industry being a very competitive field faces high rates of customer churn than retention. With the rapid development of telecommunication service providers it has become very crucial to identify the customers who are likely to terminate their service after a certain period of time with the company. Therefore companies are seeking to develope means to find the factors that increase customer churn and take necessary actions in reducing it. 

We have the past information of a telecom firm which has collected data of all its customers. The main parameters of this data include :

 - Demographics (age, gender etc.)
 - Services availed (internet packs purchased, special offers taken etc.)
 - Expenses (amount of recharge done per month etc.)
 
 In this project will find the driving factors of churn and build a ML Classification model to predict the customers who are most likely to churn. 


## Business Goals

- Why are customers churning? Find most significant features of churn customers?
- we will build a model which will predict whether a particular customer will churn or not, i.e. whether they will switch to a different service provider or not. So the variable of interest, i.e. the target variable here is ‘Churn’ which will tell us whether or not a particular customer has churned. 
- Build a summary report and presentation for the key stakeholders stating the results and action to be taken.

## Hypothesis 

Before we proceed to build the ML model, we can ask some initial questions such as
- Which variables are statistically significant in driving the churn?
- What kind of contract are taken by customers who churn? Month to Month or a year?
- Are average monthly charges higher for churn customers?
- Do they prefer taking shorter or longer tenure?
- They don't prefer signing up for Tech support? 
- Do they belong to Senior citizen category?

## Approach 
### 1. Data Acquision 
[Link](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

### 2. Data Understanding
- Importing and Inspecting the data
- Visualizing numerical and categorical variables and finding the insights

### 3. Data Preparation
- Encoding
- Data splitting
- Rescaling the variables
- Drawing Heatmap to find correlations between the variable and dropping the variables with high correlation coefficient
 
 ### 4. Training and Building the model 
- Used Recursive Feature Elimination to find the most significant features
- Create GLM model and fit the train dataset 
- Further eliminating variables using Variance Inflation factor, t - statistics and it's p-values
- Finalising the model with features having VIF less than 5 and p-value < 0.05
- Accuracy score of 79.8% was obtained on the train data
 
 ### 5. Performance Metrics
 - Metrics like sensitivity, specificity, precision were calculated
 - ROC curve was plotted and it's Area under curve(AUC) score was found out to be 0.84
 - The optimal threshold from accuracy, sensitivity and specificity was obtained as 0.3
 - The optimal threshold from precision recall curve was obtained to be 0.42
   
 ### 6. Predictions on the Test Data
 - We will use the cutoff probability from Precision recall curve to make predictions on the test data. 
 - After prediction, performance metrics were calculated on the test dataset.
