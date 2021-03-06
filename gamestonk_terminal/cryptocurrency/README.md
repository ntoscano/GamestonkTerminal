# Cryptocurrency

This page gives an overview of the ability to load cryptocurrency data.

Current crypto  data is [Powered by CoinGecko API](#https://www.coingecko.com/en).  
This is an awesome service that currently requires no API Key!

Current functionality is aimed to be similar to loading a stock ticker.

* [load](#load)
* [view](#view)

## load  <a name="load"></a>
Load a given coin vs a given currency:

````
usage: load [-c --coin] [-d --days] [--vs]
````
* -c/--coin The coin you wish to load.  This can either be the symbol or the name.  `load -c btc` and `load -c bitcoin` 
  will load.  The -c flag is optional,  the above is equivalent to `load btc`.
  
* -d/--days The number of days to look.  Defaults to 30 days.  As per the API: Minutely data will be used for duration within 1 day, 
  Hourly data will be used for duration between 1 day and 90 days, Daily data will be used for duration above 90 days.

* --vs The currency to look against.  Defaults to "usd".

Currently only retrieves price, not volume or MarketCap.

Example doge/eur for the past day:
````
load -c doge -d 1 --vs eur
````

## view  <a name="view"></a>
Plot the loaded crypto data.
````
usage: view
````
After loading the above 1 day dogecoin/eur.  Running view plots the data:

![doge](https://user-images.githubusercontent.com/18151143/112690617-7832f500-8e52-11eb-84c4-253ab222a918.png)
