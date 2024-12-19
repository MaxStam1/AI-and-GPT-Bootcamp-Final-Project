# Financial News Summarizer and Sentiment Analyzer

## Description
This project analyzes financial news articles using Natural Language Processing (NLP) techniques to provide insights about market sentiment. It combines multiple sentiment analysis approaches with topic classification to give a comprehensive view of financial news, similar to CNN's Fear and Greed Index.

## Features
- **News Fetching**: Automated retrieval of latest financial news using NewsAPI
- **Text Summarization**: Generates concise summaries using BART-large-CNN model
- **Dual Sentiment Analysis**: 
  - VADER (Valence Aware Dictionary and sEntiment Reasoner)
  - HuggingFace's sentiment analysis model
- **Topic Classification**: Categorizes articles into relevant financial topics
- **Market Sentiment Score**: Custom 1-10 scale indicator inspired by the Fear and Greed Index
- **Interactive Visualizations**: 
  - Market sentiment gauge
  - Topic distribution chart
  - Sentiment comparison graphs

## Installation

### Prerequisites
- Python 3.7 or higher
- NewsAPI key (Get it from [newsapi.org](https://newsapi.org))

### Setup
1. Clone the repository:
```bash
git clone https://github.com/MaxStam1/AI-and-GPT-Bootcamp-Final-Project.git
