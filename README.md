📊 Restaurant Review Sentiment Analysis Project
Project Overview

This project aims to analyze customer reviews for restaurants to determine the sentiment polarity—positive, negative, or neutral—and extract key insights like the most frequent words used in the reviews and the average review length. The core goal is to build a machine learning model that can automatically classify restaurant reviews as positive or negative.
📁 Dataset

    Source: restaurant_reviews.tsv file

    Format: Tab-separated values

    Columns:

        Review: Text data containing customer feedback.

        Liked: Binary target variable (1 for positive, 0 for negative).

🔍 Exploratory Data Analysis (EDA)

    Class Distribution:

        Visualized using countplot, showing a fairly balanced dataset.

        Distribution of review labels further explored with a histogram and boxplot.

    Review Length Analysis:

        Computed character counts for each review.

        Identified the longest review and displayed sample reviews.

🧹 Text Preprocessing

    Applied standard NLP cleaning techniques:

        Lowercasing

        Removing non-alphabetical characters

        Tokenization

        Stopword removal

        Stemming using PorterStemmer

    Stored the cleaned reviews in a corpus for modeling.

🧠 Feature Extraction

    Utilized Bag-of-Words model via CountVectorizer to convert text into numerical features.

    Resulting feature matrix shape: (number_of_reviews, vocabulary_size)

🔎 Sentiment Analysis
1. Naive Bayes Classifier

    Model: MultinomialNB

    Accuracy: Evaluated using accuracy_score, classification_report, and confusion_matrix.

2. Deep Learning Models

    RNN Model:

        Used Embedding and SimpleRNN layers for sequence modeling.

        Binary classification with sigmoid output.

        Trained for 10 epochs.

    LSTM Model:

        Replaced RNN with LSTM layer for better long-term dependency handling.

        Trained for 100 epochs.

    Both models were compiled with:

        Loss: Binary cross-entropy

        Optimizer: Adam

        Metrics: Accuracy

📈 Evaluation

    Accuracy and loss metrics printed after model training.

    Confusion matrix plotted for the Naive Bayes model.

    Comparative performance insights from traditional ML vs deep learning models.

📦 Model Deployment

    The final Naive Bayes model was saved using joblib as Restaurant_Review_Model.pkl for future deployment or integration into applications.
