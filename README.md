# README for Question Classification Chatbot

## Project Overview

This project aims to classify questions into different categories as part of a chatbot application. The code is written in Python and uses various libraries and machine learning techniques.

## Project Components

### 1. Data Preparation

The project begins with data preparation, where you load the labeled questions from a CSV file using Pandas.

### 2. Preprocessing

The data preprocessing step is crucial for text data. The [Hazard Motevasel](https://www.sobhe.ir/hazm/) library is used for text preprocessing. The following steps are performed:
- Special character removal
- Tokenization
- Normalization
- Removing stopwords

### 3. Occurrence Table Generation

In this step, the code creates an occurrence table for words in the dataset. This table keeps track of how many times each word occurs in each class (label).

### 4. Naive Bayes Classifier

The Naive Bayes Classifier is responsible for predicting the label (category) of a given question. It uses Bayes' Theorem to calculate the probability of a question belonging to each label.

### 5. Validation

In the validation step, k-fold cross-validation is used to assess the classifier's performance. Precision, recall, and F1-score are calculated for each fold, and the average scores are reported.

### 6. Prediction

The prediction component is used to classify a set of new questions. The code reads new questions, preprocesses them, and uses the trained Naive Bayes Classifier to predict the labels for each question. The results are saved to a CSV file.

## Usage

To use this project for your own question classification task, follow these steps:

1. Prepare Your Data: Create a CSV file containing labeled questions. Ensure it contains a 'query' column for the text of the questions and a 'label' column for the corresponding labels.

2. Modify Data Loading: Update the code to load your dataset by replacing the file path in the `pd.read_csv` function.

3. Run Preprocessing: Review the preprocessing steps in the `Preprocess` class. You can modify the special character removal, stop words, or any other text processing steps according to your dataset's requirements.

4. Train the Model: You can adjust the k-fold validation settings in the `k_fold_validation` function to fit your dataset's needs. Once the model is trained, it will provide average precision, recall, and F1-score.

5. Make Predictions: Modify the 'prediction_result_to_csv' function to read and preprocess your new set of questions from a CSV file. Ensure that the 'condition_prob' and 'words' are calculated based on your training data. After making predictions, the results will be saved to a CSV file.

## Results

The project provides metrics to assess the model's performance, including precision, recall, and F1-score. You can use these metrics to evaluate how well the model classifies questions into different categories.

## Conclusion

This project is a robust starting point for building a question classification chatbot. It demonstrates the implementation of a Naive Bayes classifier, data preprocessing, and validation techniques. You can further enhance the model by optimizing preprocessing steps, tuning hyperparameters, and increasing the size and diversity of the training dataset.
