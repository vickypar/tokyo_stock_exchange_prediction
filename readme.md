# JPX Tokyo Exchange Prediction

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

[6. Licensing and Refferences](https://github.com/vickypar/tokyo_stock_exchange_prediction#6-licensing-and-refferences)


## 0. Installation 


The code requires Python versions of 3.* and general libraries available through the Anaconda package.

## 1. Semantics


**JPX Tokyo Exchange Prediction** is a project that was created as a semester Project in the context of “Advanced Machine Learning” class.
MSc Data and Web Science, School of Informatics, Aristotle University of Thessaloniki.


## 2. About


The present work consists the official submission of the TsoumTeam to the **JPX Tokyo Stock Exchange Prediction** Competition o Kaggle.

More information available at: https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data

- **Current submition ranking:**
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


### 4.3 Models
- Linear Regression
- k-Nearest Neighbors
- Support Vector Regressor
- Random Forest
- AdaBoost
- XGBoost
- LSTM

### 4.4 Evaluation

**Daily Spread Return**: Overall predicted return at a specific day if the proposed strategy is followed 

$ 𝑅_𝑑_𝑎_𝑦 = 𝑆_𝑡_𝑜_𝑝−𝑆_𝑑_𝑜_𝑤_𝑛 $


**Score**:  The ratio between mean and standard deviation of the time series of daily spread return that is calculated every business day during a specific period

$$
Score = \frac{Average(R_d_a_y_1−_d_a_y_x )}{(STD(R_d_a_y_1−_d_a_y_x)}
$$

**Goal**: Find the largest score

 

## 5. Performance of the Models

Comparison between all approaches.

| Model	                  | MAE           | RMSE          | MSE           | Duration (sec)|
| ----------------------- | ------------- |---------------|---------------|-------------- |
| Linear Regression       | `0.016`       | `0.0260`      | `0.0006`      |**`2.922`**    |
| k - Nearest Neighbor    | `0.020`       | `0.0290`      | `0.0008`      |`1027`         |
| Support Vector Regressor| `0.016`       | `0.0263`      | `0.0006`      |`1277`         |
| AdaBoost                | `0.017`       | `0.0273`      | `0.0007`      |`713.9`        |
| Random Forest           | `0.162`       | `0.2201`      | `0.0484`      |`253.1`        |
| XGBoost                 | `0.018`       | `0.0277`      | `0.0007`      |`928.5`        |
| LSTM                    | **`0.013`**   | **`0.0232`**  | **`0.0003`**  |`31.115`       |

## 6. Licensing and Refferences



