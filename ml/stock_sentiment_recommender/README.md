# Stock Sentiment Recommender

## Overview
Stock Sentiment Recommender is an experimental project for predicting next-day stock actions at a daily granularity. The system produces one of five recommendations for each symbol: **Strong Buy**, **Buy**, **Hold**, **Sell**, or **Strong Sell**.

The project plans to combine traditional market data with large language models (LLMs) that read news and other unstructured text sources. By blending these signals, the recommender aims to capture both quantitative trends and qualitative sentiment that may influence price movements.

## Project Structure
```
ml/stock_sentiment_recommender/
├── data/        # scripts or datasets for historical price and news collection
├── lambda/      # placeholders for AWS Lambda functions used in deployment
├── offline/     # offline training and evaluation notebooks or scripts
├── sagemaker/   # artifacts related to Amazon SageMaker training jobs
└── utils/       # helper utilities and shared modules
```

## Getting Started
1. **Data Collection**: Populate the `data/` directory with historical market data and relevant news articles.
2. **Feature Engineering**: Develop utilities in `utils/` to transform raw data into model features, including embeddings from an LLM that analyzes daily news.
3. **Model Training**: Use the `offline/` workspace to prototype models that classify the next day's recommendation. Models may blend technical indicators with news-derived sentiment scores.
4. **Deployment**: Package models for inference via AWS Lambda or SageMaker once performance meets expectations.

## Incorporating an LLM
- Fetch daily news articles for the target stocks.
- Use an LLM to summarize and score sentiment or emerging events.
- Combine LLM outputs with quantitative indicators to form the final recommendation.

## Future Work
- Backtesting strategies to evaluate recommendation accuracy.
- Adding risk management and position sizing logic.
- Expanding to intra-day predictions or multi-day horizons.

This README will evolve as the project matures and additional components are implemented.
