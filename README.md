# Classification Challenge: Spam Email Detection

## Project Overview

This project aims to enhance the email filtering system for an Internet Service Provider (ISP) by developing a supervised machine learning (ML) model to accurately detect spam emails. The dataset consists of emails classified as either spam (1) or not spam (0). The objective is to create and evaluate two classification models, compare their performance, and identify the more accurate model for spam detection.

## Objectives

- Split the dataset into training and testing sets.
- Scale the features using `StandardScaler`.
- Create and evaluate a Logistic Regression model.
- Create and evaluate a Random Forest Classifier model.
- Compare the performance of both models to determine the better-performing model.

## Dataset

- **File**: `spam-data.csv` - Contains the dataset with email information.

## Project Setup

Before starting the challenge, the following steps were completed:

1. Created a new repository titled `classification-challenge`.
2. Cloned the repository to my local machine.
3. Added the starter file `spam_detector.ipynb` and pushed changes to GitHub.

## Instructions

The project was executed in the following steps:

### 1. Split the Data into Training and Testing Sets

- Loaded the data from the provided URL into a Pandas DataFrame.
- Predicted which model would perform better based on the strengths and weaknesses of the models.
- Created the labels set (`y`) from the "spam" column and the features DataFrame (`X`) from the remaining columns.
- Checked the class distribution of the labels (`y`) using `value_counts()` to assess dataset balance.
- Split the data into training and testing sets using `train_test_split`.

### 2. Scale the Features

- Created an instance of `StandardScaler` to scale the features.
- Fitted the scaler with the training data and transformed both the training and testing features.

### 3. Create a Logistic Regression Model

- Fitted a Logistic Regression model using the scaled training data (`X_train_scaled` and `y_train`), setting `random_state` to 1 for reproducibility.
- Made predictions using the testing data (`X_test_scaled`) and evaluated the model's performance using the accuracy score.

### 4. Create a Random Forest Model

- Fitted a Random Forest classifier model using the scaled training data (`X_train_scaled` and `y_train`).
- Made predictions using the testing data (`X_test_scaled`) and evaluated the model's performance using the accuracy score.

### 5. Evaluate the Models

**Model Performance:**

- Logistic Regression Accuracy: 0.92
- Random Forest Accuracy: 0.95

**Comparison of Model Performance:**

The Random Forest model outperformed the Logistic Regression model with an accuracy of 0.95 compared to 0.92. This aligns with my initial prediction that the Random Forest model would perform better due to its ability to handle non-linear relationships in the data more effectively.

## Conclusion

The Random Forest model demonstrated superior performance in detecting spam emails compared to the Logistic Regression model. Its ability to capture complex relationships in the data likely contributed to its higher accuracy score.