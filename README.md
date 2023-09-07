# Module 20 - Supervised Learning 

## Credit Risk Classification Challenge 
In this challenge I used various **Supervised Machine Learning** techniques to create and train a model to make its own data-driven predictions. In this challenge's context past lending activity data will be used to predict whether potential future borrowers loan requests may be either "healthy" or at low risk of defaulting or high risk of defaulting. 
## Table of Contents


- [Credit Risk Analysis Report](#credit-risk-analysis-report)
- [Getting Started & Installing](#getting-started--installing)
- [Contributing](#contributing)

## Credit Risk Analysis Report
1. ### Overview 
    The purpose of this analysis was to build a machine learning model that would be able to make confident predictions to whether loan applications from potential borrowers of a "peer-to-peer lending services company" would be either low or high-risk of defaulting. Using historical financial data on things such as: borrower income, total debt, debt to income % and derogatory marks. The model would take into account these features based on the loan result for customers who were approved or rejected in the past and make predictions of it's own based on this data. <br>
    Initially the data was split into training & testing data sets, to train the model and then test it on data it has not seen before. Specifically a **Logistic Regression** model was used to form our predictions. Unfortunately the original data was rather inbalanced, even still the model produced a balanced accuracy score of 95%. To solve this issue I used a **RandomOverSampler** to even out the data 100%. This improved the model's overall accuracy, which I will discuss in more detail in the next section. 

2. ### Results 
    * **Model 1** 
        * The initial model proved fairly effective, with a ***balanced accuracy score*** of 95%. Its precision and recall were nearly perfect for predicting 0's (low-risk loans), the inaccuracy was brought by the lower efficacy towards predicting 1's (high-risk loans). With a precision score of 85% and a recall of 91%. These figures make sense considering the imbalance of the data. With 18765 in support of the low-risk loans and 619 in support of the high risk for the testing data, logically the model is much more trained on the low-risk loans. 
        <br>

    * **Model 2-OverSampled**
        * After recreating the model with the `RandomOverSampler()` function from `imblearn` to balance the data, the model's overall accuracy improved significantly. Improving to by a factor of 4% to 99% when assessing the balanced accuracy score. Although the precision of the 1's(high-risk loans) decreased by 1% the recall of the 1's improved by 8% ! Meaning the model significantly improved at identifying true positives with only a slight down-tick in falsely classifying true negatives. 
3. ### Summary
    In summary the the OverSampled second model proved to the most effective at predicting high-risk loans as it produced the the highest accuracy score of the two models. As success for the question at hand means a correctly identified high-risk loan (1) the fact that we see a higher recall than precision for the 1's in the resample_report for Model #2, we can safely say the model doesn't miss as many truely risky loans as it does incorrectly identify low-risk as high risk. Or identify a true 1 as a 0. <br>
    As this is a fairly simple machine learning model, I would recommend its use as long as a few suggestions for improvement were implemented. First, I would recommend scaling the initial features first with the `StandardScaler()` technique to standardize the data. Secondly, I would recommend the company seek out more data examples of high-risk loans. As this would balance the data and allow the model to train and test itself on high-risk loans more effectively. Seeking truely balanced natural data is unrealistic as statitistically less loans are defaulted on as lending companies have rigorous application processes to idenfify high-risk situations and reject applications before lending in the first place. Using any amount more of true data and needing to "OverSample" with the `RandomOverSampler()` to a lesser degree should create a better trained model. Thus producing better test results. Finally, assure human intervention remains a major component in the approval process. With added focus on the positives predictions, as these outcomes have the highest degree for error. For example 116 of the 120 total false predictions were "false positives", meaning a low-risk assessment should have been given when a high-risk was predicted.

## Getting Started & Installing 
Simply run `pip install` followed by the individual library above to import. <br>
Modules/Libraries needed:


- `pandas`
- `numpy`
- `scikit-learn`
- `pathlib`
- `imblearn`




## Contributing 

Justin Butler

**Aided By:**  <br>
* class Teacher's Assistant
* Weekly Tutoring session