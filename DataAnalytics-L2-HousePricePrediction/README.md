# House Price Prediction Using Linear Regression

## Objective

The objective of this project is to build a machine learning model to predict house sale prices using Linear Regression.

## Dataset

The project uses the Ames Housing dataset from the Kaggle House Prices competition.

The dataset contains information about residential properties, including numerical and categorical features, with `SalePrice` as the target variable.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Exploratory Data Analysis

The following EDA steps were performed:

1. Dataset shape and column inspection.
2. Descriptive statistical analysis.
3. Missing-value analysis.
4. SalePrice distribution visualization.
5. Correlation analysis.
6. Correlation heatmap.
7. Identification of highly correlated numerical features.

## Data Preprocessing

The following preprocessing techniques were applied:

- Numerical missing values were handled using median imputation.
- Categorical missing values were represented using `"None"`.
- Categorical variables were converted into numerical features using one-hot encoding.
- `SalePrice` was used as the target variable.

## Train-Test Split

The dataset was divided into:

- 80% Training Data
- 20% Testing Data

A random state of 42 was used to make the results reproducible.

## Machine Learning Model

### Linear Regression

Linear Regression was trained using the processed features to predict house sale prices.

## Model Evaluation

The model was evaluated using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

## Visualizations

The project includes:

- Sale Price Distribution
- Correlation Heatmap
- Actual vs Predicted House Prices
- Model Evaluation Metrics

## Conclusion

The project demonstrates how exploratory data analysis, data preprocessing, feature encoding, and Linear Regression can be used to build a house price prediction model.

The Actual vs Predicted visualization provides a visual comparison between the model's predictions and the actual house sale prices.