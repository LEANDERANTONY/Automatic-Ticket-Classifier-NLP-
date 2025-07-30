# 📨 Automatic Ticket Classifier using Topic Modeling and Supervised Learning

This project builds a pipeline to classify customer complaint tickets into product/service-based categories using NLP techniques. It combines **unsupervised topic modeling** with **supervised learning** to enable scalable and accurate routing of support queries.

---

## 🧠 Problem Statement

How can we automatically classify unlabeled customer complaints into relevant service departments?

Using topic modeling on unlabeled complaint data, we identify key themes and map them to five major clusters:

- Credit Card / Prepaid Card  
- Bank Account Services  
- Theft / Dispute Reporting  
- Mortgages / Loans  
- Others

These cluster labels are then used to train a classification model that can categorize new incoming tickets automatically.

---

## 📁 Dataset

- Format: JSON
- Size: ~22,000 complaint records
- Key Field: `complaint_what_happened` (text of complaint)
- Cleaning: Removed null and empty complaints

---

## 🔍 Preprocessing

- Text cleaning with regex
- Tokenization, Stopword removal
- Lemmatization using spaCy and NLTK
- Vectorization using **TF-IDF**

---

## 📊 Unsupervised Learning

Used **Non-negative Matrix Factorization (NMF)** to extract latent topics.

- Topics = 5
- Topic-term mapping visualized using word clouds
- Manually assigned topic labels based on dominant terms

---

## 📈 Supervised Classification

Once topic labels were assigned:

- Split data into train/test
- Trained **Logistic Regression**, **Random Forest**, and **Multinomial Naive Bayes**
- Evaluated using Accuracy, Precision, Recall, and F1-score

Best model: **Logistic Regression**  
Validation Accuracy: **~85%**

---

## 📦 Requirements

The tools used for this analysis are available here [requirements.txt](requirements.txt)

