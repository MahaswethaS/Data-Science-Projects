# Product Review : Sentiment Analysis & Keyword Extraction

This project dives into Flipkart product reviews ( taken from Kaggle) to extract meaningful customer insights.
By combining sentiment analysis with keyword extraction, we identify which product categories are *loved* by users — and which ones *need attention* — based on their feedback.

---

## 1. Data Cleaning

- Loaded and parsed the raw Flipkart dataset (`Dataset.csv`)
- Dropped missing or irrelevant entries
- Created a custom function to **assign each product to a category** based on keywords in the product name
- Saved the cleaned and categorized dataset as `flipkart_with_categories.csv`

> Result: Structured and usable product review data with associated categories

---

## 2. Sentiment Analysis

- Used **VADER SentimentIntensityAnalyzer** (from NLTK) to calculate:
  - Compound sentiment scores
  - Categorize reviews as **positive**, **negative**, or **neutral**
- Aggregated sentiment results at the category level to compute:
  - **Sentiment distribution**
  - **Net sentiment score** per category

> Output Files:
- `flipkart_sentiment_per_review.csv`  
- `sentiment_counts_by_category.csv`

---

## 3. Keyword Extraction

- Applied **YAKE (Keyword Extractor)** to extract the top 5 single-word keywords per review
- Combined and aggregated keywords at the category level
- Used `collections.Counter` to count top keywords per category
- Generated **word clouds** for each major category

> Output Files:
- `flipkart_sentiment_keywords.csv`  
- `top_keywords_by_category.csv`  
- PNG word clouds per category

---

## 4. Insights

- Identified **"Highly Loved"** categories with >70% positive reviews
- Highlighted **"Needs Attention"** categories based on lowest sentiment scores
- Created clear visualizations:
  - Bar plots of top positive/negative categories
  - Horizontal sentiment comparison chart
  - Word clouds to visualize customer focus areas

> Loved Categories: e.g., "Beauty and Skin Care", "Stationery and Crafts"  
> Attention Needed: e.g., "Sports and Apparel", "Toys"

---

## 5. Conclusion

This project bridges the gap between raw e-commerce reviews and actionable business insight. By categorizing reviews, analyzing their sentiment, and extracting their most common themes, we provide a data-driven lens into customer satisfaction across product lines.

---

## Tech Stack

- **Python** (Pandas, Seaborn, Matplotlib)
- **VADER** (from NLTK)
- **YAKE** (Keyword extraction)
- **WordCloud**
- **Google Colab**

---
