
# 🧠 Quora Question Pairs - Duplicate Detection

This project focuses on solving a classic Natural Language Processing (NLP) challenge: **determining whether two questions on Quora are duplicates of each other**. Duplicate detection is crucial in Q&A systems to reduce redundancy, improve search relevance, and enhance user experience.

Given a large dataset of over 400,000 question pairs, the objective is to build models that can accurately predict whether the two questions in each pair are semantically equivalent.

---

## 📌 Dataset

We use the [Quora Question Pairs dataset](https://www.kaggle.com/competitions/quora-question-pairs) from Kaggle.

**Dataset Details:**
- 400,000+ question pairs
- Binary target variable (`is_duplicate`: 1 if questions are duplicates, else 0)
- Varying lengths and complexity of question structures

---

## 🚀 Project Pipeline

The entire solution follows a structured pipeline:

### 1. **Data Preprocessing**
- Lowercasing, punctuation removal
- Stopwords removal
- Tokenization and stemming
- Removal of HTML tags, URLs
- Feature engineering (question lengths, number of common words, etc.)

### 2. **Model Building**

We explored three main approaches:

---

## 🛠️ Approaches Used

### ✅ 1. **TF-IDF + Traditional Machine Learning**

- Vectorized each question using TF-IDF
- Combined question vectors as input features
- Trained standard ML classifiers for binary classification

---

### ✅ 2. **Bag-of-Words (BoW) + Machine Learning**

- Represented each question using simple word frequency counts
- Engineered additional features like question length and common words
- Focused on lightweight yet interpretable models

---

### ✅ 3. **Deep Learning with LSTM and Pretrained Word2Vec**

- Created a shared embedding layer initialized with Word2Vec
- Used **shared LSTM layers** for both questions
- Final merged output passed through a Dense layer with sigmoid activation
- Goal: capture semantic similarity with deep sequence models

---

## 📊 Evaluation Metrics

We evaluated each model using:
- **Accuracy**
- **Confusion Matrix**

---

## 📌 Future Enhancements

- Integrate transformer-based models like **BERT** or **DistilBERT**
- Explore multilingual duplicate detection
