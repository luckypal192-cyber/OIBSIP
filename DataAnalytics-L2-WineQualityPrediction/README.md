# Wine Quality Prediction

## Project Overview

This project focuses on predicting the quality of red wine using machine learning techniques.

The wine quality is predicted based on various physicochemical properties of wine such as acidity, sugar, sulphates, alcohol, pH, density, and chlorides.

The project also compares three different classification algorithms to identify the best-performing model.

## Objective

The main objectives of this project are:

- Analyse the Wine Quality dataset.
- Perform exploratory data analysis (EDA).
- Understand the distribution of wine quality scores.
- Analyse relationships between physicochemical properties and wine quality.
- Convert wine quality scores into meaningful classification categories.
- Train multiple machine learning classification models.
- Evaluate and compare the performance of the models.
- Identify the most suitable model for deployment.
- Analyse feature importance using the Random Forest model.

## Dataset

The project uses the Wine Quality - Red Wine dataset from the UCI Machine Learning Repository.

The dataset contains 1,599 red wine samples with physicochemical measurements and a wine quality score.

### Features

The dataset contains the following input features:

- Fixed Acidity
- Volatile Acidity
- Citric Acid
- Residual Sugar
- Chlorides
- Free Sulfur Dioxide
- Total Sulfur Dioxide
- Density
- pH
- Sulphates
- Alcohol

### Target Variable

- `quality`

The original quality score ranges from 3 to 8 in the dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Exploratory Data Analysis

The dataset was analysed using:

- Dataset shape and column inspection
- Descriptive statistics
- Missing-value analysis
- Duplicate-value analysis
- Wine quality distribution
- Correlation analysis
- Feature relationship visualization

### Visualizations

The following visualizations were created:

1. Wine Quality Distribution
2. Correlation Heatmap
3. Alcohol Content by Wine Quality

## Feature Engineering

The original wine quality scores were converted into three categories to formulate the problem as a multi-class classification task.

The categories used were:

| Quality Score | Category |
|---|---|
| 3–5 | Low |
| 6 | Medium |
| 7–8 | High |

This grouping allows the model to classify wines into Low, Medium, or High quality categories.

## Train-Test Split

The dataset was divided into training and testing sets using an 80:20 split.

A stratified split was used to preserve the class distribution in both the training and testing datasets.

- Training Data: 80%
- Testing Data: 20%
- Random State: 42

## Machine Learning Models

Three classification algorithms were trained as required for the project:

### 1. Random Forest Classifier

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve prediction performance.

### 2. SGD Classifier

Stochastic Gradient Descent (SGD) is an efficient linear classification algorithm used for classification tasks.

### 3. Support Vector Classifier (SVC)

SVC finds an optimal decision boundary that separates different classes in the feature space.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

The confusion matrices were visualized to understand the classification performance of each model.

## Model Comparison

The performance of the three models was compared based on their accuracy.

The results showed that:

**Random Forest achieved the highest accuracy of 75.62%.**

Therefore, Random Forest performed better than SGD Classifier and Support Vector Classifier on the test dataset.

## Feature Importance

Feature importance was calculated using the Random Forest model.

The feature importance chart helps identify which physicochemical properties contribute most to the prediction of wine quality.

The top important features were visualized using a horizontal bar chart.

## Screenshots

The `screenshots` folder contains the following visualizations:

- `01_wine_quality_distribution.png`
- `02_correlation_heatmap.png`
- `03_alcohol_vs_quality.png`
- `04_confusion_matrices.png`
- `05_random_forest_feature_importance.png`
- `06_model_comparison.png`

## Conclusion

A machine learning classification pipeline was successfully developed to predict red wine quality using physicochemical properties.

The original wine quality scores were converted into three categories: Low, Medium, and High.

Three classification models were trained and evaluated:

- Random Forest Classifier
- SGD Classifier
- Support Vector Classifier (SVC)

The models were evaluated using accuracy, precision, recall, F1-score, classification reports, and confusion matrices.

Among the three models, **Random Forest achieved the highest accuracy of 75.62%**.

Therefore, Random Forest was selected as the most suitable model for deployment among the tested models because it provided the best classification accuracy and also provided feature importance information for understanding the factors associated with wine quality prediction.

This project demonstrates how machine learning can be applied to wine quality prediction and data-driven analysis of physicochemical wine characteristics.