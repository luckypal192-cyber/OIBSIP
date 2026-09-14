# Sentiment Analysis

## Objective

The objective of this project is to build a machine learning model that classifies tweets into three sentiment categories: Positive, Negative, and Neutral.

## Dataset

The project uses a Twitter Sentiment Analysis dataset containing tweet-related information and sentiment labels.

The original dataset contains four sentiment labels:
- Positive
- Negative
- Neutral
- Irrelevant

For this project, only the three required sentiment classes — Positive, Negative, and Neutral — are used for machine learning classification.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Matplotlib
- Seaborn
- WordCloud
- Jupyter Notebook

## Data Preprocessing

The following preprocessing steps were performed:

1. Converted text to lowercase.
2. Removed URLs.
3. Removed punctuation.
4. Tokenized the text.
5. Removed English stopwords.
6. Removed records with missing tweet text.
7. Removed duplicate records.

## Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) was used to convert cleaned tweet text into numerical feature vectors.

Unigrams and bigrams were considered using the TF-IDF Vectorizer.

## Machine Learning Models

Two classification algorithms were implemented:

1. Multinomial Naive Bayes
2. Logistic Regression

The dataset was divided into 80% training data and 20% testing data using a stratified split.

## Model Evaluation

Both models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

## Visualizations

The project includes:

- Sentiment Distribution
- Negative Sentiment WordCloud
- Positive Sentiment WordCloud
- Neutral Sentiment WordCloud
- Naive Bayes Confusion Matrix
- Logistic Regression Confusion Matrix

## Error Analysis

Five misclassified examples were examined to understand possible reasons for incorrect predictions, including ambiguous language, sarcasm, mixed sentiment, short text, informal expressions, and context-dependent meaning.

## Conclusion

The sentiment analysis system successfully applies natural language processing and machine learning techniques to classify tweets into Positive, Negative, and Neutral sentiment categories.

The model with the higher F1-Score is considered the best-performing model for this task.

Sentiment analysis can be applied to social media monitoring, customer feedback analysis, customer satisfaction measurement, and understanding public opinions.