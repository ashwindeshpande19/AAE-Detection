# African American BIAS IN HATE SPEECH DRTECTION


# Reducing Algorithmic Bias in Social Media

This project aims to reduce algorithmic bias in social media by replacing potentially offensive words with more neutral ones. 

## Data Collection

- Collected 100k tweets labeled as hate speech, abusive, normal, or spam 
- Fetched tweet text using Twitter API based on tweet IDs
- Performed exploratory analysis like emoji, stopword, and punctuation usage

## Model 1: Hate Speech Detection

- Preprocessed tweets with custom tokenization, normalization, and TF-IDF vectors
- Trained SVM model to classify tweets as hateful, abusive, normal, or spam
- Achieved 80% accuracy on test set

## Model 2: African American English Detection 

- Collected 100k tweets labeled as African American English (AAE) or not
- Trained Multinomial Naive Bayes model to detect AAE tweets
- Achieved 86% accuracy on test set

## Bias Mitigation

- Trained Word2Vec model on AAE tweets 
- Created replacement dictionary mapping offensive to neutral words
- Ran pipeline on 100k unseen tweets, replacing offensive words in AAE tweets
- 

## Results

- Converted over 26k previously hateful/abusive tweets to normal in 100k tweets
- Visualized class distribution changes showing conversion of many hateful and abusive tweets to normal after word replacement



