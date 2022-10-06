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
#### This model produced the worst results with an accuracy score of 54.42% which is not ideal as it is basically chance with 50/50 odds. This would not be a model that I would recommend for LendingClub to use to accuratly predict credit risk. 

![Image_2](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Cluster_score.png)

#### The F-Score for Cluster Centroids Undersampling gave similar results, as you can see below in the f1 column 'high_risk' only had a .001 score for prediction and and average of .56 

![Image_3](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/Cluster_f1.png)

### * Naive Random Oversampling 
#### This model produced scores that were again lack luster when it comes to accuracy, which means I would again, not recommend this model for LendingClub. Below you can see that this model only scored 65.26%, while this is better than Cluster Centroids, 65% is not something you can rely on when trying to predict credit risk. 

![Image_4](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/ROS_Score.png)

#### The F-Socre for Naive Random Oversampling is only a touch better at predicting 'high_risk' loans than Cluster Centroids, scoring .02. The average score is quite a bit higer than the previous method receiving a .77 

![Image_5](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/ROS_f1.png)





Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

Analysis (24 points)
The written analysis has the following:

Overview of the loan prediction risk analysis:

The purpose of this analysis is well defined (4 pt)
Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
