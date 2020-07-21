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

Results :

![alt text](https://github.com/Pawan300/Stock-market-analysis/blob/master/image1.jpg)


Then 2nd approach

I tried modeling using multiple DMA's [5, 10, 20, 50, 200] and found that 20 DMA is working better than rest of the values.

Results on the above approaches :

* CNN architecture : Max(55 %) directional accuracy
* CNN + LSTM architecture - Max (58%) directional accuracy with an average of -16 negative error and 35 positive error
* LSTM/GRU architecture - Max (56.5%) directional accuracy

The image below is showing the results of CNN + LSTM architecture on test data using 20 DMA.

![alt text](https://github.com/Pawan300/Stock-market-analysis/blob/master/IMAGE1.jpg)
