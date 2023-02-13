# Cristiano Ronaldo ⚽ Goals 📊 EDA, Analysis

![image](https://user-images.githubusercontent.com/63750425/197759801-ac8534c3-2b5e-47d5-8ab8-5e35538da58f.png)

#### In this project, we conducted a career analysis of Cristiano Ronaldo, one of my favorite players. You can develop the project by using different graphs and data sets. Thank you... <br>

Cristiano Ronaldo dos Santos Aveiro, Premier Lig Takımı Manchester United'ta forvet olarak oynayan ve Portekiz milli takımının kaptanlığını yapan Portekizli profesyonel bir futbolcudur.

Current team: Portugal national football team (#7 / Forward) Trending

Born: February 5, 1985 (age 37 years), Hospital Dr. Nélio Mendonça, Funchal, Portugal

Height: 1.87 m Partner: Georgina Rodríguez (2017–) Salary: 26.52 million GBP (2022) Children: Cristiano Ronaldo Jr., Alana Martina dos Santos Aveiro, Eva Maria Dos Santos, Mateo Ronaldo


### import
```Python
import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
import matplotlib.pyplot as plt 
import seaborn as sns
from datetime import timedelta
import warnings
import os
import plotly.graph_objs as go
from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot
import plotly.express as px
```

```Python
df.head()
```

![image](https://user-images.githubusercontent.com/63750425/197760450-70046a01-c624-4008-8c49-61d99ccd9961.png)

```Python
px.histogram(
    df,
    x='Competition',
    title="Goals per competition",
    log_x=False,
    log_y=False,
    #symbol='title',
    #markers=True,
    #width=800, 
    height=500,
    color='Club',
    hover_name='Club',
    hover_data=['Competition','Club'])
 ```
 
 ![image](https://user-images.githubusercontent.com/63750425/197760620-9907e40e-84bd-4663-8adb-641e5312ebeb.png)

```Python
px.histogram(
    df,
    x='Club',
    title="Goals per Clubs - Seasons",
    log_x=False,
    log_y=False,
    #symbol='title',
    #markers=True,
    #width=800, 
    height=500,
    color='Season',
    hover_name='Season',
    hover_data=['Competition','Season','Club'])
 ```
 
 ![image](https://user-images.githubusercontent.com/63750425/197760704-f8a7e2d5-f785-4a8a-966c-035c9cad6f79.png)

```Python
plt.figure(figsize=(30,10))
plt.title('Goals per venue', fontsize=20)
df.Venue.value_counts().plot(kind='pie', labels=['Home', 'Away'], wedgeprops=dict(width=.7), autopct='%1.0f%%', startangle= -20,  textprops={'fontsize': 15})
 ```
 
 ![image](https://user-images.githubusercontent.com/63750425/197760794-7c87b35f-7543-4fb1-a641-e747a7abe875.png)

```Python
temp = df[['Opponent']]
temp['Count'] = 1
temp = temp.groupby('Opponent').sum()
temp.sort_values('Count',inplace=True,ascending=False)
temp_high = temp.head(10)
temp_low = temp.tail(10)

plt.figure(figsize=(20,10))
plt.subplot(1,2,1)
sns.barplot(x=temp_high.Count,y=temp_high.index)
plt.subplot(1,2,2)
sns.barplot(x=temp_low.Count,y=temp_low.index)
plt.show()
 ```
 
 ## Don't forget to like and fork. I wish you healthy days.
 
 ![Başlıksız-1A](https://user-images.githubusercontent.com/63750425/197761042-8654b0e6-92a8-41bd-a38d-55ee5f4b3882.png)
