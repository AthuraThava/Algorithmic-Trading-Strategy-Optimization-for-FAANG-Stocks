### Group_5_Project_2
#Algorithmic Trading Strategy Optimization for FAANG Stocks
![FAANG-stocks](https://github.com/AthuraThava/Group_5_Project_2/assets/125109159/11ac0756-0815-4d7f-8565-cc884b0ea0f0)

**Team Members:** <br>
Athura Thavathasan <br>
Brandon Petrie <br>
Harshitha Katta <br>
Nicholas Gracan <br>
Pablo Acevedo <br>

*Presentation June 15th, 2023*

### To access the Prezi presentation use the following link: 
import link/file

## Hypothesis
The project focuses on creating an algorithmic trading system with a specific emphasis on FAANG stocks (Facebook, Apple, Amazon, Netflix, and Google). The primary objective is to conduct thorough backtesting and market analysis using historical data of these stocks. By employing various trading models, the project aims to develop accurate predictions and optimize trading strategies. Technical indicators such as Simple Moving Average (SMA) and logistic regression are utilized to enhance the models' predictive capabilities. Through extensive backtesting and model development, the project seeks to identify buy or sell signals for each FAANG stock, enabling informed trading decisions. The ultimate goal is to create a robust and effective algorithmic trading system that can generate profitable results based on market analysis and strategy optimization.  <br>

## Datasets
To retrieve historical stock data, we utilize the yfinance library. By importing 'import yfinance as yf' library allows us to fetch data directly from Yahoo Finance, providing us with a convenient and reliable source of historical stock prices for analysis and modeling.

## Libraries and Models
# Import Libraries
import pandas as pd ()
import yfinance as yf
import finta
import plotly.graph_objects as go
from pandas.tseries.offsets import DateOffset
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import classification_report
from sklearn import svm
from sklearn.svm import SVC

## Major Findings
data analysis, model training, and evaluation processes
## Conclusion

## PostMortem

### Difficulties/ Limitations


### Furthur Findings: What would you research next if you had two more weeks?:
* There is a lot more opportunity to build on. To implement additional technical indicators or develop custom features that might provide valuable insights for trading strategies. Consider indicators such as Relative Strength Index (RSI), by incorporating these features it could improve the accuracy of the models.
* Sentiment analysis techniques to incorporate real-time market data from news articles, social media, or financial reports. Determine whether sentiment analysis can enhance the prediction accuracy of the trading models and potentially provide early indications of market movements.
* Implement a trading bot in real-time scenarios, connecting it to live market data and executing trades automatically.
##References


