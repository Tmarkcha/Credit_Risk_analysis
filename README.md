# Credit_Risk_analysis

## Overview
The purpose of this project is to determine how the different variables in “LoanStats_2019Q1” affect the decision as to whether or not approve someone for a credit loan. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. The imbalanced-learn and scikit-learn libraries are built and used to evaluate models using resampling.

The data is oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusteredCentroids algorithm. Afterwards, a combined approach of over and undersampling will be applied with the SMOTEEN algorithm. Furthermore, in order to predict credit risk, two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, are compared. Finally, the different methodologies and algorithms are compared to determine whether they should be used to predict credit risk.

## Results

Note:
Both the precision, and recall, noted in the imbalanced classification report refers to the percentage of correct positive predictions relative to total positive predictions. 

By using the RandomOverSampler algorithm for the oversampling we can note the following observations: 
-	Balanced Accuracy score of 64.7%
-	Imbalanced classification report:
-- High risk precision: 1%
-- Low risk precision: 100%
-- High risk recall: 62%
-- Low risk recall: 67% 


Moving on to the next tested algorithm, SMOTE oversampling, we can observe the following results:
-	Balanced Accuracy score of 62.5%
-	Imbalanced classification report:
o	High risk precision: 1%
o	Low risk precision: 100%
o	High risk recall: 62%
o	Low risk recall: 63%


Switching from oversampling to undersampling, and utilizing the ClusterCentroids algorithm, the results are as follows:
-	Balanced Accuracy score of 52.1%
-	Imbalanced classification report:
o	High risk precision: 1%
o	Low risk precision: 100%
o	High risk recall: 61%
o	Low risk recall: 43%


Moreover, using the SMOTEEN algorithm for the combined over and undersampling, the results are:
-	Balanced Accuracy score of: 62.5%
-	Imbalanced classification report:
o	High risk precision: 1.0%
o	Low risk precision: 100%
o	High risk recall: 71%
o	Low risk recall: 54%


Furthermore, when the training data is resampled using the BalancedRandomForestClassifier algorithm with 100 estimators, the results are as follows:
-	Balanced Accuracy score of 77.2%
-	Imbalanced classification report:
o	High risk precision: 3%
o	Low risk precision: 100%
o	High risk recall: 66%
o	Low risk recall: 88%


Lastly, the same data is resampled with the EasyEnsembleClassifier algorithm with 100 estimators. The final results are:
-	Balanced Accuracy score of 91.8%
-	Imbalanced classification report:
o	High risk precision: 9%
o	Low risk precision: 100%
o	High risk recall: 89%
o	Low risk recall: 94%

## Summary

The initial four methodologies consisted of a mix of oversampling, undersampling and combination algorithms in order to determine each model’s effectiveness at predicting the associated risk with credit loans. The final two methods comprised of resampling, using ensemble models. 

Based on the results, the ensemble methods proved to be more effective at determining the risks for the credit loans. What the ensemble methods provided that set them apart, was the balanced mix of precision and recall accuracy scores, and the high accuracy scores.

