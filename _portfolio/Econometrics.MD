title: "Econometrics IPUMS Project"
excerpt: "Income disparities between Nashville and Tennessee, with a focus on gender-based variations through regression analysis"
header:
  image: assets/img/Image 11-10-23 at 10.46 AM.jpeg
  teaser: assets/img/Image 11-10-23 at 10.36 AM.jpeg
gallery:
  - image_path: assets/img/Image 11-10-23 at 10.36 AM.jpeg
  - image_path: assets/img/Image 11-10-23 at 10.46 AM (1).jpeg
  - image_path: assets/img/Image 11-10-23 at 10.46 AM.jpeg
---

# Python Portfolio

## Public Use Microdata Sample (PUMS) Project

```python
# File: BulgerJack_HW9.py

import pandas as pd # data import
import numpy as np # math operations
import statsmodels.formula.api as smf # regressions
import seaborn as sns #plotting
import matplotlib.pyplot as plt # library for plotting
from scipy import stats
from scipy.stats import f
from scipy.stats import t


### open CSV file
with open('HW9_CensusData.csv') as PUMS:
    Nash_PUMS_df = pd.read_csv(PUMS, na_values= ['nan'])

### Get rid of duplicates
print(Nash_PUMS_df.head())
df_1 = Nash_PUMS_df.drop_duplicates(subset = ['SERIAL'])

### Get rid of 9999999 INCTOT Value
df_2 = df_1[df_1['INCTOT'] != 9999999]
column = df_2['INCTOT']
print(column.max())

### Get rid of 0 INCTOT value
df_3 = df_2[df_2['INCTOT'] != 0]
column1 = df_3['INCTOT']
print(column.min())

### Filter by Nashville, Davidson County -- METAREA was not avaliable to download so I use CITY variable
nashville_df = df_3[df_3['CITY'] == 4410]

### Calculate median income for the greater Nashville area and the entire state of Tennessee
median_income_nashville = nashville_df['INCTOT'].median()
median_income_tennessee = df_3['INCTOT'].median()

### Calculate 1st and 3rd quartiles for the greater Nashville area and the entire state of Tennessee
q1_nashville = nashville_df['INCTOT'].quantile(0.25)
q3_nashville = nashville_df['INCTOT'].quantile(0.75)
q1_tennessee = df_3['INCTOT'].quantile(0.25)
q3_tennessee = df_3['INCTOT'].quantile(0.75)

### Print the results
print("Median income for greater Nashville area:", median_income_nashville)
print("Median income for entire state of Tennessee:", median_income_tennessee)
print("1st quartile income for greater Nashville area:", q1_nashville)
print("3rd quartile income for greater Nashville area:", q3_nashville)
print("1st quartile income for entire state of Tennessee:", q1_tennessee)
print("3rd quartile income for entire state of Tennessee:", q3_tennessee)

### Create new variable - ln(INCTOT)
nashville_df['ln_income'] = np.log(nashville_df['INCTOT'])
df_3['ln_income'] = np.log(df_3['INCTOT'])

### create dummy variables
nashville_df = pd.get_dummies(nashville_df, columns=['RACE'], prefix='RACE', drop_first=True)
df_3 = pd.get_dummies(df_3, columns=['RACE'], prefix='RACE', drop_first=True)

### Create a dummy variable for 'SEX' in both DataFrames
nashville_df['Female'] = (nashville_df['SEX'] == 'Female').astype(int)
df_3['Female'] = (df_3['SEX'] == 'Female').astype(int)

### Drop the original 'SEX' column since we've created a dummy variable
nashville_df = nashville_df.drop(columns=['SEX'])
df_3 = df_3.drop(columns=['SEX'])

### Simple Regression
df_3['Intercept'] = 1

### Create the regression model using the formula API
reg = smf.ols('ln_income ~ Female', data=df_3, missing='drop').fit()
print(reg.summary())
nashville_df['Intercept'] = 1

### Create the regression model using the formula API
reg2 = smf.ols('ln_income ~ Female', data=nashville_df, missing='drop').fit()
print(reg2.summary())

### Multivariable Regression
nashville_df['Intercept'] = 1
reg_nashville = smf.ols('ln_income ~ Female + EDUC + IND + RACE_2 + AGE', data=nashville_df)
result_nashville = reg_nashville.fit()
print(result_nashville.summary())
df_3['Intercept'] = 1
reg_tn = smf.ols('ln_income ~ Female + EDUC + IND + RACE_2 + AGE', data=df_3)
result_tn = reg_nashville.fit()
print(result_tn.summary())

### Heat Map
### Tennessee
regression_variables = df_3[['ln_income', 'Female', 'EDUC', 'IND', 'RACE_2', 'AGE']]
correlation_matrix = regression_variables.corr()

### Create a heatmap
plt.figure(figsize=(10, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt='.2f')
plt.title('Correlation Heatmap of Regression Variables (Tennessee)')
plt.show()

### Nashville
regression_variables = nashville_df[['ln_income', 'Female', 'EDUC', 'IND', 'RACE_2', 'AGE']]
correlation_matrix = regression_variables.corr()

### Create a heatmap
plt.figure(figsize=(10, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt='.2f')
plt.title('Correlation Heatmap of Regression Variables (Nashville)')
plt.show()

{% include gallery caption= "Regression Analysis and Heat Map of Variables" %}
