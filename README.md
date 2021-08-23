# ruthsrepo 

## My first github repository

#1
A = [1,2,3,4,5,6]
B = [13, 21, 34]
c = A.extend(B)
print(c)

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

url = 'https://raw.githubusercontent.com/WalePhenomenon/climate_change/master/fuel_ferc1.csv'
fueldt = pd.read_csv('https://raw.githubusercontent.com/WalePhenomenon/climate_change/master/fuel_ferc1.csv')

dtdf = pd.DataFrame(data=fueldt)
#2

print(np.identity(3))


#3

print(dtdf['fuel_cost_per_unit_burned'].min())

dtdf['fuel_cost_per_unit_burned'].idxmin()

dtdf.iloc[7733,:]

#4

dtdf['fuel_mmbtu_per_unit'].std()
dtdf['fuel_mmbtu_per_unit'].quantile(0.75)

#5

dtdf['fuel_qty_burned'].skew()
dtdf['fuel_qty_burned'].kurtosis()

#6
dtdf.isnull().sum()
dtdf.isnull().sum()

#10

print(dtdf['fuel_cost_per_unit_delivered'].max())

dtdf['fuel_cost_per_unit_delivered'].idxmax()

dtdf.iloc[3564,:]

#8
sns.boxplot(x='fuel_cost_per_unit_burned',y='utility_id_ferc1',palette=['m','g'], data=fueldt)
