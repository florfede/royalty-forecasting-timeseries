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

Below is a detailed explanation of each variable used in the dataset:

| **Field**                    | **Description**                                                                             |
| ---------------------------- | ------------------------------------------------------------------------------------------- |
| `artist_id`                  | Unique identifier for the artist.                                                           |
| `date`                       | Date of the data record (monthly frequency).                                                |
| `royalties`                  | Amount of royalties the artist earned during the period.                                    |
| `instagram_followers`        | Total number of Instagram followers at the given date.                                      |
| `twitter_followers`          | Total number of Twitter followers at the given date.                                        |
| `track_release`              | Flag indicating whether the artist released a track during the period.                      |
| `sentiment`                  | Monthly sentiment score (from 0 to 1), calculated from the sentiment of Instagram comments. |
| `mentions_followers`         | Total number of Instagram followers from artists who mentioned the analyzed artist.         |
| `num_posts`                  | Number of Instagram posts made by the artist during the period.                             |
| `num_comments`               | Number of comments received on the artist’s Instagram posts during the period.              |
| `mean_royalties_6m`          | Average royalties over the past 6 months.                                                   |
| `std_instagram_followers_6m` | Standard deviation of Instagram followers over the past 6 months (measuring volatility).    |
| `growth_twitter_followers`   | Growth in Twitter followers compared to the previous period (absolute or %).                |
| `growth_instagram_followers` | Growth in Instagram followers compared to the previous period (absolute or %).              |
| `sum_track_releases_6m`      | Total number of tracks released in the last 6 months.                                       |
| `mean_sentiment_3m`          | Average Instagram comment sentiment over the past 3 months.                                 |
| `sum_mentions_followers_3m`  | Total `mentions_followers` over the past 3 months.                                          |
| `month`                      | Month being analyzed.                                                     |

The raw data is available in the `data/` folder.

---

## ⚙️ Models & Methodology

Each artist's royalty time series is modeled individually. For each approach, we:

1. Preprocess the data (handle missing, outliers, etc.)
2. Train and evaluate models using MAE and MAPE
3. Store forecasts for Power BI visualization

Detailed notebooks are provided in the `notebooks/` folder.

---

## 📈 Results

The model performance was evaluated both per artist and globally:

| Model     | Mean MAE   | Mean MAPE |
|-----------|------------|-----------|
| LSTM      | 28,129.29  | 12%       |
| XGBoost   | 29,293.74  | 13%       |
| SARIMAX   | 68,548.15  | 30%       |
| Prophet   | 236,606.38 | 104%      |

> 🔍 LSTM performed best on average, but XGBoost showed better interpretability and speed.

## 📁 Folder Structure

```
royalty-forecasting-timeseries/
│
├── data/              # Example data
├── notebooks/         # One notebook per model
├── outputs/           # Forecasts and metrics
├── src/               # Optional helper scripts
├── requirements.txt   # Python dependencies
└── README.md
```
---

## 🧪 How to Run

1. Clone the repo:
```bash
git clone https://github.com/tu-usuario/royalty-forecasting-timeseries.git
cd royalty-forecasting-timeseries
```

2. Install requirements:
```bash
pip install -r requirements.txt
```

3. Run each model notebook in `notebooks/`:
- `sarimax.ipynb`
- `prophet.ipynb`
- `xgboost.ipynb`
- `lstm.ipynb`

---

## 📚 Tech Stack

- Python
- pandas / numpy
- matplotlib / seaborn
- statsmodels / Prophet / XGBoost / TensorFlow
- Jupyter Notebook

---

## 👩‍💻 Author

**Florencia Federico**  
Data & Machine Learning Engineer  
[LinkedIn](https://www.linkedin.com/in/florenciafederico88/)
