# QSAR-biodegradation
ESILV - Python for data analysis - project 2022

## Motivation
School Project from the Data Analysis course in Python, taught as part of the ESILV master's degree.

## Dataset
The dataset was provided by UCI.
https://archive.ics.uci.edu/ml/datasets/QSAR+biodegradation

## Objective

The objective here is to obtain a reliable model to determine if a compound is biodegradable or not.

## Preview of the Exploratory Data Analysis (EDA)

![Correlation Matrix](https://github.com/NaderNarcisse/QSAR-biodegradation/blob/main/Pictures/Correlation_between_features.png "Correlation Matrix")


![Correlation Matrix for each class](https://github.com/NaderNarcisse/QSAR-biodegradation/blob/main/Pictures/Correlation_seperate_class.png "Correlation Matrix for each class")



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
```
Fitting 4 folds for each of 216 candidates, totalling 864 fits
Best params: {'C': 3, 'gamma': 0.2, 'kernel': 'rbf'}
Train Result:
================================================
Accuracy Score: 97.53%
_______________________________________________
CLASSIFICATION REPORT:
                    0           1  accuracy   macro avg  weighted avg
precision    0.983264    0.967611  0.975309    0.975437      0.975437
recall       0.967078    0.983539  0.975309    0.975309      0.975309
f1-score     0.975104    0.975510  0.975309    0.975307      0.975307
support    486.000000  486.000000  0.975309  972.000000    972.000000
_______________________________________________
Confusion Matrix: 
 [[470  16]
 [  8 478]]

Test Result:
================================================
Accuracy Score: 89.24%
_______________________________________________
CLASSIFICATION REPORT:
                    0           1  accuracy   macro avg  weighted avg
precision    0.927536    0.825688  0.892405    0.876612      0.893694
recall       0.909953    0.857143  0.892405    0.883548      0.892405
f1-score     0.918660    0.841121  0.892405    0.879891      0.892896
support    211.000000  105.000000  0.892405  316.000000    316.000000
_______________________________________________
Confusion Matrix: 
 [[192  19]
 [ 15  90]]

CPU times: user 676 ms, sys: 139 ms, total: 815 ms
Wall time: 7.99 s
```

### Random Forest
```
Fitting 3 folds for each of 144 candidates, totalling 432 fits
Best parameters: {'max_depth': 40, 'max_features': 2, 'min_samples_leaf': 1, 'min_samples_split': 9, 'n_estimators': 2000}
Train Result:
================================================
Accuracy Score: 97.22%
_______________________________________________
CLASSIFICATION REPORT:
                    0           1  accuracy   macro avg  weighted avg
precision    0.971253    0.973196  0.972222    0.972224      0.972224
recall       0.973251    0.971193  0.972222    0.972222      0.972222
f1-score     0.972251    0.972194  0.972222    0.972222      0.972222
support    486.000000  486.000000  0.972222  972.000000    972.000000
_______________________________________________
Confusion Matrix: 
 [[473  13]
 [ 14 472]]

Test Result:
================================================
Accuracy Score: 86.08%
_______________________________________________
CLASSIFICATION REPORT:
                    0           1  accuracy   macro avg  weighted avg
precision    0.915423    0.765217  0.860759    0.840320      0.865513
recall       0.872038    0.838095  0.860759    0.855067      0.860759
f1-score     0.893204    0.800000  0.860759    0.846602      0.862234
support    211.000000  105.000000  0.860759  316.000000    316.000000
_______________________________________________
Confusion Matrix: 
 [[184  27]
 [ 17  88]]

CPU times: user 5.28 s, sys: 269 ms, total: 5.55 s
Wall time: 3min 47s
```

## Summary

+ Support Vector Machine achieved an accuracy of **89 %**
+ Model is trained on a **balanced class dataset**, using Oversampling with the Synthetic Minority Oversampling Technique (SMOTE)
+ This model could be used as a Proof of Concept for the use of simulation on compounds to determine whether it is biodegradable or not.
