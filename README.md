# credit-risk-classification

## Overview of the Analysis

This analysis was completed to determine the credit-worthiness of borrowers using specific characteristics (features). This is used to make a fair prediction on how future borrowers will act based on past performance on loans with similar characteristics. Some of the characteristics considered were loan size, interest rate, income of the borrower, debt to income ratios, and total debt. 

The loans in the data set were divided into two categories: healthy and unhealthy loans. Healthy loans are loans that are less likely to default, while unhealthy have a high risk of default. 

This analysis started with a review of the data provided to determine what was provided. The number of samples were counted to determine how many healthy and unhealthy samples were provided. It clearly showed an imbalance between healthy and unhealthy, leaning strongly towards healthy loans. The data was then split between features and loan status (labels) then fed into a logistic regression model. The accuracy of the results was reviewed using a confusion matrix then classified. This process was repeated using a random oversampler model (RandomOverSampler), giving a more balanced representation of loan statuses. 

## Results

* Machine Learning Model 1:
    * Accuracy: 0.9918489475856377
    * Precision Healthy Loans: 1.00
    * Precision Unhealthy Loans: 0.85
    * Recall Healthy Loans: 0.99
    * Recall Unhealthy Loans: 0.91
    
* Machine Learning Model 2:
    * Accuracy: 0.9938093272802311
    * Precision Healthy Loans: 1.00
    * Precision Unhealthy Loans: 0.84
    * Recall Healthy Loans: 0.99
    * Recall Unhealthy Loans: 0.99
    
## Summary

Both models provided a similar accuracy score for the data provided. The recall score was increased dramatically on the unhealthy loans using the oversampler model which provided a higher overall F1 score for that loan type. The precision and recall numbers stayed similar for the healthy loans through both models. 

For this use case, the oversampler model ('2') does provide a more accurate method of determining which loans are going to be unhealthy. It provided more examples of loans that were true negatives or false negatives then the model based on just the sample data provided. In both models, the F1 score remained similar for the healthy loans so either model would work when looking at healthy loans. When determining credit-worthiness, it is important to consider if the loan has a high risk of default, which the second model did with a higher level of recall. Based on this, I would recommend using model 2 when determine credit-worthiness of future borrowers based on the characteristics provided. 
