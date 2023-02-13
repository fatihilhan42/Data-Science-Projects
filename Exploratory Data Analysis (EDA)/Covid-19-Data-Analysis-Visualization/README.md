# Covid-19-Data-Analysis-Visualization

The first project of our data visualization studies is the COVID-19 data analysis project. In this project, we analyzed the data of the COVID-19 pandemic, which started in the first month of 2020 and still continues to affect the world, on the basis of countries. You can find the brief details of the project we realized in 3 stages in the readme file. We have tried to explain the details of the project step by step below. We wish you healthy days.

## Covid-19-Data-Analysis-Visualization 1

First, we will download the libraries we will use.

`!pip install folium -- !pip install plotly`

### import
```Python
import plotly.express as px
import plotly.graph_objects as go
import plotly.figure_factory as ff
from plotly.subplots import make_subplots

import folium

import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt

%matplotlib inline

import math 
import random
from datetime import timedelta

import warnings 
warnings.filterwarnings('ignore')
```


### After importing our libraries, we defined our dataset.
```!git clone https://github.com/laxmimerit/Covid-19-Preprocessed-Dataset```

### Total number of covid-19 cases in the world


![Total number of covid-19 cases in the world](https://user-images.githubusercontent.com/63750425/151665566-712196f4-5789-4e33-aee6-fa56c3b6dc1b.png)


### Total number of covid-19 deaths in the world
![Total number of covid-19 deaths in the world](https://user-images.githubusercontent.com/63750425/151666393-21eb486f-2c87-45a4-b791-f22624d45306.png)

## Covid-19 Data Analysis Visualization 2

### Confirmed Cases with Choropleth Map

![Confirmed Cases with Choropleth Map](https://user-images.githubusercontent.com/63750425/151666566-34003976-59f4-40f6-9166-794e557e6c89.png)

### Confirmed and Detah Cases with Static Colormap

![Confirmed and Detah Cases with Static Colormap](https://user-images.githubusercontent.com/63750425/151666603-80d5d570-22dc-492d-8418-f16fc64225ad.png)

## Covid-19 Data Analysis Visualization 3

### Line Plot

![Line Plot](https://user-images.githubusercontent.com/63750425/151666876-ca2adeea-5b08-47ed-b90a-483c0663640a.png)

### Growth Rate after 100k Cases

![Growth Rate after 100k Cases](https://user-images.githubusercontent.com/63750425/151666973-1ff87547-9456-4277-90a2-dd292c6ac487.png)


### Tree Map Analysis

### Deaths Cases

![Deaths Cases](https://user-images.githubusercontent.com/63750425/151667008-8f8422a2-d42a-4042-b77e-494dee9e7060.png)

### Covid-19 vs Other Similar Epidemics

![Covid-19 vs Other Similar Epidemics](https://user-images.githubusercontent.com/63750425/151667063-d9afacc8-14cf-4952-a78e-24960db158bc.png)


We tried to show some important and striking graphics in our project above. You can find all the files of our first project in our data science journey in the github repo.
