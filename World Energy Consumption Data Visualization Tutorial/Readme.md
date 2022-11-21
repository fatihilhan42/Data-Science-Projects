# Energy Consumption - Data Visualization Tutorial 🔌

![image](https://user-images.githubusercontent.com/63750425/201611786-bb49fd6b-af85-4644-99e1-3d3e93331bb2.png)

### In this project, we will visualize world energy consumption data and take a closer look at the energy consumption of several major countries.

### About the dataset ------> https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption
This dataset is a collection of key metrics maintained by Our World in Data. It is updated regularly and includes data on energy consumption (primary energy, per capita, and growth rates), energy mix, electricity mix and other relevant metrics.

Data sources Energy consumption (primary energy, energy mix and energy intensity): this data is sourced from a combination of two sources—the BP Statistical Review of World Energy and SHIFT Data Portal. 
Electricity consumption (electricity consumption, and electricity mix): this data is sourced from a combination of two sources—the BP Statistical Review of World Energy and EMBER – Global Electricity Dashboard. Other variables: this data is collected from a variety of sources (United Nations, World Bank, Gapminder, Maddison Project Database, etc.). More information is available in our codebook.

### Importing Libraries

```Python
import pandas as pd
import numpy as np
from sklearn.preprocessing import StandardScaler
from sklearn.cluster import KMeans, AffinityPropagation
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
import warnings
warnings.filterwarnings("ignore")
import plotly as py
import plotly.graph_objs as go
import os
py.offline.init_notebook_mode(connected = True)
#print(os.listdir("../input"))
import datetime as dt
import missingno as msno
plt.rcParams['figure.dpi'] = 140
```


### GDP Vs Population Trends

![image](https://user-images.githubusercontent.com/63750425/201612790-df16e19c-2e59-48d1-b2de-8cb7868fb7af.png)


### Electricty source distribution in Turkey

![image](https://user-images.githubusercontent.com/63750425/201612900-fdfcce46-3324-40f9-95c7-2091415774c7.png)

# Thank You...

 ![Başlıksız-1A](https://user-images.githubusercontent.com/63750425/197761042-8654b0e6-92a8-41bd-a38d-55ee5f4b3882.png)
