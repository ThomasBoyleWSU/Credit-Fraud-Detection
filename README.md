# Credit Card Fraud Detection Model
A machine learning project developed in R to detect fraudulent credit card transactions. This project compares the performance of the algorithms XGBoost, Random Forest, and Generalized Linear Models (GLM), on a highly imbalanced dataset.

# Project Overview
Credit card fraud detection is a classic imbalanced classification problem, where the number of fraudulent transactions is vastly outnumbered by legitimate ones. This project practices model building on a real-world dataset.

Key Result: The random forest model achieved an AUCPR score of 0.986, significantly outperforming other models and providing a highly effective solution for identifying fraud.

# Dataset
This project uses the Credit Card Fraud Detection dataset from Kaggle.

Dataset: [Kaggle Credit Source Data](https://www.kaggle.com/datasets/whenamancodes/fraud-detection)

Description: The dataset contains 284,807 transactions made by European cardholders over two days from September 2013.

Anonymization: For confidentiality purposes, features V1 through V28 had undergone a transformation through principal component analysis. The only original features that were not transformed are time, amount, and class. 

Class Imbalance: The dataset is highly imbalanced, with only 0.172% of transactions classified as fraudulent.

# Algorithms & Techniques
* Models Used: XGBoost (eXtreme Gradient Boosting), Random Forest, Generalized Linear Model (Binomial)

* Ensemble Methods: Leveraged built-in bagging (Random Forest) and boosting (XGBoost) techniques to enhance predictive accuracy and robustness.

* Hyperparameter Tuning: Optimized XGBoost performance using grid search with 5-fold cross-validation.

* Class Imbalance Handling: Addressed the severe class imbalance by utilizing the AUCPR metric, area under the precision-recall curve, instead of traditional accuracy, as it is more informative for datasets with a class imbalance.

# Tools & Libraries
Language: R

IDE: RStudio

Key Libraries:

* dplyr: Data transformation
* caret: Partitioning data for training
* PRROC: Calculating AUCPR metric and graphical representation
* randomForest: Building the random forest model
* xgboost: Building the XGBoost model
* glmnet: Building the GLM model
* kniter: Creating an html file

# Results
The primary metric for model evaluation was Area Under the Precision-Recall Curve (AUCPR) due to the extreme class imbalance in the data.

|Model|Score|Key Characteristics| 
|---|:---:|---|
|Random Forest| 0.9860211 | Bagging, Decision Trees|
|XGBoost (Untuned)| 0.8588341 | Gradient Boosting|
|XGBoost (Tuned)| 0.8615031 | Gradient Boosting, Grid Search, Cross-Validation|
|GLM (Binomial)| 0.747024 | Linear Modeling|
