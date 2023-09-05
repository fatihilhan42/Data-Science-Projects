# Stock-Market-Analysis-with-Pandas-Python
Hello, today I will tell you the details of the stock market analysis project with python.

## Stock Market Analysis with Pandas Python

First, let's start our project by importing the libraries. 

### import
```Python
1.	import pandas_datareader.data as web 
2.	import datetime
3.	import matplotlib.pyplot as plt
4.	import numpy as np
5.	%matplotlib inline
```


After defining our libraries, we determine our start and end dates for our stock market analysis. 
```Python
1.	start = datetime.datetime(2021,1,1)
2.	end = datetime.datetime(2022,2,25)
```
### What is Pandas Datareader in Python?
Pandas Datareader is a Python package that allows us to create a pandas DataFrame by using some popular data sources available on the internet including: 
1.	Yahoo Finance 
2.  Google Finance
3.	Morningstar
4.	IEX
5.	Robinhood
6.	Engima
7.	Quandl
8.	FRED
9.	World Bank
10.	OECD and many more.

Yes, we learned what datareader is, now let's use datareader to pull google stock market data from yahoo source.

```Python 
google = web.DataReader("GOOGL", "yahoo", start, end)
```
```Python 
1.google.head()
```
![Ekran görüntüsü 2022-02-27 120838](https://user-images.githubusercontent.com/63750425/155878863-6bb6dfab-5d67-4e74-bfde-7ae57b740942.png)

```Python 
google.tail()
```
![Ekran görüntüsü 2022-02-27 121409](https://user-images.githubusercontent.com/63750425/155878914-457b6803-29f4-48c1-ba64-6ccfef2a448d.png)

Yes, we have extracted the change table of the google stock market data within the first and last 5 days in the date ranges we defined above.

```Python 
1.	google['Open'].plot(label = 'GOOGL Open price', figsize= (16,8))
2.	google['Close'].plot(label = 'GOOGL Close price')
3.	google['High'].plot(label = 'GOOGL High price')
4.	google['Low'].plot(label = 'GOOGL Low price')
5.	plt.legend()
6.	plt.title('Google Stock Prices')
7.	plt.ylabel('Stock Price')
8.	plt.show()
```

Thanks to the code blocks above, we showed Google's data such as opening, closing, volume in certain time intervals in the stock market on the plot chart.

Now three big automobile and engine companies; Let's examine the stock market data of TESLA, FORD AND GENERAL MOTORS.

```Python 
1.	tesla = web.DataReader("TSLA",'yahoo', start, end)
2.	ford  = web.DataReader("F", 'yahoo', start, end)
3.	gm = web.DataReader("GM", 'yahoo', start,end)
```
Just like we got Google data, we got the data of three companies from yahoo using pandas datareader. 

```Python 
1.	tesla.to_csv('Tesla_Stock.csv')
2.	ford.to_csv('Ford_Stock.csv')
3.	gm.to_csv('GM_Stock.csv')
```
We will use the following lines of code to convert the captured data into a csv file.

```Python 
tesla.head()
```

![Ekran görüntüsü 2022-02-27 122157](https://user-images.githubusercontent.com/63750425/155879056-2e2e0569-c898-4162-aa3a-5a86824c60cc.png)

```Python 
1.	tesla['Open'].plot(label = 'Tesla', figsize= (16,8))
2.	gm['Open'].plot(label = 'GM')
3.	ford['Open'].plot(label = 'Ford')
4.	plt.legend()
5.	plt.title('Stock Prices of Tesla, GM, Ford')
6.	plt.ylabel('Stock Price')
7.	plt.show()
```
Thanks to the code blocks we wrote above, you can see our chart below, which compares the opening data of three companies.


![Ekran görüntüsü 2022-02-27 122516](https://user-images.githubusercontent.com/63750425/155879097-f8ac8312-cc4d-41bc-8a61-87a04160da14.png)

```Python 
1.	tesla['Total Traded']= tesla['Open'] * tesla['Volume']
2.	gm['Total Traded']= gm['Open'] * gm['Volume']
3.	ford['Total Traded']= ford['Open'] * ford['Volume']
```

```Python
1.	tesla['Total Traded'].plot(label = 'Tesla', figsize= (16,8))
2.	gm['Total Traded'].plot(label = 'GM')
3.	ford['Total Traded'].plot(label = 'Ford')
4.	plt.legend()
5.	plt.ylabel('Total Traded')
```
![Ekran görüntüsü 2022-02-27 122957](https://user-images.githubusercontent.com/63750425/155879133-b52ac66b-5bd9-4de3-b18e-7c9067700fb0.png)
Thanks to the lines of code we wrote above, we compared the total trade data of 3 companies.

### Moving average

In statistics, a moving average (rolling average or running average) is a calculation to analyze data points by creating a series of averages of different subsets of the full data set. It is also called a moving mean (MM)[1] or rolling mean and is a type of finite impulse response filter. Variations include: simple, cumulative, or weighted forms.
Given a series of numbers and a fixed subset size, the first element of the moving average is obtained by taking the average of the initial fixed subset of the number series. Then the subset is modified by "shifting forward"; that is, excluding the first number of the series and including the next value in the subset.

```Python
1.	tesla['Open'].plot(label = 'No Moving Average', figsize= (16,8))
2.	tesla['MA50']=tesla['Open'].rolling(50).mean()
3.	tesla['MA50'].plot(label='MA50')
4.	tesla['MA200']= tesla['Open'].rolling(200).mean()
5.	tesla['MA200'].plot(label='MA200')
6.	plt.legend()
```


![Ekran görüntüsü 2022-02-27 123436](https://user-images.githubusercontent.com/63750425/155879178-9fda2153-e43c-4f27-a255-2624956556ea.png)

In the chart we have seen above, we have drawn the moving average chart of the tesla company.

### What is a Scatter Matrix?

A scatter matrix (pairs plot) compactly plots all the numeric variables we have in a dataset against each other one. In Python, this data visualization technique can be carried out with many libraries but if we are using Pandas to load the data, we can use the base scatter_matrix method to visualize the dataset.
Now let's create a scatter matrix together and display our data on the scatter map.
```Python
1.	from pandas.plotting import scatter_matrix
2.	import pandas as pd
```
```Python
1.	car_comp = pd.concat([tesla['Open'],gm['Open'],ford['Open']],axis = 1)
2.	car_comp.columns = ['Tesla Open', 'GM Open', 'Ford Open']
```
```Python
scatter_matrix(car_comp,figsize = (12,12))
```
![Ekran görüntüsü 2022-02-27 123940](https://user-images.githubusercontent.com/63750425/155879214-f343bd56-4e73-4fc5-8f78-195559879acd.png)

Yes, in this project I tried to show you how to make a simple stock market data analysis application over python. 

I wish you a healthy day.
