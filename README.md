# svm_classifier
This project uses the Support Vector Machine (SVM) algorithm to predict whether a loan application should be approved or rejected based on applicant information such as income, credit history, education and employment status.
# Loan Approval Prediction using Support Vector Machine (SVM)

## Project Overview

This project uses the Support Vector Machine (SVM) algorithm to predict whether a loan application should be approved or rejected based on applicant information such as income, credit history, education and employment status.

The goal is to build a classification model that helps financial institutions make data-driven loan approval decisions.

## Problem Statement

Loan approval is a critical decision for banks. Incorrect approvals may lead to financial loss while incorrect rejections may result in lost customers.

This project aims to:
- Analyze loan applicant data
- Build a classification model
- Predict loan approval status
- Evaluate model performance

## Dataset Information

Dataset: Loan Approval Dataset

Features include:

- Gender
- Married
- Dependents
- Education
- Self Employed
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area

Target Variable:

Loan_Status:
- Y → Approved
- N → Not Approved

## Technologies Used

Python  
Pandas  
NumPy  
Scikit-learn  
Matplotlib  
Seaborn  

## Machine Learning Algorithm

Support Vector Machine (SVM)

Why SVM?

SVM is effective for classification problems and works well for datasets with clear class separation. It finds the optimal hyperplane that maximizes the margin between classes.

## Hyperparameter Tuning

To improve model performance, hyperparameter tuning was performed on the SVM model. Parameters like kernel type, C value and gamma were adjusted to find the best performing model.

GridSearchCV was used to identify optimal parameters.

Example:

from sklearn.model_selection import GridSearchCV
from sklearn.svm import SVC

param_grid={
'C':[0.1,1,10],
'kernel':['linear','rbf'],
'gamma':['scale','auto']
}

grid=GridSearchCV(SVC(),param_grid,cv=5)

grid.fit(X_train,y_train)

print(grid.best_params_)

best_model=grid.best_estimator_

## Improvement Achieved

Hyperparameter tuning improved model accuracy and helped select the best kernel for classification.

## Key Learning

This demonstrated how tuning parameters significantly affects model performance and generalization ability.
