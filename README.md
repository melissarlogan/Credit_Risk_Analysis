# Credit_Risk_Analysis

## Overview of the analysis

The below analysis reviews many factors provided in the loan_stats csv and how they relate to someone receiving a "low" or "high-risk" credit status. Models were then created using this data set to determine if the model could predict which credit score an applicant should be assigned.

## Results: balanced accuracy scores and the precision and recall scores
- Model 1: Naive Random Oversampling

        The Balanced Accuracy Score is 65%
        
        The Precision Score for high-risk is 1%
        
        The Recall Score is 67%

![image](https://user-images.githubusercontent.com/85718354/138608530-9dae2848-806c-40f0-81a7-1f46be6fd6aa.png)


- Model 2: SMOTE Oversampling


        The Balanced Accuracy Score is 63%
        
        The Precision Score for high-risk is 1%
        
        The Recall Score is 61%

![image](https://user-images.githubusercontent.com/85718354/138608585-74f2daab-9d1a-4aa0-b69f-e503997560c8.png)

- Model 3: Under sampling

        The Balanced Accuracy Score is 63%
        
        The Precision Score for high-risk is 1%
        
        The Recall Score is 59%
        
 ![image](https://user-images.githubusercontent.com/85718354/138608631-4ad0f82f-a5ee-4ccb-aa3c-d63dcae4af87.png)


- Model 4: Combination (Over and Under) Sampling
        The Balanced Accuracy Score is 51%
        The Precision Score for high-risk is 1%
        The Recall Score is 70%
 
 ![image](https://user-images.githubusercontent.com/85718354/138608656-507b42af-e488-44d6-b7c3-d97f2c5db95c.png)


- Model 5:Balanced Random Forest Classifier

        The Balanced Accuracy Score is 77%
        
        The Precision Score for high-risk is 3%
        
        The Recall Score is 66%
        
 ![image](https://user-images.githubusercontent.com/85718354/138608681-ec4f8872-a03c-4c64-b8a9-cc9eaefd5df5.png)


- Model 6:Easy Ensemble AdaBoost Classifier

        The Balanced Accuracy Score is 92%
        
        The Precision Score for high-risk is 9%
        
        The Recall Score is 89%
        
![image](https://user-images.githubusercontent.com/85718354/138608701-544bac01-a4da-44d0-a90d-899361ac8c9e.png)


## Summary

In the first four models I sampled using under sampling, oversampling and a combo of both with the goal of determining which analysis is best at predicting which loans should be classified as high-risk. The following two models (5 & 6) I used resampling to try and predict the same. 

In the initial models using sampling, the accuracy sores range from 51%-65% where with using resampling these climb to a range of 77%-92%. 

## Recommendation

As the bank would be concerned with precision- meaning that if the model pulls out high-risk, there's a high likelihood that the applicant should be high risk, rather than recall which is the ability to find all the high-risk applicants. A low precision is indicative of many false positives. The Easy Ensemble AdaBoost Classifier has the best of all these metrics and is the better model to use out of the 6



In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.

