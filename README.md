# Credit_Risk_Analysis

### Overview
#### This analysis shows various machine learning models to evaluate credit risk for individual customers. The data set used for these models was from LendingClub, a peer-to-peer lending service. The first task was to clean the data and make sure that all of the data was readable by the learning models. After the data was cleaned it was heavily unbalanced with only 347 of the 68,817 entries being "high-risk" so now we will go over the different models and try to determine the best option for LendingClub. 
![Image_1](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/y_counts.png)

#### Models Used:
* RandomOverSampler
* SMOTE
* ClusterCentroids
* SMOTEENN
* BalancedRandomForestClassifier
* EasyEnsembleClassifier

### Results 
#### When looking at the different models used, we will be looking at the Balanced Accuracy Score (balanced_accuracy_score) as well as the Imbalanced Classification Report (classification_report_imbalanced). When going over the Imbalanced Classification Report the most important column to look at is "f1" this column shows the 'F-Score' which measures the accuracy of the test, we will be able to see the score from the high risk, low risk and an average. 

#### The following results are presented in ascending order based on the Balanced Accuracy Score. 

### * Cluster Centroids Undersampling 
This model produced the worst results with an accuracy score of 54.42% which is not ideal as it is basically chance with 50/50 odds. This would not be a model that I would recommend for LendingClub to use to accuratly predict credit risk. 

![Image_2](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Cluster_score.png)

The F-Score for Cluster Centroids Undersampling gave similar results, as you can see below in the f1 column 'high_risk' only had a .001 score for prediction and and average of .56 

![Image_3](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Cluster_f1.png)

### * Naive Random Oversampling 
This model produced scores that were again lack luster when it comes to accuracy, which means I would again, not recommend this model for LendingClub. Below you can see that this model only scored 65.26%, while this is better than Cluster Centroids, 65% is not something you can rely on when trying to predict credit risk. 

![Image_4](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/ROS_Score.png)

The F-Socre for Naive Random Oversampling is only a touch better at predicting 'high_risk' loans than Cluster Centroids, scoring .02. The average score is quite a bit higer than the previous method receiving a .77 

![Image_5](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/ROS_f1.png)

### * Combination Sampling 
This model had very similar results to Naive Random Oversampling with the accuracy score being 65.42%, which means that I would advise against this model as well. 

![Image_6](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/SMOTEENN_Score.png)

With Combination Sampling the F-Scores were very similar to Naive Random Oversampling, the difference being that the average score was actually lower than the score we got with the previous method. 

![Image_7](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/SMOTEEN_f1.png)

### * SMOTE Oversampling 
This model was similar to the last two methods with an accuracy score of 65.44% meaning that these three methods were all pretty much the same with thier ability to test the accuracy coming in under 2/3rds accuracy. With odds like 2/3rds I would still not recommend this model for LendingClub. 

![Image_7](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/SMOTE_score.png)

This model had the same score for 'high_risk' as Combination Sampling, .02 but had a better average score coming in at .80 which is better but this is still not the numbers we would want to see to make a recommendation to LendingClub. 

![Image_8](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/SMOTE_f1.png)

### * Balanced Random Forest Classifier 
When looking at the results from Balanced Random Forest Classifier, we see that it has improved quite a bit from the last models we analyzed. The score of this model was 78.85% which is over 3/4ths accurate which would suffice but hopefully we can find a better model to recommend to LendingClub. 

![Iamge_9](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Forest_score.png)

This model had better scores for 'high_risk' coming in at .06 with an average of .93 which is quite a bit higher than we have seen with the last 4 models. 

![Image_10](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Forest_f1.png)

### * Easy Ensemble AdaBoost Classifier 
The results from this model were the best, the accuracy score is 93.16% which is very good, acceptable for LendingClub to use when determining loan risk. 

![Image_11](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Easy_score.png)

The F-Scores were also the best of the 6 models we analyzed with the 'high_risk' coming in at .16, this is the only model that was over .1. The average score being .97 which is again the highest we have seen in the models used. 

![Image_12](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Easy_f1.png)

### Summary 
#### After looking at the results from all of the models tested, if there was one model I had to chose I would suggest that LendingClub use the Easy Ensemble AdaBoost Classifier. With the accuracy score bing over 90% it seems like it would be an easy choice. But one concern that I have is that when looking at the F-Scores, there is still a big gap in accuracy of 'high_risk' to 'low_risk' with .16 for high risk and .97 for low risk. The large gap would probably come from there being such a large difference in the data set from high to low risk loans meaning the learning model has to fill in quite a bit and has low accuracy on determining the high risk loans. I would want to test this model a few more times on potantial datasets before saying with confidence that LendingClub should go forward with using Easy Ensemble AdaBoost Classifier. 
