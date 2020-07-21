# Stock-market-analysis

Recently I was trying to chase stock market data of xyz company,
It has variables [Open, Close, High, Low, Volume] :

and tried approaches are:
- Using technical indicators such as moving average, exponential moving average, rate of Change of closing price, momentum etc.
- Using feature engineering
- Using deep learning models
  * CNN architecture - Max (55%) accuracy
  * CNN + LSTM architecture - Max (58.13%) accuracy
  * LSTM/GRU architecture - Max (55%) accuracy
  * and other machine learning approaches
  
Metrics are directional accuracy and error between y_true and y_predicted.
Directional accuracy (percentage of data follow the condition) = 

condition : np.sign(y_actual[i] - y_actual[i-1]) == np.sign(y_pred[i] - y_actual[i-1])

Error rate :
error = (y_pred[i]-y_actual[i])/abs((y_actual[i-1]-y_actual[i]))

(+)ve and (-)ve error rates are the main metrics
