# Project README

## Title

**The Impact of Financial Aid and Academic Pathways on Student Success: Analytics, Predictive Modeling, and Interactive Tools**


## Overview

The project creates an extensive predictive analytics system which investigates how financial assistance and academic preparedness and student enrollment choices affect undergraduate students' ability to graduate. The project analyzes 25,926 student records which combine demographic details with high school achievements and AP coursework and placement test results and standardized test scores and financial aid information spanning multiple academic years to develop machine learning models for institutional decision support.

## Key Features

The system integrates academic records with demographic information and financial aid data through end-to-end data processing.

The system performs complete data preparation through cleaning operations and deduplication and leakage prevention and feature engineering steps.

The system implements machine learning modeling through logistic regression and random forest and gradient boosting and XGBoost and SVMs and Naïve Bayes.

The optimized XGBoost model achieved a test data AUC score of 0.846.

The system provides users with model interpretation tools which include feature importance analysis and partial dependence plots and policy simulations and categorical gap analysis.

The system integrates with Power BI to deliver real-time prediction capabilities and threshold adjustment tools and scenario modeling functions.

## Dataset Description

The financial aid dataset contains 25,960 records which combine student demographics with high school information and placement test results and standardized test scores and FAFSA need assessment and six years of financial aid disbursements.

The AP Dataset contains 58,246 records which show all student AP exam attempts distributed across seven academic subjects.

The merged dataset contains 25,926 students after completing data preprocessing and deduplication and left-join operations.

The modeling dataset contains 33 pre-enrollment and first-term attributes which were selected from the 157-feature merged dataset.

### Data Processing Highlights

The system replaces missing numeric values with zeros and categorical values with "Unknown" during processing.

The system transforms AP data into multiple formats which include exam attempt counts and credit points and average grades and STEM-focused performance indicators.

The system generates financial support features which include SupportBin and TotalSupport and NeedStatus and Supported.

The system implemented leakage prevention to prevent any future information from entering the modeling process.

## Modeling Framework

The system divides data into three parts for training and validation and testing through stratified sampling at 70/15/15 ratios.

The system applies median imputation and z-score normalization and one-hot encoding to the data during preprocessing.

The system uses Accuracy and Precision and Recall and F1-Score and AUC as its evaluation metrics.

The system tested five machine learning algorithms including Logistic Regression and Random Forest and Gradient Boosting and XGBoost and Linear SVM and RBF SVM and Gaussian Naïve Bayes.

The system performed PCA dimensionality reduction but removed it because it caused performance deterioration.

The system used RandomizedSearchCV to optimize hyperparameters for tree-based models.

## Model Results

The XGBoost model achieved its best results after hyperparameter optimization.

The model achieved 0.7578 accuracy and 0.7400 precision and 0.7869 recall and 0.7627 F1 score and 0.8456 AUC.

### Key Predictors Identified

The model shows that English placement scores and ALEKS math placement scores and SAT Math and Reading/Writing scores and total financial support and high-support funding bins above $20,000 and transfer student status and high school GPA and rank percentile are the most important factors for graduation success.

## Interpretability and Insights

### Feature Importance

The models show that academic readiness and financial support and student transfer status determine graduation success rates most strongly.

### Categorical Gap Analysis

The models show consistent patterns which indicate:

Students who transfer to the institution achieve better results than students who enter as freshmen.

The academic performance of female students exceeds that of male students.

The models show significant performance variations between different student ethnic groups.

The level of financial support stands as the most influential factor among all categorical variables.

### Policy Simulations

The simulated changes show that:

Students who transfer to the institution and students who receive more financial aid and students with better high school grades achieve better results.

The model shows negative results when institutions reduce financial aid and when students perform poorly academically and when they are labeled as new freshmen.

## Power BI Deployment

The XGBoost model operates within Power BI through Python-based inference to deliver three main functions:

The system generates instant predictions for students based on their individual characteristics.

The system enables users to modify threshold values which helps institutions adjust their policies.

The system enables users to create different scenarios for financial aid and academic policy development.

## Conclusions

The research proves that machine learning models which receive proper data cleaning and interpretation methods can successfully predict student graduation rates using only information available before students start their studies. The operational Power BI dashboard provides universities with an operational tool for financial aid planning and early student intervention and strategic advising programs.

