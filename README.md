# Credit_Risk_Analysis

## Overview of the analysis:
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, using different techniques train and evaluate models with unbalanced classes. Using not only imbalanced-learn but also scikit-learn libraries help me build and evaluate models using resampling. Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I will be able to oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Result
### Deliverable 1
I evaluated three machine learning models by using resampling to determine which is better at predicting credit risk. First, I used the oversampling RandomOverSampler and SMOTE algorithms, and then I used the undersampling ClusterCentroids algorithm. Using these algorithms, I resampled the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

* Random OverSampling
![image](https://user-images.githubusercontent.com/105985796/194149532-dcc6f364-6b10-4c56-9ca5-ab354fb1e1e6.png)

* In random oversampling, examples of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced. examples from the minority class are randomly selected and added to the minority class.

* SMOTE ALgorithm
![image](https://user-images.githubusercontent.com/105985796/194150727-27e5358d-83a2-4275-a625-31ff70749717.png)

* The synthetic minority oversampling technique (SMOTE), as the previuous the size of the minority is increased, but these new examples are interpolated. That is, for an instance from the minority class, a number of its closest neighbors is chosen. Based on the values of these neighbors, new values are created.

* Cluster Centroids
![image](https://user-images.githubusercontent.com/105985796/194155656-b669802e-c2c3-4558-a267-2e3d8329fd57.png)

* Cluster centroid undersampling is akin to SMOTE. The middle of a cluster. A centroid is a vector that contains one number for each variable, where each number is the mean of a variable for the observations in that cluster. The centroid can be thought of as the multi-dimensional average of the cluster.

### Deliverable 2
Using the SMOTEENN algorithm, I resampled the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

![image](https://user-images.githubusercontent.com/105985796/194156619-15875229-db3a-4ff7-8a49-632df6a5b147.png)

### Deliverable 3
I trained and compared two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

* Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/105985796/194157089-5c198c85-0fe3-435e-b7e7-6efda6be6319.png)

* A balanced random forest classifier. A balanced random forest randomly under-samples each boostrap sample to balance it. Each tree is simpler because it is built from a random subset of features.

* Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/105985796/194157770-4c4c7f05-ef69-4a79-a8bf-6ec2085ed090.png)

* AdaBoost also called Adaptive Boosting is a technique in Machine Learning used as an Ensemble Method.

## Summary
We should make sure what is what we want to detect whether a future loan´s customer is high risk or not, our model is going to be the one that prevent the least amount of high risk loans pass through undetected. For example, our model must be must sensitive or with a recall for high-risk high. Therefore, I would recomend AdaBoost Ensemble Classifier because this model got a the highest balanced accuracy, the highest precision high risk and the highest Recall high risk.
