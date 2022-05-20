# Credit_Risk_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

As part of a new Fintech, we are on our way to build several machine learning models that can predict if a candidate will be approved or not to receive a loan. In the last years loands have become an essential part of modern society, but with this growth both, great opportunities and higher risks appear. Using Supervised Machine Learning models we will be able to learn from databases that already have a feedback whether the loan was paid or not and evaluate new data using this past information.
Specifically with credit risk the main challenge comes from having a very small portion of true positives (considering positive the ones that are high risk and they ended up not paying). So for this challenge we will have to resample using different techniques to optimize our models.

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

### RandomOverSampler
Balanced accuracy score & Confusion matrix and imbalanced classification report
* As we were expecting, in a fraud detection machine learning model, the main challenge is that positives (high risk) are much smaller than negatives. Using RandomOverSampler to diminish this effect we got the following results:
![RandomOverSampler](https://user-images.githubusercontent.com/31755703/169526549-0019f8be-1f0a-4573-98b3-287ff8c337a7.PNG)

* Balance accuracy score is 62% which means the model will be right 62% of the time. As per the confusion matrix we notice that despite the detection of actually fraud cases we are still missing high risk loans, as well as we are missing low risk loans because we are detecting them as High Risk and this could impact profitability letting go potential low risk clients.

* Precision score: How likely is it that the loan will be high risk? With such a low value we can't be sure.
Precision = TP/(TP + FP):
52/(52+5952) = 0.01

* Recall (Sensitivity) score : We know it is a High Risk, how likely is that the model will predict it? It is also a low value considering that almost have of the high risk loans will go undetected.
Sensitivity = TP/(TP + FN):
52/(52 + 35) = 0.60

* F1 Score: There is a pronounced imbalance between sensitivity and precision resulting in a low F1 Score. This is not a useful algorithm.
2(Precision * Sensitivity)/(Precision + Sensitivity) = 0.02


### SMOTE
Balanced accuracy score & Confusion matrix and imbalanced classification report
* In SMOTE we need to remember how the minority is increased, and this is by interpolating new values.

![SMOTE](https://user-images.githubusercontent.com/31755703/169526567-2331d427-0eb1-479e-b886-4618217ca24e.PNG)

* After running the model, we have a higher Balance accuracy score of 65%. This increase helps but we are still far away from the performance we would like to have. Therefore the values of Precision, Recall and F1 Score are similar.
* Precision score: 
Precision = TP/(TP + FP):
56/(56+5840) = 0.01

* Recall (Sensitivity) score : 
Sensitivity = TP/(TP + FN):
56/(56 + 31) = 0.64

* F1 Score: 
2(Precision * Sensitivity)/(Precision + Sensitivity) = 0.02

### ClusterCentroids
Balanced accuracy score & Confusion matrix and imbalanced classification report.
Using ClusterCentroids we did't get better results which reminds us that while resampling can attempt to address imbalance, it does not guarantee better results.
![ClusterCentroids](https://user-images.githubusercontent.com/31755703/169526583-9ff8b0c4-9501-4a87-9f3e-a8f97df95da2.PNG)

* Precision score: 
Precision = TP/(TP + FP):
56/(56+5840) = 0.01

* Recall (Sensitivity) score : 
Sensitivity = TP/(TP + FN):
56/(56 + 31) = 0.64

* F1 Score: 
2(Precision * Sensitivity)/(Precision + Sensitivity) = 0.02

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
