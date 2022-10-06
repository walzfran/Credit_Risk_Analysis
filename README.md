# Credit_Risk_Analysis

### Overview
#### This analysis shows various machine learning models to evaluate credit risk for individual customers. The data set used for these models was from LendingClub, a peer-to-peer lending service. The first task was to clean the data and make sure that all of the data was readable by the learning models. After the data was cleaned it was heavily unbalanced with only 347 of the 68,817 entries being "high-risk" so now we will go over the different models and try to determine the best option for LendingClub. 
![Image_1](https://github.com/walzfran/Credit_Risk_Analysis/blob/main/images/y_counts.png)

#### Models Used:
#### * RandomOverSampler
#### * SMOTE
#### * ClusterCentroids
#### * SMOTEENN
#### * BalancedRandomForestClassifier
#### * EasyEnsembleClassifier

### Results 
#### When looking at the different models used, we will be looking at the Balanced Accuracy Score (balanced_accuracy_score) as well as the Imbalanced Classification Report (classification_report_imbalanced). When going over the Imbalanced Classification Report the most important column to look at is "f1" this column shows the 'F-Score' which measures the accuracy of the test, we will be able to see the score from the high risk, low risk and an average. 

The following results are presented in ascending order based on the Balanced Accuracy Score. 







Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

Deliverable 4 Requirements
Structure, Organization, and Formatting (6 points)
The written analysis has the following structure, organization, and formatting:

There is a title, and there are multiple sections (2 pt)
Each section has a heading and subheading (2 pt)
Links to images are working, and code is formatted and displayed correctly (2 pt).
Analysis (24 points)
The written analysis has the following:

Overview of the loan prediction risk analysis:

The purpose of this analysis is well defined (4 pt)
Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
