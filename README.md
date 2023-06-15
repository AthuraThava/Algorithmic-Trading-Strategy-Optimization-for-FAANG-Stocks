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
To retrieve historical stock data, we utilize the yfinance library. By importing `import yfinace as yf` library and providing the needed ticker symbols `META``AAPL``AMZN``NFLX``GOOGL` it allowed us to fetch data directly from Yahoo Finance, providing us with a historic stock prices for analysis and modeling. 

## Libraries and Models
# Import Libraries
import pandas as pd (Used for data manipulation and analysis)
import yfinance as yf ( to fetch historical stock price data of FAANG stocks)
import finta (Used for technical analysis for indicators such as SMA, EMA and Boolinger Bands)
import plotly.graph_objects as go ()
from pandas.tseries.offsets import DateOffset
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import classification_report
from sklearn import svm
from sklearn.svm import SVC

## Data Analysis
Retrieved historical data for FAANG stocks using the `yf.download` function from the `yfinance` library. The data is retrieved for the time period from `start_date` July 1, 2021, to `end_date` June 1, 2023, at an hourly interval.

Computed various technical analysis indicators such as Simple Moving Averages (SMA) and Exponential Moving Average (EMA) for each stock. 

Using the `go.Candlestick` class from the `plotly.graph_objects` library visualized the stock price and creates a candlestick chart. The chart helps visualize the stock's price movements and the trend indicated by the moving averages.

Dropping unnecessary columns from the DataFrame and preparing the data for training and testing the machine learning model.

Initializes a new column called 'signal' in the DataFrame and assigns signals (-1 for sell and 1 for buy) based on the comparison between SMA, EMA, and the stock price. The code generates trading signals based on the relationship between the SMAs and EMA. If both the SMA_9 and SMA_21 are below the EMA_200, a sell signal (-1) is assigned. If both SMAs are above the EMA_200, a buy signal (1) is assigned. The generated signals are stored in the `signal` column of the DataFrame

# Model Training
Splitting the data into training and testing sets, with the training set covering a 3-month period from the start of the data. The code prepares the data for model training and testing. The signal column is copied to a new Series called 'y', and the SMA_9, SMA_21, and EMA_200 columns are selected and copied to a new DataFrame called 'X'. The data is split into training and testing sets based on the specified time periods.

Applied feature scaling to the training and testing data using the `StandardScaler` from `sklearn.preprocessing` to normalize the input features. The code applies the StandardScaler to scale the features (SMA_9, SMA_21, EMA_200) in the training and testing data. The code creates an SVM model (SVC()) and fits it to the scaled training data. 

Created an SVM classifier (`SVC` class from `sklearn.svm`) and fit it to the training data.

The trained SVM model will predict the trading signals for both the training and testing data. The predictions are stored in `training_signal_predictions` and `testing_signal_predictions`

# Evaluation

Evaluated the model's performance by generating a classification report for both the training and testing data, which provides metrics such as precision, recall, F1-score, and accuracy. The classification report evaluates the model's performance in predicting the trading signals.

Created a new DataFrame `predictions_df` for predictions, which includes the predicted signals, actual returns, and algorithmic trading returns.

Plotted the cumulative returns for the actual returns and the trading algorithm returns.

## Conclusion

## PostMortem

### Difficulties/ Limitations


### Furthur Findings: What would you research next if you had two more weeks?:
* There is a lot more opportunity to build on. To implement additional technical indicators or develop custom features that might provide valuable insights for trading strategies. Consider indicators such as Relative Strength Index (RSI), by incorporating these features it could improve the accuracy of the models.
* Sentiment analysis techniques to incorporate real-time market data from news articles, social media, or financial reports. Determine whether sentiment analysis can enhance the prediction accuracy of the trading models and potentially provide early indications of market movements.
* Implement a trading bot in real-time scenarios, connecting it to live market data and executing trades automatically.
##References


