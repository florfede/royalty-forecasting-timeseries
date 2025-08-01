# 🎵 Royalty Forecasting using Time Series Models

This project explores the use of different time series forecasting techniques to predict monthly royalty earnings for music artists based on historical data. The goal is to compare model performance and identify the best approach for supporting business decision-making in the music finance industry.

---

## 📊 Project Overview

Forecasting royalties accurately is crucial for financing music careers and managing risk. In this project, we analyze real-world artist earnings data and apply several models to predict future income:

- SARIMAX (Statistical Time Series)
- Prophet (Additive Model by Meta)
- XGBoost (Gradient Boosted Trees)
- LSTM (Neural Networks)

---

## 🧪 Dataset

The dataset contains anonymized monthly royalty data per artist over several years, including:

- `artist_id`: unique artist identifier
- `date`: monthly timestamp
- `royalties`: earnings in USD  
- External variables such as:
  - Number of releases
  - Followers
  - Social media sentiment (optional)

> 🛑 The raw data cannot be shared due to confidentiality, but an example file is available in the `data/` folder.

---

## ⚙️ Models & Methodology

Each artist's royalty time series is modeled individually. For each approach, we:

1. Preprocess the data (handle missing, outliers, etc.)
2. Train and evaluate models using MAE and MAPE
3. Store forecasts for Power BI visualization

Detailed notebooks are provided in the `notebooks/` folder.

---

## 📈 Results

We evaluate model performance by artist and globally:

| Model     | Mean MAE | Mean MAPE |
|-----------|----------|-----------|
| SARIMAX   | 415.3    | 21.7%     |
| Prophet   | 420.5    | 23.1%     |
| XGBoost   | 399.0    | 20.2%     |
| LSTM      | 390.7    | 19.4%     |

> 🔍 LSTM performed best on average, but XGBoost showed better interpretability and speed.

---

## 🧠 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/florfede/royalty-forecasting-timeseries.git
   cd royalty-forecasting-timeseries
