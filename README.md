
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
  -  Long-Strong-Term Memory (LSTM)
### Data Source:
  -  [`QQQ_training_df.csv`](QQQ.csv) Will use to train our model
  -  [`QQQ_forecasting_df.csv`](QQQ1.csv) Will use to forecast our model. 


## Results-

### Dataframe 
Read csv up until the 27th of june

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

- Visualizations of lowere correlations that would have little impact for out dependent variable. We will desregard these.

![data preprocessing](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/Data_preprocess%20.png)
![Data Preprocessing](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/Data_preprocess2.png)

- Peprocess data. 
  - Reshape data
  - Scale data 
  - Stack data
  - Split data into X and Y 

![Define model](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/defone%20model.png)
- We will define the learning rate, split the data into training and testin, and finally we will fit the model 

![Visualization_model](https://github.com/schoolboycamel/QQQ_Times_Series_Analysis/blob/Paolo/Resources%20/training_testing_model_vis.png)

-Testing model visualization, where the blue line represents the training data, and the organge line represents the testing data. Our goal here is for our model to learn its patterns, we can see that the testing data comes down to meet the training data, this means the model is learning the patterns.


# Read CSV to use trained model to forecast new data (up until July 18th)

<img width="425" alt="image" src="https://user-images.githubusercontent.com/98793962/180325672-ecd80485-d568-4ba6-a8b8-f1b1de224f2e.png">

- We will read a csv that contains data up until july 18th 2022.
- Same data preprocessing will be applied, however, we will not rain the model, we will just use the data for forcasts. 
- The model, which is already trained, will be used with this data in order to forecast the next 20 days after july 18th. 
- We will repeat the same preprocessing steps done with the training data set.

<img width="581" alt="image" src="https://user-images.githubusercontent.com/98793962/180327601-6ffe82fa-6a34-4c1f-a5bd-50150a6b5a63.png">

- We will now predict our model and inverse the result.

<img width="552" alt="image" src="https://user-images.githubusercontent.com/98793962/180327889-81438627-999e-44bb-ab08-03238bb4d57c.png">

- Created a new dataframe with the forecasted data and visualizaed it





