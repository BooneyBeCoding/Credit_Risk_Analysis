# Credit_Risk_Analysis

## Overview
The purpose of this analysis was to use various machine learning models to predict credit risk in loans. Due to the unbalanced nature of credit risk data (much fewer fraudulent cases then unfraudulent), I employed undersampling, oversampling, and combination techniques to overcome this. In addition, I utilized two other models to attempt to reduct bias in the predictions.

## Results
### Oversampling
Random Over Sampler: This model yieled an accuracy score of 64.81%. The precision was low for the minority class (high risk) at 0.01, while high for the majority class (low risk) at 1.00. The recall was higher for the minority class at 0.74 and a little lower for the minority class at 0.61.
![Random Oversampling](https://user-images.githubusercontent.com/71455991/107886650-c2759d80-6ec6-11eb-850a-5bfb0c5a5d0a.PNG)

#### SMOTE
This model yieled an accuracy score of 66.26%. The precision for the minority class was 0.01 and 1.00 for the majority class. The recall was 0.63 for the minority class and 0.69 for the majority class.
![SMOTE](https://user-images.githubusercontent.com/71455991/107886677-0072c180-6ec7-11eb-8a51-0ba1057eddb0.PNG)

### Undersampling
Cluster Centroids: This model yieled an accuracy score of 54.73%. The precision for the minority class was 0.01 and 1.00 for the majority class. The recall for the minority class was 0.68 and 0.41 for the majority class.
![Cluster Centroid](https://user-images.githubusercontent.com/71455991/107886707-521b4c00-6ec7-11eb-95d3-9eb80fda3290.PNG)

### Combination (Over and Under) Sampling
#### SMOTTEENN
This model yielded an accuracy score of 66.39%. The precision for the minority class was 0.01 and 1.00 for the majority. The recall for the minority class was 0.75 and 0.58 for the majority class.
![SMOTEENN](https://user-images.githubusercontent.com/71455991/107886732-8262ea80-6ec7-11eb-88b5-0ff0ef4ecfe3.PNG)

### Ensemble Learners
#### Balanced Random Forest Classifer
This model yielded an accuracy score of 78.85%. The precision for the minority class was 0.03 for the minority class and 1.00 for the majority class. The recall for the minority class was 0.70 and 0.87 for the majority class.
![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/71455991/107886780-c35aff00-6ec7-11eb-873f-9150e3900bb9.PNG)

#### Easy Ensemble AdaBoost
This model yielded an accuracy score of 93.17%. The precision for the minority class was 0.09 and 1.00 for the majority class. The recall for the minority class was 0.92 and 0.94 for the majority class.
![AdaBoost](https://user-images.githubusercontent.com/71455991/107886805-ea193580-6ec7-11eb-9236-877efd0b940e.PNG)

## Summary
The precision for the majority class for all models was high at 1.0. However, the precision for all the models for the minority class was very low with the ensemble learners performing slightly better. The low precision for the minority class indicates that there is unreliable positive classification across the board. The recall for the majority and minority classes were more varied across the models. The recall score for the minority class was the highest for the AdaBoost model at 0.92 and lowest for the Cluster Centroids and SMOTE models at 0.69 & 0.68. A lower recall score indicates a large number of false negatives. The model I recommend would be the Easy Ensemble AdaBoost model, because it had the highest recall, precision, and accuracy score.
