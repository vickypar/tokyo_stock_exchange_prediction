# JPX Tokyo Exchange Prediction
![image](https://user-images.githubusercontent.com/95586847/172226164-435897a7-0236-4f58-be8a-dd58b13d1e55.png)

## Authors

- Vasiliki Chrysovalanto Parousidou
- Zoi Chatzichristodoulou (@zoichatzi)
- Charilaos Kaliakatsos

## Table of Contents

[0. Installation](https://github.com/vickypar/tokyo_stock_exchange_prediction#0-installation)

[1. Semantics](https://github.com/vickypar/tokyo_stock_exchange_prediction#1-semantics)

[2. About](https://github.com/vickypar/tokyo_stock_exchange_prediction#2-about)

[3. Competition Overview](https://github.com/vickypar/tokyo_stock_exchange_prediction#3-competition-overview)

[4. About Our Approach](https://github.com/vickypar/tokyo_stock_exchange_prediction#4-about-our-approach)

[5. Performance of the Models](https://github.com/vickypar/tokyo_stock_exchange_prediction#5-performance-of-the-models)

[6. icensing and Refferences](https://github.com/vickypar/tokyo_stock_exchange_prediction#6-licensing-and-refferences)


## 0. Installation 


The code requires Python versions of 3.* and general libraries available through the Anaconda package.

## 1. Semantics


**JPX Tokyo Exchange Prediction** is a project that was created as a semester Project in the context of “Advanced Machine Learning” class.
MSc Data and Web Science, School of Informatics, Aristotle University of Thessaloniki.


## 2. About


The present work consists the official submission of the TsoumTeam to the **JPX Tokyo Stock Exchange Prediction** Competition o Kaggle.

More information available at: https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data

- **Current submition ranking:** 303 (06/06/2022) 
- **Current #teams:** 1466 (06/06/2022) 


## 3. Competition Overview

Success in any financial market requires one to identify solid investments. When a stock or derivative is undervalued, it makes sense to buy. If it's overvalued, perhaps it's time to sell. While these finance decisions were historically made manually by professionals, technology has ushered in new opportunities for retail investors. Data scientists, specifically, may be interested to explore quantitative trading, where decisions are executed programmatically based on predictions from trained models.

There are plenty of existing quantitative trading efforts used to analyze financial markets and formulate investment strategies. To create and execute such a strategy requires both historical and real-time data, which is difficult to obtain especially for retail investors. This competition will provide financial data for the Japanese market, allowing retail investors to analyze the market to the fullest extent.

Japan Exchange Group, Inc. (JPX) is a holding company operating one of the largest stock exchanges in the world, Tokyo Stock Exchange (TSE), and derivatives exchanges Osaka Exchange (OSE) and Tokyo Commodity Exchange (TOCOM). JPX is hosting this competition and is supported by AI technology company AlpacaJapan Co.,Ltd.

This competition will compare your models against real future returns after the training phase is complete. The competition will involve building portfolios from the stocks eligible for predictions (around 2,000 stocks). Specifically, each participant ranks the stocks from highest to lowest expected returns and is evaluated on the difference in returns between the top and bottom 200 stocks. You'll have access to financial data from the Japanese market, such as stock information and historical stock prices to train and test your model.

## 4. About Our Approach


### 4.1 Preprocessing of the Data

### 4.2 Timeseries Analysis
- Visualize the per day closing price of the stock.
- Visualize the data in our series through a probability distribution.

A given time series is thought to consist of three systematic components including level, trend, seasonality, and one non-systematic component called noise.

These components are defined as follows:

- Level: The average value in the series.
- Trend: The increasing or decreasing value in the series.
- Seasonality: The repeating short-term cycle in the series.
- Noise: The random variation in the series.

In order to analyse this components we moved forward with multiplicative decomposition of the stocks.

Further more we checked if a series is stationary via the ADF (Augmented Dickey-Fuller) Test.

The Dickey-Fuller test is one of the most popular statistical tests. It can be used to determine the presence of unit root in the series, and hence help us understand if the series is stationary or not. The null and alternate hypothesis of this test is:

**Null Hypothesis:** The series has a unit root (value of a =1)

**Alternate Hypothesis:** The series has no unit root.

### 4.3 Models


## 5. Performance of the Models


 ### 5.1 Time Performance

| Model	                  | Run time      |
| ----------------------- | ------------- |
| Linear Regression       | `1.1` sec     |
| k - Nearest Neighbor    | `2.0` sec     |
| Support Vector Regressor| `2.0` sec     |
| AdaBoost                | `2.0` sec     |
| Random Forest           | `2.0` sec     |
| XGBoost                 |               |
| LSTM                    |               |
| CNN                     |               |

## 6. Licensing and Refferences



