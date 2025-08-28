# Coca-Cola-Live-Stocks-Prediction-and-Strategy-Comparison
This project involves analyzing Coca-Cola's historical stock data to build a machine learning model that predicts stock closing prices. It further compares a traditional **Buy &amp; Hold strategy** with a **Machine Learning (ML)-based trading strategy** based on predicted price movements.

**Dataset Description**



Two datasets were used:

\- `Coca-Cola\\\_stock\\\_history.csv`: Contains historical stock price data (Open, High, Low, Close, Volume, Dividends, Stock Splits).

\- `Coca-Cola\\\_stock\\\_info.csv`: Additional company details (not directly used in the model).





**Exploratory Data Analysis (EDA)**



EDA included:

\- Descriptive statistics of prices and volume.

\- Visualizations of closing prices and moving averages.

\- Daily return and rolling volatility calculations.





**Feature Engineering**



Engineered features:

\- 20-day \& 50-day Moving Averages

\- Daily Returns

\- 20-day Rolling Volatility





**Model Training**



\- Model: `RandomForestRegressor` from Scikit-learn.

\- Features used: Open, High, Low, Volume, Dividends, Stock Splits, MA\_20, MA\_50, Daily\_Return, Volatility.

\- Target: Close price.

\- Data was split into train/test without shuffling (time series constraint).



**Evaluation Metrics:**

\- MSE (Mean Squared Error)

\- MAE (Mean Absolute Error)





**Strategy Logic**



**Buy \& Hold Strategy**

\- Invest once at the start and hold throughout.



**ML Strategy**



\- Buy if the model predicts the next day's closing price will be higher than today’s actual price.

\- Otherwise, hold cash (do not invest).



---



**Final Results**



| Strategy       | Final Value (USD) |

|----------------|-------------------|

| Buy \& Hold     | $13,726,542.31    |

| ML Strategy    | $804,038.22       |

| Difference | - $12,922,504.09 |



**Insight**: The ML strategy underperformed due to overtrading or noisy predictions — a valuable real-world lesson.


**Video Presentation Link:**
https://drive.google.com/drive/folders/10XpucRINVhnntocZOnewfur4M9_7oAie?usp=sharing




**Conclusion**





In this project, we developed a machine learning pipeline to predict Coca-Cola’s stock closing prices and compared a model-driven investment strategy with a traditional buy-and-hold approach. Using Random Forest Regressor and historical stock data, we generated predictive signals to simulate buy/sell decisions over time. While the model showed the ability to capture market patterns, the final portfolio value under the ML strategy significantly underperformed the buy-and-hold strategy. This highlights a crucial insight: \*\*predicting stock prices is not the same as achieving better financial returns.\*\* Overfitting, noise, transaction costs, and model lag can heavily impact real-world profitability, even if predictions appear statistically accurate.



Overall, this project demonstrates how data science can be applied to financial analysis and investment strategy design, providing valuable hands-on experience in real-world predictive modeling and time series data handling.
