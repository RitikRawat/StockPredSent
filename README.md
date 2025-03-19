# 📈 Statistical Learning Stock Price Predictor

A machine learning-based project that predicts stock price movements by combining traditional financial indicators with sentiment analysis derived from social media (Twitter) data. Built as a part of the Design Project at IIIT Vadodara.

---

## 📖 Introduction

Stock prices are influenced not only by financial indicators but also by public sentiment and news. In today's world, social media is a powerful source of sentiment, where the crowd’s opinion can affect market trends.

This project aims to predict stock price behavior using:
- Historical stock data (open, high, low, close, volume)
- Sentiment features derived from Twitter
- Statistical and machine learning models

---

## 🎯 Objectives

- Predict stock price trends using machine learning models.
- Incorporate Twitter sentiment as a predictive feature.
- Compare performance with and without sentiment data.
- Improve on past models with better accuracy and generalization.

---

## 🔍 Literature Survey

- Prior research shows sentiment analysis improves stock price prediction accuracy.
- Earlier works reported accuracies of ~70–80% using classical models.
- Our goal: surpass those benchmarks using combined feature engineering and optimized learning models.

---

## 🧠 Methodology

### 🔹 Step 1: Financial Feature Analysis

- Collected daily stock features: `Date`, `Open`, `High`, `Low`, `Close`, etc.
- Trained models like:
  - **Linear Regression** → Error ≈ 1.325
  - **Random Forest** → Error ≈ 0.868

### 🔹 Step 2: Twitter Sentiment Analysis

- Collected tweets using **Tweepy API** (past 24 hours).
- Preprocessed tweets for noise reduction.
- Used **WordNet** and **SentiWordNet** for sentiment scoring.
- Extracted features:
  - `Positivity Score`
  - `Negativity Score`

### 🔹 Step 3: Tweet Embedding

- Used a variation of **Word2Vec** to embed tweets.
- Generated weighted averages of tweet vectors across time spans.

### 🔹 Step 4: Model Training

- Tried various models; best results with:
  - **LSTM (Long Short-Term Memory)** neural network
- Configuration:
  - **Activation**: tanh  
  - **Optimizer**: RMSprop  
  - **Epochs**: 500

---

## 📊 Results

- Average model accuracy: **~90%**
- LSTM outperformed traditional regression-based models.
- Models trained with sentiment features performed significantly better than those without.

---

## ✅ Conclusion

- Public sentiment on platforms like Twitter plays a key role in stock price behavior.
- Combining financial and sentiment data improves prediction accuracy.
- Our model was able to reasonably predict **stock behavior**, if not exact prices.

---

## 🔮 Future Work

- Train on longer historical windows (more than one day).
- Expand to multiple companies across sectors.
- Deploy as a live application or alert system.
- Use real-time sentiment streams for intraday predictions.

---

## 🧑‍🤝‍🧑 Team Members

- **Vikash Choudhary** (201851144)  
- **Himanshu Bhadu** (201851048)  
- **Ritik Rawat** (201851102)  
- **Noorul Hasan Ali** (201851078)  

### 🎓 Institution

*Indian Institute of Information Technology Vadodara*  
Government Engineering College, Sector-28, Gandhinagar, Gujarat - 382028  

---

## 👨‍🏫 Supervisor

**Dr. S.K. Patra**  
IIIT Vadodara

---

## 📚 References

1. [Illustrated Guide to LSTM’s and GRU’s – Michael Phi (Towards Data Science)](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21)  
2. [Stock Market Prediction Using Twitter Sentiment Analysis – Stanford](http://cs229.stanford.edu/proj2011/GoelMittal-StockMarketPredictionUsingTwitterSentimentAnalysis.pdf)  
3. [Machine Learning for Stock Prediction – Towards Data Science](https://towardsdatascience.com/machine-learning-for-stock-prediction-a-quantitative-approach-4ca98c0bfb8c)  
4. [Tweepy Documentation – Python Twitter API](https://www.tweepy.org/)  
5. [SentiWordNet](https://github.com/aesuli/SentiWordNet)  

---

> 📂 For more details, refer to the full project report: [`DesignProject-Report.pdf`](./DesignProject-Report.pdf)
