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

![Naive Random Oversampling](https://user-images.githubusercontent.com/111096246/212571504-1f09a470-3890-4a78-a10e-7e4b93432013.PNG)

Moving on to the next tested algorithm, SMOTE oversampling, we can observe the following results:
-	Balanced Accuracy score of 62.5%
-	Imbalanced classification report:
-- High risk precision: 1%
-- Low risk precision: 100%
-- High risk recall: 62%
-- Low risk recall: 63%

![SMOTE Oversampling](https://user-images.githubusercontent.com/111096246/212571510-42d9e5d0-0b0f-49f6-9a90-d5feb50568dd.PNG)

Switching from oversampling to undersampling, and utilizing the ClusterCentroids algorithm, the results are as follows:
-	Balanced Accuracy score of 52.1%
-	Imbalanced classification report:
-- High risk precision: 1%
-- Low risk precision: 100%
-- High risk recall: 61%
-- Low risk recall: 43%

![Undersampling](https://user-images.githubusercontent.com/111096246/212571515-4fe61ec3-d2a9-4f03-891d-b7968966d916.PNG)

Moreover, using the SMOTEEN algorithm for the combined over and undersampling, the results are:
-	Balanced Accuracy score of: 62.5%
-	Imbalanced classification report:
-- High risk precision: 1.0%
-- Low risk precision: 100%
-- High risk recall: 71%
-- Low risk recall: 54%

![Combination Sampling](https://user-images.githubusercontent.com/111096246/212571521-d661e4b3-1247-4f14-b24b-c099f142e9cf.PNG)

Furthermore, when the training data is resampled using the BalancedRandomForestClassifier algorithm with 100 estimators, the results are as follows:
-	Balanced Accuracy score of 77.2%
-	Imbalanced classification report:
-- High risk precision: 3%
-- Low risk precision: 100%
-- High risk recall: 66%
-- Low risk recall: 88%

![balanced Random Forest Classifier](https://user-images.githubusercontent.com/111096246/212571523-0edde375-c8ff-4696-bd69-2d81e0b6bf4a.PNG)

Lastly, the same data is resampled with the EasyEnsembleClassifier algorithm with 100 estimators. The final results are:
-	Balanced Accuracy score of 91.8%
-	Imbalanced classification report:
-- High risk precision: 9%
-- Low risk precision: 100%
-- High risk recall: 89%
-- Low risk recall: 94%

![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/111096246/212571528-6122bb41-c7dd-4cb1-8020-1b4fdbf8e7de.PNG)

## Summary

The initial four methodologies consisted of a mix of oversampling, undersampling and combination algorithms in order to determine each model’s effectiveness at predicting the associated risk with credit loans. The final two methods comprised of resampling, using ensemble models. 

Based on the results, the ensemble methods proved to be more effective at determining the risks for the credit loans. What the ensemble methods provided that set them apart, was the balanced mix of precision and recall accuracy scores, and the high accuracy scores.
