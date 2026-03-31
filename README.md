# Logistic Regression Model for SUV Purchase Prediction

## Project Overview
This notebook demonstrates the process of building and evaluating a Logistic Regression model to predict whether a customer will purchase an SUV based on their Age and Estimated Salary. The project covers data loading, preprocessing, model training, evaluation, and visualization, along with explanations of core machine learning concepts.

## Table of Contents
1.  **Data Loading & Exploration**: Loading the dataset, displaying basic information (head, shape, columns), and checking data types and missing values.
2.  **Data Preprocessing**: Handling missing values (none found), encoding categorical variables (Gender), selecting relevant features ('Age', 'EstimatedSalary'), and separating features (X) and target (y).
3.  **Train-Test Split & Feature Scaling**: Splitting the dataset into training and testing sets (80/20, 70/30, 75/25 splits) and applying `StandardScaler` for feature standardization.
4.  **Model Training (Logistic Regression)**: Training a Logistic Regression model using `sklearn`.
5.  **Model Evaluation**: Predicting on test data and computing accuracy and confusion matrix.
6.  **Visualization**: Plotting the decision boundary of the Logistic Regression model for 2D features.
7.  **Model Improvement**: Experimenting with different train-test split ratios to observe their impact on model accuracy.
8.  **Interview Ready Questions**: Detailed explanations of Logistic Regression and the Confusion Matrix.

## Key Findings
*   The dataset contains `User ID`, `Gender`, `Age`, `EstimatedSalary`, and `Purchased` columns.
*   No missing values were found in the dataset.
*   The 'Gender' column was successfully encoded using `LabelEncoder`.
*   The highest accuracy achieved during the test size experimentation was **0.88 (88%)** with a 75/25 train-test split.
*   The confusion matrix provides insights into True Positives, True Negatives, False Positives, and False Negatives, highlighting the model's performance in correctly identifying purchases and non-purchases.
