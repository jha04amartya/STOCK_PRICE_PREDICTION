# STOCK_PRICE_PREDICTION
The aim of our project is to study the stocks of 4 to 5 different companies from 1981 to 2020 i.e. 40 years and try to forecast the data for a whole year i.e. 2021.
# DATA:-
We use the yfinance library in python to get the data , the data had different features like open price , low price , high price , closed price , adjusted closed price for a day . We only focused on the closed price of the stocks for a day and the volume of stocks traded .
# MODELS and RESULTS:-
We used different models and techniques to get better results.
# liner regression:-
first we tried linear regression, in which we used a sample space of 100 data points to predict the next day prediction 
LSTM:-
In this we used a test train split of 80-20 (the first 80% of 40 years data being train data) and achieved a r2 score of .982 on APPLE , .97 ON GOLDMAN SACHS , .963 on COCA COLA , .9784 on IBM test dataset
# TRANSFORMERS + TIME EMBEDDINGS:-
Transformers combined with natural language data tend to utilize positional encoding to provide the model with word order. In detail, the positional encoding represents a word’s value and position in a sentence, allowing the Transformer to obtain knowledge about a sentence structure and word inter-dependencies, so for the information of time to go through the network, we will use TIME2VEC. The Time2Vec architecture is based on the popular Word2Vec model, which is used for learning vector representations of words in natural language processing. Time2Vec learns vector representations of time by treating time as a sequence of categorical values, which are then converted to continuous vector representations using an embedding layer.
# TEMPORAL FUSION TRANSFORMER:-
Temporal Fusion Transformer (TFT) is a deep learning architecture developed by Google AI that is designed for forecasting tasks, particularly in domains with multiple interacting time-series. TFT consists of three main components: a temporal encoding layer, a multi-headed self-attention layer, and a decoder layer. The temporal encoding layer is responsible for encoding the time information of the input data, while the multi-headed self-attention layer attends to the interactions between the different time-series. The decoder layer generates the final forecast. We trained the model to forecast the values of stock closing price for 154 days based on the given context data of 308 days.
# PROPHET - Facebook’s Time Series Forecasting model:-
Prophet is a time-series forecasting model developed by Facebook.The Prophet model uses a decomposable time-series model with three main components: trend, seasonality, and holidays. The trend component models non-periodic changes in the time series while the seasonality component models periodic changes (e.g. daily, weekly, yearly). The holidays component allows for modeling the effects of known events such as public holidays.
We utilized the Prophet time-series forecasting model to predict stock prices for a given company. The model was trained using stock price data spanning from 1981 to 2020 and was used to forecast stock prices for the entirety of 2021. The results of the forecast indicated that the stock price would experience a gradual increase throughout the year with a few minor fluctuations.

All the results of different models and their graphs and r2 scores are present in the report (doc file) .
