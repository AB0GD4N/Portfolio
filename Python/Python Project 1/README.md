The purpose of this project is predicting the price of Uber stock to check whether it is going to match
the expected rise in earnings, which is estimated at over 1700% over the next 5 years. 

For project purpose the following hypothesises have been created:
    
    H1: Uber Stock will continue to grow on annual basis
    H2: Uber Stock will surpass the 120$ per share level in the 5 year horizon.
    
The test will be conducted using the autoregressive integrated moving average (ARIMA) with following data:
    
Explained variable (Y) - Uber Stock Price

Explanatory variablex (X):
    -lagged Uber Stock Price
    -S&P 500 Index
    -FED Interest Rate
    
Data Sources:
    
Uber Stock Price : https://finance.yahoo.com/quote/UBER/history
S&P 500 Index : https://stooq.pl/q/d/?s=%5Espx&c=0&d1=20190510&d2=20240308
FED Interest Rate : https://tradingeconomics.com/united-states/interest-rate

Before model application, data should be inspected for autocorrelation, stationarity, cointegration and heteroscedasticity.

For data examination following tests were chosen:

Autocorrelation - Durbin-Watson test
Stationarity - Advanced Dickey-Fuller test
Cointegration - Johannsen test
Heteroscedasticity - Breusch Pagan test
