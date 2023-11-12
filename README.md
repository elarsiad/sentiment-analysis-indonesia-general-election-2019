# Sentiment Analysis of Tweets from Indonesia's 2019 Election

## Overview

This project performs sentiment analysis on a dataset of tweets related to the 2019 Indonesian election. The goal is to classify tweet sentiment into positive, negative or neutral categories. 

The analysis goes through the typical NLP workflow:

- Data cleaning and preprocessing 
- Exploratory data analysis
- Feature extraction  
- Modeling 
- Evaluation

## Data Cleaning and Preprocessing

The raw tweet data is cleaned by:

- Removing URLs, hashtags, mentions
- Stripping punctuation and special characters 
- Converting slang words to formal text
- Removing stopwords
- Stemming words to their root form

The cleaned tweets are tokenized for feature extraction.

## Exploratory Data Analysis 

Stats and visualizations are created to understand data distributions, correlations, word frequencies etc. Word clouds illustrate most common terms for each sentiment class.

## Feature Extraction

The cleaned tweets are vectorized into numeric feature vectors using CountVectorizer. Only the most predictive unigrams are retained as features. 

## Models

### LSTM

- An LSTM layer with 8 units is used as the recurrent layer
- This is followed by dense layers to reduce dimensions
- Output layer has 3 units for softmax classification 
- Model is compiled with categorical crossentropy loss and RMSprop optimizer

### Random Forest

- CountVectorizer is used to vectorize tweets into feature vectors
- A Random Forest model with 200 trees is trained on the vectors

## Evaluation

Both models are evaluated on metrics like accuracy, confusion matrix, classification report etc. The LSTM model performs better with higher accuracy. Errors are analyzed to identify areas for improvement.

## Conclusion

The project shows how deep learning and classical ML models can be applied for text classification. The models can be improved further and deployed for real-time sentiment monitoring.