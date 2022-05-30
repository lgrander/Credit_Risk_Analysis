# Credit_Risk_Analysis

In this project, we use Python to build and evaluate several machine learning models, listed below, to predict credit risk. We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.
-	oversample the data using the RandomOverSampler and SMOTE algorithms.
-	Undersample the data using the ClusterCentroids algorithm.
-	Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
-	Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier

# Results

## Randone Over Sampler Model

The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 67%.
![Over_Sampling_Model](https://github.com/lgrander/Credit_Risk_Analysis/blob/main/Over_Sampling_Model.png)

## SMOTE Model

The results are pretty similar to the previous model.
The balanced accuracy score is 63%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 63%.
![SMOTE_Model](https://github.com/lgrander/Credit_Risk_Analysis/blob/main/SMOTE_Model.png)

## Cluster Centroids Model

Here the balanced accuracy score is down to about 52%.
The high_risk precision is still 1% only with 57% sensitivity which makes a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is only 46%.
![Cluster_Centroids_Model](https://github.com/lgrander/Credit_Risk_Analysis/blob/main/Cluster_Centroids_Model.png)

## SMOTEENN Model

The balanced accuracy score is about 63%.
The high_risk precision is 1% with 71% sensitivity which makes a F1 of only 2%.
Due to the high number of false positives, the low_risk sensitivity is 54%.
![SMOTEENN_Model](https://github.com/lgrander/Credit_Risk_Analysis/blob/main/SMOTEENN_Model.png)

## Balanced Random Forest Classifier Model

The balanced accuracy score improved to about 79%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% precision.
![Balanced_Random_Forest_Classifier_Model](https://github.com/lgrander/Credit_Risk_Analysis/blob/main/Balanced_Random_Forest_Classifier_Model.png)

## Easy Ensemble Classifier Model

The balanced accuracy score is high to about 93%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.
![Easy_Ensemble_Classifier_Model](https://github.com/lgrander/Credit_Risk_Analysis/blob/main/Easy_Ensemble_Classifier_Model.png)

# Summary 

None of the models showed a strong precision when determining if a credit risk is high. The ensemble model had the best sensitivity when detecting high risk credits. For example the EasyEnsembleClassifier model shows a recall of 93% so it detects almost all high risk credit. Unfortunately, it has a low precision, resulting in a lot of low risk credits are still falsely detected as high risk which effects the banks revenue due to missed business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.

