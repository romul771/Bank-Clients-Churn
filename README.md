**Project Description**

The bank is faced with an outflow of customers. To prevent churn in the future, we need to predict whether a client will leave the bank in the near future or not.

**Project Objectives**

- Build a binary classification model based on customer behavior and churn data for 10k customers;
- Maximize *F1* metric (baseline - 0.59), controlling for the value of *AUC-ROC*.

**Project Results**

- During EDA we discovered that the dataset is moderately imbalanced (ca 20% of clients left the bank);
- First, we tried to apply two classification models, logistic regression and random forest, without taking into account the imbalance, but were unable to exceed the baseline;
-  After adjusting for imbalance, including by changing the threshold, class weighting and up- / downsampling, all models showed an improvement in the *F1* metric (from 5% to 30%);
- However, only the random forest exceeded the baseline on the validation set;
- *AUC-ROC* for all models significantly exceeded 0.5, i.e. the models performed better than a random guess;
- We tested the random forest model using two imbalance adjustment methods, threshold adjustment and class weighting, but only applying the former method we were able to "pass the test" achieving *F1* metric of 0.62 (similar to validation).      

**NOTE** See requirements.txt for environment requirements 