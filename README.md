
## Deep Learning and Neural Networks Time Series Analysis 

### Overview

This analysis involves in the incorporation of ***Machine Learning*** statistical algorithms that allows us to make predictions based on data patterns. The purpose of this challenge is to focus on ***Neural Networks*** and ***Deep Learning*** in order to perform a ***Time Series Forecasting*** using ***Keras***, an Open Source Neural Network library that runs on top of ***Tensorflow*** which essentially anlyzes patterns in data collected in [Yahoo Finance](https://finance.yahoo.com/) (specifically the ***QQQ*** an ETF which offers broad exposure to the tech sector by tracking the [Nasdaq 100 Index ](https://www.investopedia.com/terms/n/nasdaq100.asp)), in order to make predictions on whether the security is worth adding to our portfolio or not, as well as its over all trend, based on the fundamentals extracted from the data collected. 


## Resources 

### Software & Libraries 

  - Python 
  - Scikit-learn
  - Pandas
  - TensorFlow
  - Keras 
  - Jupyter Notebook
  - Seaborn
  - Matplotlib
  - Plotly 
### Data Source:
  -  [`QQQ_training_df.csv`](QQQ.csv)
  -  [`QQQ_forecasting_df.csv`](QQQ1.csv)


## Results-

### Dataframe 

![Dataframe](https://github.com/schoolboycamel/final_project/blob/Paolo/Resources%20/DF_QQQ.png)

- Dataframe contains 5864 rows and 7 columns
- Dependent Variable chosen: 'CLOSE'

![Technical_indicators](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/DF_technical_indicators%20.png)

- Added 14 technical indicator columns to data frame independent variables:
- Simple Moving Average (SMA)
- Moving Average Convergance/Divergance (MACD)
- Commodity Channel Index (CCI)
- Bollinger Bands (bbands)
  -BBL
  -BBM
  -BBU
  -BBP
  -BBB
- Relative Strength Index (RSI)
- Volume-Weighted Average Price (VWAP)
- On-Balance Volume (OBV)
- Dataframe now contains 5864 rows × 21 columns

![Correlations](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/correlations.png)

- Found correlations of all columns 
- Since 'Close' is our dependent variable, we found its correlations and chose the highest correlations to implement in our model:
  - All SMAs
  - VWAP
  - BBL
  - BBM
  - BBU

![Good correlations](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/Good_correlation.png)

- Visualizations of high correlations that we will use in our model (closer to 1) 

![Bad correlations](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/bad%20correlation.png)

- Visualizations of lowere correlations that would have little impact for out dependent variable. We will desregard these




