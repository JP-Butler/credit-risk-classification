# Module 20 - Supervised Learning 

## Credit Risk Classification Challenge 
In this challenge I used various **Supervised Machine Learning** techniques to create and train a model to make its own data-driven predictions. In this challenge's context past lending activity data will be used to predict whether potential future borrowers loan requests may be either "healthy" or at low risk of defaulting or high risk of defaulting. 
## Table of Contents


- [Credit Risk Analysis Report](#credit-risk-analysis-report)
- [Getting Started & Installing](#getting-started--installing)
- [Resources](#resources)
- [Contributing](#contributing)

## Credit Risk Analysis Report
1. ### Overview 
    The purpose of this analysis was to build a machine learning model that would be able to make confident predictions to whether a loan applications from a potential borrowers of a "peer-to-peer lending services company" would be either low or high-risk of defaulting. Using historical financial data on things such as: borrower income, total debt, debt to income % and derogatory marks. The model would take into account these figures based on the loan result for customers who were approved or rejected in the past and make predictions of it's own based on this data. <br>
    Initially the data was split into training & testing data sets, to train the model and then test it on data it has not seen before. Specifically a **Logistic Regression** model was used to form our predictions. Unfortunately the original data was rather inbalanced, even still the model produced a balanced accuracy score of 95%. To solve this issue I used a **RandomOverSampler** to even out the data 100%. This improved the model's overall accuracy, which I will discuss in more detail in the next section. 

2. ### Results 

3. ### Summary

## Getting Started & Installing 

## Contributing 

Justin Butler

**Aided By:**  <br>
* class Teacher's Assistant
* Weekly Tutoring session