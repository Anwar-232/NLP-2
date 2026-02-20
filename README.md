#  SMS Spam Classification: Traditional ML Approach

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn">
  <img src="https://img.shields.io/badge/NLP-Traditional_ML-orange?style=for-the-badge" alt="NLP">
  <img src="https://img.shields.io/badge/Data_Visualization-Seaborn-blue?style=for-the-badge" alt="Visualization">
</p>

##  Project Overview
This project implements a robust pipeline for detecting SMS spam using foundational Machine Learning techniques. It demonstrates the complete lifecycle of an NLP project, from exploratory data analysis (EDA) and text cleaning to feature extraction and model benchmarking.

The primary objective is to compare how different text representation methods (**Bag of Words** vs. **TF-IDF**) affect the performance of classical classifiers like **Naive Bayes**, **Logistic Regression**, and **SVM**.

---

##  Exploratory Data Analysis (EDA)
- **Class Distribution:** Visualized using pie charts to handle potential class imbalance.
- **Text Metrics:** Engineered features like `num_characters`, `num_words`, and `num_sent` to analyze the structural differences between Spam and Ham messages.
- **Visual Insights:** Used Seaborn histograms and pair plots to reveal that Spam messages typically contain significantly more characters and words.

---

##  Data Preprocessing & NLP Pipeline
A custom transformation function was developed to clean the raw text:
1. **Lowercasing:** Standardizing text format.
2. **Tokenization:** Breaking text into individual words.
3. **Alphanumeric Filtering:** Removing special characters and noise.
4. **Stopword Removal:** Filtering out common English words (e.g., "the", "is") that don't add semantic value.
5. **Stemming:** Using `PorterStemmer` to reduce words to their root form (e.g., "loving" -> "love").

---

##  Model Benchmarking
The project compares three major algorithms across two vectorization strategies:

| Vectorizer | Algorithms Evaluated |
| :--- | :--- |
| **Bag of Words (CountVectorizer)** | Naive Bayes (Multinomial), Logistic Regression, SVM |
| **TF-IDF (TfidfVectorizer)** | Naive Bayes (Multinomial), Logistic Regression, SVM |

###  Metrics Captured
- **Accuracy Score**
- **Precision Score** (Crucial for Spam detection to minimize False Positives)
- **Recall & F1-Score**
- **Confusion Matrix**

---

##  Visualizations
- **Word Clouds:** Generated specifically for Spam and Ham corpuses to identify high-frequency keywords (e.g., "Free", "Win", "Call" in Spam).
- **Top 30 Words:** Bar plots for frequency analysis of the spam corpus.

---

##  How to Run
1. **Clone the repo:** `git clone https://github.com/Anwar-232/SMS-Spam-Classification-ML`
2. **Install Dependencies:** `pip install pandas numpy scikit-learn nltk seaborn matplotlib wordcloud`
3. **Data:** Ensure `Spam_SMS.csv` is in the project directory.
4. **Run:** Execute the notebook to see the comparative analysis of the models.
