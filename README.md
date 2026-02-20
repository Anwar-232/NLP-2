# SMS-Spam-Classification-ML

  Overview
This project focuses on building a classification system using Natural Language Processing (NLP) techniques and Machine Learning algorithms to distinguish between legitimate (Ham) and unwanted (Spam) text messages.
This binary classification task is a critical step in message filtering systems designed to enhance user protection.
 
 Dataset
•	File Name: Spam_SMS.csv
•	Description: The dataset contains text messages labeled into two classes:
o	0: Ham (Legitimate Message)
o	1: Spam (Unwanted Message)
•	Size: Initially contained 5,574 messages.
 
 Methodology & Workflow
The following stages were followed to prepare and train the models:
1. Data Cleaning & Preparation
•	The message class (Class) was converted from text labels to numeric values (0 and 1) using LabelEncoder.
•	415 duplicate values were removed, resulting in 5,159 unique messages for analysis.
•	No missing values were found.
2. Exploratory Data Analysis (EDA)
•	Class Distribution: The data exhibited significant imbalance: 4,518 Ham messages versus 641 Spam messages.
•	Text Feature Analysis: New features (word count, character count, sentence count) were created. Analysis showed that Spam messages typically have a higher character and word count compared to Ham messages.
3. Text Preprocessing
A comprehensive transformation function (transform_text) was applied to the message content, including:
•	Lowercasing.
•	Tokenization.
•	Removal of non-alphanumeric characters.
•	Removal of Stopwords.
•	Stemming using PorterStemmer.
4. Feature Vectorization
Two main techniques were utilized to convert the processed texts into numerical arrays for model consumption:
•	Bag of Words (CountVectorizer): To count word frequencies.
•	TF-IDF (TfidfVectorizer): To weigh word importance across the corpus.
5. Model Training & Evaluation
Multiple Machine Learning algorithms were evaluated using both the CountVectorizer and 
TF-IDF feature sets.
Algorithms Used:
•	Multinomial Naive Bayes (MNB)
•	Support Vector Machine (SVM)
•	Random Forest
•	K-Nearest Neighbors (KNN)
•	Decision Tree
•	Logistic Regression
 
Results and Best Performance
The Multinomial Naive Bayes (MNB) model demonstrated superior performance for this classification task, particularly when trained on the CountVectorizer features.
Model	Text Representation Method	Accuracy	Precision
Multinomial Naive Bayes	CountVectorizer	97.4%	100%
Multinomial Naive Bayes	TF-IDF	97.2%	100%
Note: The 100% Precision score indicates that the model did not falsely classify any legitimate (Ham) message as Spam (False Positives), making it an extremely reliable model for message filtering applications.

