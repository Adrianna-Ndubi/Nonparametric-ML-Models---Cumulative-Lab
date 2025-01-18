# Nonparametric-ML-Models---Cumulative-Lab
Overview
This project involves applying nonparametric machine learning models — k-nearest neighbors (kNN) and decision trees — to predict forest cover types based on cartographic variables. The dataset contains over 38,000 rows of land cell data labeled as either "Cottonwood/Willow" (1) or "Ponderosa Pine" (0). The objective is to identify the most accurate and efficient model through iterative experimentation.

Objectives
Preprocessing: Scale and prepare the data for modeling.
Baseline Models: Build and evaluate initial kNN and decision tree models.
Hyperparameter Tuning: Iteratively improve models by exploring various parameters.
Model Comparison: Evaluate performance metrics to select the best model.
Final Model Deployment: Train the selected model on the full dataset and evaluate its generalization.
Dataset Details
Source: UCI Machine Learning Repository (adapted).
Features: 52 columns including elevation, slope, distance metrics, wilderness areas, and soil types.
Target: Binary classification (Cover_Type: 0 or 1).
Imbalance: Majority class (0) constitutes ~93% of data.
Key Steps
Data Preparation:

Split dataset into training and testing sets with stratification.
Scale features using StandardScaler.
Baseline kNN Model:

Evaluated using cross-validated log loss.
Achieved log loss of 0.1296, slightly outperforming logistic regression.
Iterative kNN Improvements:

Tuned n_neighbors and metric hyperparameters.
Best log loss: 0.0634 (k=10, Manhattan distance).
Baseline Decision Tree Model:

Default settings yielded poor performance (log loss: 0.7352).
Iterative Decision Tree Improvements:

Tuned max_depth and min_samples_split.
Best log loss: 0.3463 (max_depth=10).
Final Model:

Selected kNN with n_neighbors=10 and Manhattan distance as the best performer.
Model trained and evaluated for deployment.
Results
Best Model: kNN with hyperparameters (n_neighbors=10, metric='manhattan').
Metrics:
Log Loss: 0.0634
Significant improvement over previous logistic regression and decision tree models.
