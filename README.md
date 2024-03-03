# EX.NO: 01 PLOT A TIME SERIES DATA...

###  DATE : 

## AIM :

To Develop a python program to Plot a time series data (population/ market price of a commodity/temperature) .

## ALGORITHM :

1. Import the required packages like pandas and matplot.
   
2. Read the dataset using the pandas.
 
3. Calculate the mean for the respective column.
   
4. Plot the data according to need and can be altered monthly, or yearly.
   
5. Display the graph.

## PROGRAM :

### Population Time Series Data :

```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2017-01"]
df["2017"].mean()
df["2017-05":"2017-06"]
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```

### Market Price of a Commodity Time Series Data :

```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("gold_price_data.csv",parse_dates=["Date"],index_col="Date")
df.head()
df["2017-01"]
df["2017-01"].mean()
df["2017-05-01":"2017-08-31"]
df.resample('M').mean()
df.plot(kind='line')
plt.xlabel("Date")
plt.ylabel("Value")
plt.show()
mean=df.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("VAlue")
plt.show()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Value")
plt.show()

```

### Temperature Time Series Data :

```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("/content/DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
df["2017-01"]
df["2017"].mean()
df["2017-05-01":"2015-08-31"]
df['meantemp'].resample('M').mean()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
mean=df["meantemp"].resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Temperature")
plt.show()

```

## OUTPUT :

### Population Time Series Data :

![image](https://github.com/Pavan-Gv/TSA_EXP1/assets/94827772/437a1edc-f19e-4be4-8a1b-046451e19acd)

### Market Price of a Commodity Time Series Data :

![image](https://github.com/Pavan-Gv/TSA_EXP1/assets/94827772/119e0938-8bae-4ea2-8169-39f59e520fd7)

![image](https://github.com/Pavan-Gv/TSA_EXP1/assets/94827772/5f227f16-d1ce-402c-8a19-25e12cce6cd9)

![image](https://github.com/Pavan-Gv/TSA_EXP1/assets/94827772/edf144ee-2eba-4330-9c47-88c59fccbd99)

### Temperature Time Series Data :

![image](https://github.com/Pavan-Gv/TSA_EXP1/assets/94827772/5d810fb8-2d8f-4e0e-a6f8-6cf942027bae)

![image](https://github.com/Pavan-Gv/TSA_EXP1/assets/94827772/9c571964-7b8b-450c-b5ab-be78a71a0b57)

## RESULT :

Thus, we have created the python code for plotting the time series of given data.
