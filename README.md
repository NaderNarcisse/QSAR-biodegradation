# QSAR-biodegradation
ESILV - Python for data analysis - project 2022

## Motivation
School Project from the Data Analysis course in Python, taught as part of the ESILV master's degree.

## Dataset
The dataset was provided by UCI.
https://archive.ics.uci.edu/ml/datasets/QSAR+biodegradation

## Objective

The objective here is to train a reliable model to determine if a compound is biodegradable or not.

## Exploratory Data Analysis (EDA)


## Model Selection
With Cross-validation: evaluating estimator performance,
1. Logistic regression
2. Decision Tree
3. Support Vector Machine
4. Linear Discriminant Analysis (LDA)
5. Quadratic Discriminant Analysis (QDA)
6. Random Forest
7. K-Nearest Neighbors
8. Bayes

## Selecting Random Forest and SVM
Since it provides the overall best performance, we've selected the two best models.
![Model Selection](https://github.com/NaderNarcisse/QSAR-biodegradation/blob/main/Pictures/Model_Performances.png "Model Selection")

## Model Testing

### SVM Support Vector Machine



### Random Forest



## Summary

+ Support Vector Machine achieved an accuracy of 89 %
+ Model is trained on a **balanced class dataset**, using Oversampling with the Synthetic Minority Oversampling Technique (SMOTE)
+ This model could be used as a Proof of Concept for the use of simulation on compounds to determine whether it is biodegradable or not.
