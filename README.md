# Sentiment Analysis of Genshin Impact Indonesian Reviews
## Machine Learning vs Deep Learning Comparison
### By Muhammad Auffa Hakim Aditya

This project presents a complete Natural Language Processing (NLP) pipeline for Sentiment Analysis of Indonesian user reviews of Genshin Impact collected from the Google Play Store.

The project was developed by Muhammad Auffa Hakim Aditya to compare the performance of Machine Learning and Deep Learning models in classifying sentiment in Indonesian text data.

------------------------------------------------------------

PROJECT OBJECTIVES

1. Scrape 40,000 Indonesian reviews from Google Play Store.
2. Perform text preprocessing for Indonesian language.
3. Apply lexicon-based sentiment labeling.
4. Compare performance between:
   - GRU (Deep Learning)
   - Word2Vec + LSTM (Deep Learning)
   - TF-IDF + SVM (Machine Learning)
5. Determine the best-performing model based on accuracy.

------------------------------------------------------------

DATASET INFORMATION

Source        : Google Play Store
Application   : Genshin Impact
Language      : Indonesian
Total Reviews : ~40,000

Scraping library used:
- google-play-scraper

------------------------------------------------------------

NLP PIPELINE

1. Data Cleaning
   - Remove URLs
   - Remove mentions and hashtags
   - Remove numbers
   - Remove punctuation and symbols

2. Case Folding
   - Convert all text to lowercase

3. Slang Word Normalization
   - Custom Indonesian slang dictionary
   - Genshin Impact specific terminology normalization

4. Tokenization
   - Using NLTK

5. Stopword Removal
   - NLTK Indonesian stopwords
   - NLTK English stopwords
   - Custom stopwords

6. Stemming
   - Using Sastrawi Stemmer

------------------------------------------------------------

SENTIMENT LABELING

Sentiment labeling is performed using a Lexicon-Based approach:

- Positive lexicon dictionary
- Negative lexicon dictionary
- Negation handling (e.g., "not", "never", etc.)

Sentiment classes:
- Positive
- Negative
- Neutral

------------------------------------------------------------

MODEL EXPERIMENTS

SCHEMA 1 — GRU (Deep Learning)
- Tokenizer + Padding
- Embedding Layer
- GRU Layer
- Dense + Dropout
- Softmax output (3 classes)

SCHEMA 2 — Word2Vec + LSTM (Deep Learning)
- Gensim Word2Vec training
- Embedding Matrix initialization
- LSTM Layer
- EarlyStopping
- Dense + Dropout

SCHEMA 3 — TF-IDF + SVM (Machine Learning)
- TfidfVectorizer
- Linear SVM
- Traditional ML classification pipeline

------------------------------------------------------------

MODEL EVALUATION

Models are evaluated using:
- Accuracy Score
- Performance comparison between ML and DL approaches

The best model is automatically selected based on highest accuracy.

------------------------------------------------------------

MODEL SAVING

All trained models are saved for reuse:

- .keras (Deep Learning models)
- .joblib (SVM and Tokenizers)
- .model (Word2Vec)

This allows easy deployment or inference on new data.

------------------------------------------------------------

TESTING WITH NEW SENTENCES

The project includes prediction testing on unseen review sentences after applying full preprocessing pipeline to ensure consistent inference.

------------------------------------------------------------

INSTALLATION

Install dependencies:

pip install -r requirements.txt

------------------------------------------------------------

HOW TO RUN

1. Clone repository:
   git clone https://github.com/YOUR_USERNAME/sentiment-analysis-genshin-impact-indonesia.git

2. Install requirements
3. Run the Python script or notebook

------------------------------------------------------------

AUTHOR

Muhammad Auffa Hakim Aditya

This project was developed as an exploration of:
- Natural Language Processing (NLP)
- Sentiment Analysis in Indonesian
- Machine Learning vs Deep Learning comparison
- Text Classification
- Word Embedding (Word2Vec)
- Sequence Modeling (GRU & LSTM)

------------------------------------------------------------

KEYWORDS (For Search Optimization)

Muhammad Auffa Hakim Aditya
Sentiment Analysis Indonesia
Indonesian NLP Project
Machine Learning Indonesia
Deep Learning Indonesia
Genshin Impact Sentiment Analysis
TF-IDF SVM Indonesia
Word2Vec LSTM Indonesia
Text Classification Project
NLP Portfolio Project

------------------------------------------------------------

Note:
This project is intended for educational and research purposes.
All review data is publicly available from Google Play Store.
