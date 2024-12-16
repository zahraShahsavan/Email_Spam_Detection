# Email Spam Classification System

## Overview

This project implements an Email Spam Classification system using a Naive Bayes machine learning model. It processes an email dataset to train a spam classifier and provides functionalities to process the email text with nltk and predict whether a given email is spam or not.

---

## Features

- **Dataset Handling**: Automatically downloads and processes the Kaggle email spam dataset.
- **Preprocessing**: Tokenizes and cleans email text data for training and prediction with nltk SpaceTokenizer.
- **Model Training**: Uses the `MultinomialNB` classifier to train on email data.
- **Evaluation**: Outputs a confusion matrix, classification report, and F1 score to evaluate performance.
- **Prediction**: Predicts if a new email is spam or not using the trained model.
- **Serialization**: Saves the trained model for reuse without retraining.

---

## Requirements

Install the necessary dependencies:

```bash
pip install kagglehub pandas numpy scikit-learn nltk
```

Ensure you have access to the Kaggle dataset "balaka18/email-spam-classification-dataset-csv".

---

## Project Structure

- **`Email_Spam_Detection.ipynb`**: The main script containing the implementation.
- **`spam_model.pkl`**: The saved trained model (generated during execution).
- **`.gitignore`**: To manage the git files.
- **Input and Output**: User provides email content for prediction, and the system outputs the classification.

---

## How to Use

### Clone the Repository:

```bash
git clone https://github.com/your-repo/email-spam-classification.git
cd email-spam-classification
```

### Run the Script:

```bash
jupyter notebook Email_Spam_Detection.ipynb 
```

### Provide Email Content:

Run the codes one by one and enter the email content.

### View Results:

The script will classify the email as either "Spam" or "Not Spam."

---

## Dataset

The dataset is automatically downloaded from Kaggle using `kagglehub`:

- **Source**: [Email Spam Classification Dataset](https://www.kaggle.com/datasets/balaka18/email-spam-classification-dataset-csv)
- **Columns**:
  - `Email No.`: Identifier for emails.
  - `Prediction`: Label (1 for spam, 0 for not spam).
  - `3000 columns`: words that are used in the 5172 emails.

---

## Implementation Details

### Preprocessing:

- Converts email text to lowercase.
- Tokenizes the text using NLTK's `SpaceTokenizer`.

### Model:

- `MultinomialNB` from `scikit-learn` is used for classification.

### Evaluation Metrics:

- **Confusion Matrix**: Visualizes true positives, true negatives, false positives, and false negatives.
- **Classification Report**: Provides precision, recall, and F1 score.
- **F1 Score**: Balances precision and recall to measure model effectiveness.

### Prediction:

- User-provided email is tokenized and transformed into feature counts before classification.

