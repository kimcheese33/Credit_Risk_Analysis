# Credit Risk Analysis

## Overview

The purpose of this analysis was to use various machine learning models to predict credit risk in loans. Due to the unbalanced nature of credit risk data (much fewer fraudulent cases then unfraudulent), I employed undersampling, oversampling, and combination techniques to overcome this. In addition, I utilized two other models to attempt to reduct bias in the predictions.

## Results

### Oversampling

- Random Over Sampler: This model yieled an accuracy score of 67.43%. The precision was low for the minority class (high risk) at 0.01, while high for the majority class (low risk) at 1.00. The recall was higher for the minority class at 0.74 and a little lower for the minority class at 0.61.

<img src="https://github.com/kimcheese33/Credit_Risk_Analysis/blob/main/images/RandomOverSampler.png" />


- SMOTE: This model yieled an accuracy score of 66.23%. The precision for the minority class was 0.01 and 1.00 for the majority class. The recall was 0.68 for the minority class and 0.41 for the majority class.

<img src="https://github.com/kimcheese33/Credit_Risk_Analysis/blob/main/images/SMOTE.png" />

### Undersampling

- Cluster Centroids: This model yieled an accuracy score of 54.70%. The precision for the minority class was 0.01 and 1.00 for the majority class. The recall for the minority class was 0.68 and 0.41 for the majority class.

<img src="https://github.com/kimcheese33/Credit_Risk_Analysis/blob/main/images/ClusterCentroid.png" />

### Combination (Over and Under) Sampling

- SMOTTEENN: This model yielded an accuracy score of 66.15%. The precision for the minority class was 0.01 and 1.00 for the majority. The recall for the minority class was 0.73 and 0.59 for the majority class

<img src="https://github.com/kimcheese33/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png" />

### Ensemble Learners

- Balanced Random Forest Classifier: This model yielded an accuracy score of 78.85%. The precision for the minority class was 0.03 for the minority class and 1.00 for the majority class. The recall for the minority class was 0.70 and 0.87 for the majority class.

<img src="https://github.com/kimcheese33/Credit_Risk_Analysis/blob/main/images/BalancedRandomForest.png" />

- Easy Ensemble AdaBoost: This model yielded an accuracy score of 93.17%. The precision for the minority class was 0.09 and 1.00 for the majority class. The recall for the minority class was 0.92 and 0.94 for the majority class.

<img src="https://github.com/kimcheese33/Credit_Risk_Analysis/blob/main/images/AdaBoost.png" />


## Summary

The precision for the majority class for all models was high at 1.0. However, the precision for all the models for the minority class was very low with the ensemble learners performing slightly better. The low precision for the minority class indicates that there is unreliable positive classification across the board. The recall for the majority and minority classes were more varied across the models. The recall score for the minority class was the highest for the AdaBoost model at 0.92 and lowest for the Cluster Centroids and SMOTE models at 0.68. A lower recall score indicates a large number of false negatives. The model I recommend would be the Easy Ensemble AdaBoost model, because it had the highest recall, precision, and accuracy score.
