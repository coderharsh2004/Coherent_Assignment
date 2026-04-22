# Stock News Scraper and Sentiment Analyzer

## Overview

Stock market movements are significantly influenced by news sentiment. However, analyzing large volumes of financial news manually is inefficient and time-consuming.

This project presents an end-to-end solution that automates the process of collecting, processing, and analyzing stock-related news to determine sentiment. It combines web scraping, data preprocessing, and deep learning to classify news as Positive, Negative, or Neutral.

---

## Problem Statement

Investors and analysts struggle with:

* The overwhelming volume of financial news generated daily
* Difficulty in extracting actionable insights from unstructured text
* Lack of real-time sentiment understanding for decision-making

Without automation, identifying trends and reacting to market sentiment becomes inefficient and error-prone.

---

## Solution

This project builds a Stock Sentiment Analyzer that:

* Scrapes stock-related news from multiple sources using APIs and **BeautifulSoup for web scraping**
* Cleans and preprocesses textual data
* Constructs a structured and labeled dataset
* Trains a transformer-based NLP model
* Predicts sentiment for unseen news articles

---

## Project Pipeline

```
News Sources → Web Scraping (BeautifulSoup + APIs) → Data Preprocessing → Dataset Creation → Model Training → Sentiment Prediction
```

---

## Features

* Multi-source news collection using APIs and **BeautifulSoup-based web scraping**
* Large-scale dataset creation (20,000+ labeled samples)
* Text preprocessing using NLP techniques
* Fine-tuned BERT model for sentiment classification
* High accuracy (~89%) on test data
* Scalable pipeline for future extensions

---

## Data Sources

* NewsAPI
* NewsData.io
* Google News
* Yahoo Finance
* Alpha Vantage
* StockNewsAPI

---

## Tech Stack

**Programming Language:** Python

**Libraries and Tools:**

* **BeautifulSoup (core web scraping tool for extracting news content)**
* NLTK (text processing)
* HuggingFace Transformers
* PyTorch
* Pandas, NumPy

---

## Model Details

* Model: BERT (bert-base-uncased)
* Type: Transformer-based NLP model
* Task: Multi-class classification
* Classes: Positive, Neutral, Negative

### Performance

* Accuracy: 89%
* Balanced performance across classes
* Strong results on positive sentiment classification

---

## Workflow

### 1. Data Collection

* Retrieved news articles using APIs and **BeautifulSoup to scrape full article content from web pages**
* Filtered relevant articles using stock-related keywords

### 2. Data Preprocessing

* Converted text to lowercase
* Removed URLs, special characters, and noise
* Tokenized sentences using NLTK
* Removed duplicates and irrelevant entries

### 3. Model Training

* Tokenized text using BERT tokenizer
* Split dataset into training and testing (80:20)
* Fine-tuned using HuggingFace Trainer API

### 4. Prediction

```python
predict_sentiment("The stock market is crashing badly.")
# Output: Negative
```

---

## Dataset

* Size: 20,000+ labeled sentences
* Format: CSV
* Labels: Positive, Neutral, Negative
* Cleaned and preprocessed for training

---

## Challenges

* API rate limitations
* Filtering irrelevant or noisy data
* Handling class imbalance
* Extracting meaningful text from raw HTML using web scraping

---

## Future Work

* Real-time sentiment analysis dashboard
* Integration with stock price prediction models
* Improved performance on minority classes
* Deployment as a full-stack web application

---

## Conclusion

This project demonstrates how natural language processing and deep learning can be applied to financial data to extract meaningful insights. By leveraging **BeautifulSoup for web scraping** and transformer-based models, it enables automated and scalable sentiment analysis for stock market applications.

---

## Author

Harsh Bhartia
B.Tech Computer Science Engineering (AI/ML)
