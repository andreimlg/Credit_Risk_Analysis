# Credit_Risk_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

As part of a new Fintech, we are on our way to build several machine learning models that can predict if a candidate will be approved or not to receive a loan. In the last years loands have become an essential part of modern society, but with this growth both, great opportunities and higher risks appear. Using Supervised Machine Learning models we will be able to learn from databases that already have a feedback whether the loan was paid or not and evaluate new data using this past information.
Specifically with credit risk the main challenge comes from having a very small portion of true positives (considering positive the ones that are high risk and they ended up not paying). So for this challenge we will have to resample using different techniques to optimize our models.

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

### RandomOverSampler
Balanced accuracy score & Confusion matrix and imbalanced classification report
![RandomOverSampler](https://user-images.githubusercontent.com/31755703/169526549-0019f8be-1f0a-4573-98b3-287ff8c337a7.PNG)

* A
* B
* C

### SMOTE
Balanced accuracy score & Confusion matrix and imbalanced classification report
![SMOTE](https://user-images.githubusercontent.com/31755703/169526567-2331d427-0eb1-479e-b886-4618217ca24e.PNG)

* A
* B
* C

### ClusterCentroids
Balanced accuracy score & Confusion matrix and imbalanced classification report
![ClusterCentroids](https://user-images.githubusercontent.com/31755703/169526583-9ff8b0c4-9501-4a87-9f3e-a8f97df95da2.PNG)

* A
* B
* C

### SMOTEENN
Balanced accuracy score & Confusion matrix and imbalanced classification report
![SMOTEENN](https://user-images.githubusercontent.com/31755703/169526595-95731b07-81ed-443a-9eb4-3c72c0cb7e98.PNG)

* A
* B
* C

### BalancedRandomForest
Balanced accuracy score & Confusion matrix and imbalanced classification report
![RandonForest](https://user-images.githubusercontent.com/31755703/169526803-3f75fbee-7769-4eeb-8805-6c80bda0bdeb.PNG)

* A
* B
* C

### EasyEnsemble AdaBoost
Balanced accuracy score & Confusion matrix and imbalanced classification report
![EasyEnsemble](https://user-images.githubusercontent.com/31755703/169526785-e446e674-3097-47fb-a875-a3a7aa0b3877.PNG)

* A
* B
* C

## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
