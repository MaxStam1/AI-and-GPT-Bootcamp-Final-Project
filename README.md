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
Please enter your NewsAPI key:
API Key: ··········
Loading models...
Device set to use cpu
Device set to use cpu
Device set to use cpu

Analyzing 10 articles about 'financial markets'...

Analyzing: Wealth strategies that used to be reserved for billionaires are becoming more accessible
URL: https://www.businessinsider.com/wealth-strategies-for-billionaires-are-becoming-more-accessible-2024-12
Asking to truncate to max_length but no maximum length is provided and the model has no predefined maximum length. Default to no truncation.

Processed: Wealth strategies that used to be reserved for billionaires are becoming more accessible
Summary: New tech is lowering the price of entry in fields like direct indexing and private markets. These personalized portfolios used to be out of reach.
Market Sentiment: 7.7/10 (Greed)
Main Topic: Technology Trends (confidence: 0.79)

Analyzing: Private credit firms are hot acquisition targets. As M&A ramps up next year, here are the firms likely to be bought.
URL: https://www.businessinsider.com/private-market-asset-management-deal-outlook-2024-12

Processed: Private credit firms are hot acquisition targets. As M&A ramps up next year, here are the firms likely to be bought.
Summary: Firms want more private market products to offer clients. Private credit firms with $30 billion to $70 billion in assets will be the firms to watch.
Market Sentiment: 6.8/10 (Greed)
Main Topic: Mergers & Acquisitions (confidence: 0.51)

Analyzing: AirPods to Be Made in India for the First Time Next Year
URL: https://www.macrumors.com/2024/12/13/airpods-made-in-india-from-next-year/

Processed: AirPods to Be Made in India for the First Time Next Year
Summary: Apple will begin making AirPods in India for the first time early next year. Foxconn will make the wireless earphones at a factory near Hyderabad in Telangana state.
Market Sentiment: 6.1/10 (Greed)
Main Topic: Risk Analysis (confidence: 0.21)

Analyzing: Upvest — which powers stock trading on Revolut, N26, Bunq — secures €100M
URL: https://thenextweb.com/news/upvest-which-powers-stock-trading-on-revolut-n26-bunq-secures-e100m

Processed: Upvest — which powers stock trading on Revolut, N26, Bunq — secures €100M
Summary: Upvest runs a stock-trading API that integrates into some of the biggest fintechs in Europe. Through these banks, some 50 million users have access use the company’s investment products.
Market Sentiment: 6.2/10 (Greed)
Main Topic: Market Sentiment (confidence: 0.19)

Analyzing: Stripe CFO joins the board of $3 billion AI startup Vercel
URL: https://www.businessinsider.com/stripe-cfo-steffan-tomlinson-joins-vercel-board-2024-12

Processed: Stripe CFO joins the board of $3 billion AI startup Vercel
Summary: Stripe's chief financial officer, Steffan Tomlinson, will serve as a director on Vercel's board. He was previously the CFO at several other tech startups, including Palo Alto Networks and Confluent.
Market Sentiment: 6.5/10 (Greed)
Main Topic: Company Earnings (confidence: 0.18)

Analyzing: 10 business leaders who spearheaded industry-transforming change in 2024
URL: https://www.businessinsider.com/transforming-business-executives-creating-change-media-tech-finance-transportation-2024-12

Processed: 10 business leaders who spearheaded industry-transforming change in 2024
Summary: Executives must understand how technological advancements, systemic barriers, and generational shifts are affecting their growth. Business Insider's annual list of people transforming business highlights these leaders who work in media, finance, technology, and labor.
Market Sentiment: 6.4/10 (Greed)
Main Topic: Market Analysis (confidence: 0.26)

Analyzing: Make These 4 Money Moves Before Thursday
URL: https://www.cnet.com/personal-finance/banking/make-these-4-money-moves-before-wednesday/

Processed: Make These 4 Money Moves Before Thursday
Summary: The Federal Reserve cut interest rates today. Knowing how to react can help you use these changes to your advantage. Here are four things you should do now to maximize your benefits.
Market Sentiment: 6.4/10 (Greed)
Main Topic: Economic Policy (confidence: 0.27)

Analyzing: Top Cheap Stocks Under $10 to Buy for Big Gains in 2025
URL: https://finance.yahoo.com/news/top-cheap-stocks-under-10-195800730.html

Processed: Top Cheap Stocks Under $10 to Buy for Big Gains in 2025
Summary: The Nasdaq jumped to another record on Monday. Wall Street bulls have pushed stocks higher throughout 2024 and off the market’s 2022 lows based on the outlook for lower interest rates and impressive, technology-driven earnings growth.
Market Sentiment: 8.7/10 (Extreme Greed)
Main Topic: Market Analysis (confidence: 0.36)

Analyzing: Where Does Corporate Climate Action Go Next?
URL: https://time.com/7202110/corporate-climate-action-in-2025/

Processed: Where Does Corporate Climate Action Go Next?
Summary: Companies have faced an onslaught from conservative activists, leading many businesses to go silent about their climate efforts. Public sentiment, which helped propel a lot of these efforts in the first place, hasn't been much help as of late.
Market Sentiment: 4.4/10 (Fear)
Main Topic: Risk Analysis (confidence: 0.38)

Analyzing: What's ahead for the markets in 2025, according to experts
URL: https://qz.com/2025-stock-market-predictions-analyst-sp500-djia-nasdaq-1851713886

Processed: What's ahead for the markets in 2025, according to experts
Summary: U.S. stocks rose in 2024, fueled by the unprecedented surge of artificial intelligence. Inflation also eased after a couple of years of persistent price pressure. The results of the presidential election provided an additional boost, propelling the Dow to record highs.
Market Sentiment: 8.7/10 (Extreme Greed)
Main Topic: Market Analysis (confidence: 0.36)


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
