# Iris-ML
PROJECT OVERVIEW:
1.	In this particular project, the famous iris dataset was picked up from kaggle. 
2.	The iris dataset, is a table of features of 4 different species of a particular plant.
3.	The dataset includes length of different parts common to each species.
4.	The usual accuracy for this dataset is ~96% but using K-Folds I was able to take the accuracy to ~98%.
5.	The dataset was explored for null values, outliers and missing values.
6.	The anomalies in the dataset were rectified by omitting NaN values, treating outliers using Univariate and Bivariate analysis and the missing values were imputed using the column mean.
7.	The visualization of the dataset, was done using seaborn and matplotlib libraries defined previously in the python language.
8.	Different Machine Learning techniques were applied for classisfication:
Logistic regression
SVM
Decision Tree
Random forest 
And by using Kfold technique the accuracy was increased. 

PROBLEM:
When evaluating hyperparameters for estimators, such as the |C| setting that must be manually set for a Support vector machine, there is a potential risk of overfitting the model on the test set because the parameters can be easily changes until the estimator performs in an optimal condition. Therefore, during this the test set might “leak” into the model and evaluation metrics would no longer give a true picture of the general performance of the model. To solve this problem, another part of the dataset is held out called as the “validation set”: training proceeds on the training set, after which evaluation is done on the validation set, and when the accuracy of the model is close to required, final evaluation is done on the test set.
However, by partitioning the available data into three sets, the number of samples are reduced drastically, which can be used for better learning of the model, and these results can depend on a particular random choice for the pair of (train, validation) sets.

SOLUTION:
A solution to this problem is a procedure called cross-validation. A test set should still be held out for final evaluation, but the validation set is no longer needed when doing CV. In the k-fold CV approach, the training set is split into k smaller sets (other approaches are described below, but generally follow the same principles). The following procedure is followed for each of the k “folds”:
•	A model is trained using k−1 of the folds as training data;

•	the resulting model is validated on the remaining part of the data (i.e., it is used as a test set to compute a performance measure such as accuracy).

The performance measure reported by k-fold cross-validation is then the average of the values computed in the loop. This approach can be computationally expensive, but does not waste too much data (as is the case when fixing an arbitrary validation set), which is a major advantage in problems such as inverse inference where the number of samples is very small.
