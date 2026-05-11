# Disaster-Tweets-Classification-Project

This project was developed for the TM340 Natural Language Processing assignment. The goal of the project is to classify tweets as either:

* **1 → Real Disaster**
* **0 → Not a Disaster**

The project demonstrates a complete NLP pipeline including text preprocessing, feature extraction using Bag of Words, model training with Naive Bayes, and evaluation using standard classification metrics.

---

# Project Objectives

* Load and explore the disaster tweets dataset.
* Clean and preprocess textual data.
* Convert text into numerical features using Bag of Words.
* Train a Machine Learning model for text classification.
* Evaluate model performance using multiple metrics.
* Discuss ambiguity challenges in NLP.
* Analyze ethical considerations in disaster detection systems.

---

# Dataset

The dataset used in this project is:

* `train.csv`

It contains:

* Tweet text
* Target labels

  * `1 = Real Disaster`
  * `0 = Not a Disaster`

Total records: **7613 tweets**

---

# Technologies and Libraries

The project was implemented using Python and the following libraries:

* Pandas
* NLTK
* Scikit-learn
* NumPy

---

# NLP Pipeline

## 1. Data Loading and Exploration

The dataset was loaded using Pandas and explored to:

* Display the first rows
* Check dataset size
* Analyze class distribution

---

## 2. Text Preprocessing

Text normalization steps included:

* Converting text to lowercase
* Tokenization using NLTK
* Removing punctuation
* Removing English stopwords

---

## 3. Feature Extraction

The cleaned text was transformed into numerical vectors using:

* **CountVectorizer (Bag of Words Model)**

Feature matrix shape:

> (7613, 21804)

---

## 4. Train-Test Split

The dataset was split into:

* 80% Training Data
* 20% Testing Data

Using:

```python
train_test_split(test_size=0.2, random_state=202520262)
```

---

## 5. Model Training

The classification model used was:

* **Multinomial Naive Bayes (MultinomialNB)**

The model was trained using the Bag of Words features.

---

## 6. Model Evaluation

Evaluation metrics included:

* Accuracy Score
* Confusion Matrix
* Precision
* Recall
* F1-Score
* False Negatives Analysis

### Model Accuracy

> 0.8024

---

# Ambiguity in NLP

A Bag of Words model has limitations because it ignores context and semantic meaning.

Example:

1. "There is a massive fire in the building!" → Real Disaster
2. "That new song is fire!" → Not a Disaster

---

# Ethical Considerations

This project discusses ethical challenges in NLP systems, including:

* Performance disparities across demographic groups
* Bias caused by non-diverse training data
* Risks of misclassifying emergency messages
* Potential downstream harm in disaster response systems

---

# Results Summary

| Metric             | Result                  |
| ------------------ | ----------------------- |
| Accuracy           | 80.24%                  |
| Model              | Multinomial Naive Bayes |
| Feature Extraction | Bag of Words            |
| Dataset Size       | 7613 Tweets             |

---

# Repository Structure

```text
├── TM340_.ipynb
├── train.csv
└── README.md
```


# Future Improvements

Possible future enhancements include:

* Using TF-IDF instead of Bag of Words
* Applying Deep Learning models such as LSTM or BERT
* Improving handling of slang and contextual language
* Reducing False Negatives for disaster detection


**Jomana Mohamed Hamed**
Natural Language Processing Project
