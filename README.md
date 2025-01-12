# SMS Spam Classifier Using Naive Bayes

This project implements an SMS spam classifier using the **Naive Bayes** algorithm to classify messages as either **spam** or **ham** (non-spam). The classifier is built from scratch with Python, utilizing basic data processing techniques, feature extraction, and machine learning methods.

## Project Overview

This project aims to develop a spam classifier for SMS messages using the **Naive Bayes** classifier, which is a probabilistic model based on Bayes' Theorem. The dataset used is the **SMS Spam Collection** from the UCI Machine Learning Repository, which contains a labeled collection of SMS messages classified as **ham** (non-spam) or **spam**.

- **Dataset**: [SMS Spam Collection Dataset](https://archive.ics.uci.edu/dataset/228/sms+spam+collection)
- **Algorithm**: Naive Bayes Classifier (Multinomial Naive Bayes)

The Naive Bayes classifier works by calculating the posterior probability of a message being spam or ham using Bayes' Theorem, based on the frequency of words in the message and the prior probabilities of spam and ham messages.

## Dataset

The **SMS Spam Collection** dataset consists of 5,574 SMS messages, labeled as either **spam** or **ham**. The dataset includes two columns:
- **Message**: The text content of the SMS message.
- **Label**: The classification label indicating whether the message is spam (1) or ham (0).

You can download the dataset from the UCI Machine Learning Repository: [SMS Spam Collection Dataset](https://archive.ics.uci.edu/dataset/228/sms+spam+collection).

## Features and Approach

The project uses the following steps to preprocess and classify the SMS messages:

1. **Data Preprocessing**:
   - The messages are read and labeled based on whether they are spam or ham.
   - Tokenization and vectorization of text data using **CountVectorizer**, which converts the SMS messages into a bag-of-words representation.

2. **Training the Model**:
   - **Naive Bayes** classifier is used, which calculates the likelihood of each word being associated with either spam or ham.
   - Laplace smoothing is applied to handle the possibility of words not appearing in the training set.
   
3. **Testing and Evaluation**:
   - The dataset is split into **training** and **test** sets.
   - Model evaluation is done using accuracy, precision, recall, and F1-score.
   - A **confusion matrix** is used to visualize the performance.

4. **Posterior Calculation**:
   - For each message, the likelihood of it being spam or ham is calculated using **Naive Bayes** formula, which incorporates the prior probabilities and likelihoods of each word.

## Getting Started

### Prerequisites

Ensure you have Python installed on your machine. You can install the necessary libraries via `pip`:

```bash
pip install -r requirements.txt
