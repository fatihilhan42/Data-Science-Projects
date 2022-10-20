## Import

```Python
import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)

# import necessary libraries.

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats
import seaborn as sns
```

### 1) Train Dataset

![image](https://user-images.githubusercontent.com/63750425/196395034-aef7603f-618d-438f-aa10-4c32eda082ac.png)

```Python
sns.heatmap(data=corMat)
plt.show()
```

![image](https://user-images.githubusercontent.com/63750425/196395205-ff3c454d-d333-411e-920e-3539c9f13e30.png)


### 2) Test Dataset

```Python
test.head()
```

![image](https://user-images.githubusercontent.com/63750425/196395360-2e49925c-fdef-4628-a55f-0922bb849d2f.png)


### Visual Exploration
```Python
train_store.boxplot(column='Sales', by='Year')
plt.show()
```

![image](https://user-images.githubusercontent.com/63750425/196395721-e3a50da5-21f2-4484-87b1-8bdedfe7e4e3.png)


### Sales by Month

```Python
train_store.boxplot(column='Sales', by='Month')
plt.show()
```

![image](https://user-images.githubusercontent.com/63750425/196395858-54dabf65-cbc1-4aba-89a1-ace1886c500a.png)


![image](https://user-images.githubusercontent.com/63750425/196395925-4adcd21a-cea0-4ea2-8e91-dc41b8fa1d1b.png)

![image](https://user-images.githubusercontent.com/63750425/196395991-133cde19-a408-4f65-bf99-f9c802fcdace.png)

![image](https://user-images.githubusercontent.com/63750425/196396031-5d7f5c9e-a3c1-464a-854c-076a936067f6.png)

