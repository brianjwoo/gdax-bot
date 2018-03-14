# gdax-bot

Plan is to build a functional for trading btc/ethereum using the gdax-api.

Historical btc data is available in batch from http://api.bitcoincharts.com/v1/csv/

#1 Create a API to consume GDAX streaming API and save the data to a postgres database.
#2 Develop a ML model using technical analysis to perform next period price prediction.
  *Use Keras to prototype a Convolutional Bidirectional Recurrnet NN on different aggregations of data to calcualte OHLC. (5/10min(?), 1hr, 1d(30), 1w(26), 1m(24))
  
  Current raw data should exist as:
  (symbol), price, volume, timestamp
  
  
  *Create standard technical analysis features. SMA/EMA/BollingerBands/MACD at different time points for compairison purposes 
  
#3 Deploy ML model to score on streaming API every X minutes and perform automated trading using the stream taking into account current position.
