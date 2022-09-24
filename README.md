                                   workshop -2 Bivariate/Multivariate Analysis
                                   
                                   
  Aim:
  
     To Perform Bivariate/Multivariate Analysis
     
 Algorithm
      
    1. Read the given data 
    2.Get information from the data 
    3.Perform the Bivariate/Multivariate Analysis
    4. Save the clean data to File
    
program:

Types of Bivariate Analysis: 

(i) Numerical & Numerical 

Scatter plot

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

sns.scatterplot (df['Price'],df['Arrival_Time'])

![image](https://user-images.githubusercontent.com/113016781/192111763-96a29e60-ed64-4035-baf3-fd3ee08e5685.png)

ii) Numerical & Categorical

Bar Plot

import pandas as pd

import seaborn as sns

sns.barplot (x=df['Duration'],y=df['Price'])

![image](https://user-images.githubusercontent.com/113016781/192111820-01dc7fd3-aeef-46f8-b8b4-a7f010ffc164.png)

states=df.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

import matplotlib.pyplot as plt

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()

![image](https://user-images.githubusercontent.com/113016781/192111978-cd66faba-1000-4f3e-b730-7dec5b685f41.png)

Multivariate Analysis

df.corr()

![image](https://user-images.githubusercontent.com/113016781/192112024-5b1acb6f-1325-4499-b7b0-cd01335d32ad.png)


import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/flght.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()

![image](https://user-images.githubusercontent.com/113016781/192112036-ed8bba59-834c-4032-a444-ce8593b4fb69.png)


Result : 
    Thus we applied Bivariate/Multivariate Analysis Successfully







