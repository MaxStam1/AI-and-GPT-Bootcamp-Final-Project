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
```
3. Install required packages:
pip install -r requirements.txt

## Usage
1. Run the Jupyter notebook:
```bash
jupyter notebook
```
2. Open the notebook and run the cells in order:
- Cell 1: Install required packages
- Cell 2: Load the analyzer class
- Cell 3: Run the analysis (you'll be prompted for your NewsAPI key)

## Example Output
```
Analyzing 5 articles about 'financial markets'...

Processed: Market Rally Continues Amid Strong Earnings
Summary: The stock market extended its gains as major companies reported better-than-expected earnings.
Market Sentiment: 8.5/10 (Greed)
Main Topic: Market Analysis (confidence: 0.89)
```

## How It Works
### Sentiment Analysis
- VADER provides rule-based sentiment scoring
- HuggingFace model adds deep learning-based analysis
- Combined score reflects both technical and contextual sentiment

### Topic Classification
Categories include:
- Market Analysis
- Company Earnings
- Economic Policy
- Technology Trends
- Mergers & Acquisitions
- Market Sentiment
- Risk Analysis

## Technologies Used
- Python: Primary programming language
- NLTK: Natural Language Processing toolkit
- HuggingFace Transformers: State-of-the-art NLP models
- NewsAPI: News article sourcing
- Plotly: Interactive visualizations
- Newspaper3k: Article text extraction

## Author
Max Stamakun
