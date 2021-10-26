# Credit_Risk_Analysis
## Overview
The purpose of this analysis was to predict credit risk using credit card credit data from Lending Club. I oversampled the data using  RandomOverSampler  and SMOTE algorithms, as well as undersampled the data using ClusterCentroids algorithms. I then used a combination approach and compared to compare the results of all the test. Last I used BalancedRandomForestClassifier and EasyEnsembleClassifier to try and predict credit  risk of potential applicants. 

## Results
### Random Sampling
![Oversampling](https://user-images.githubusercontent.com/83738699/138814028-bd2d6870-5595-4d55-803d-8c618efd9598.PNG)

The balance accuracy score is 65% which is very apparent when you look at the confusion matrix. Looking at the confusion matrix you can see that there is a a large amount of predicted low risk applicants in the data set. If you look at the imbalaced classification report the f1 score for high risk is only 2% while low risk is 80%, this means we need to either oversample, undersample, or use a combination approach.  
### Under Sampling
![undersampling](https://user-images.githubusercontent.com/83738699/138814666-fedec4fd-fdec-4640-aa16-2f34f75ef895.PNG)

By under sampling the data, I took a smaller sample of data from the low risk category to match that of the high risk.  Using under sampling decreased our balance accuracy score to 51%, meaning under sampling the data will not produces accurate predictions. 
### Combination of Undersampling and OverSampling
![combination](https://user-images.githubusercontent.com/83738699/138815115-ad6e8908-a971-4944-865f-57dc0ccee937.PNG)

By using the combination approach, the balance accuracy score goes back to 64% close to what  RandomSampling produced. When looking at the confusion matrix the predicted high risk but actually low risk category is less than just under sampling the data but has a higher true low risk prediction. This is a good thing with this type of data because its better to over predict those that would cause a high risk of loss, and then  review the application  to make a final determination. Even looking at the imbalanced classification report, the recall score for high risk is now to 70% with low risk at 57%. 
### BalancedRandomForestClassifier
![balancedforest](https://user-images.githubusercontent.com/83738699/138816274-55f32aaf-ca4f-4fce-854e-868883b7da0e.PNG)

Using the BalancedRandomForestClassifier did improve our results having less predicted high risk actually be low risk. Then when you look at the true predicted low risk category you can see that the model is now more accurate at predicating credit risk. 
### Easy EnsembleClassifier
![easyec](https://user-images.githubusercontent.com/83738699/138816862-d19b731d-4bdc-480e-856f-fc24a3953253.PNG)

EasyEnsembleClassifier is the the best yet at providing the most accurate prediction of credit risk. With a balance score of 93%, less than a 1000 false high risk predictions and an even more accurate low risk prediction. The f1 score for high risk is double even using BalancedRandomForestClassifier and both recall scores are over 90%. 
## Summary
While all methods were accurate to an extent, by applying different methods to the the analysis you are able to have your MachineLearning algorithm preform more accurately.  By cutting down  on the amount of false perditions, especially when predicting credit risk, you are saving time and money for a person to then review the application. From this analysis, all the methods used are good at predicting low risk credit but EasyEnsembleClassifier is the most accurate at identifying high risk with a recall of 91%. Although there are still a good number of false high risk, for a credit card company this is not a bad number to work with compared to the other methods.  

> Written with [StackEdit](https://stackedit.io/).
