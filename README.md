# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df
```
<img width="1227" height="418" alt="image" src="https://github.com/user-attachments/assets/66d5abac-5b8c-4768-860e-fc6bc721100a" />

```
df.info()
```

<img width="492" height="412" alt="image" src="https://github.com/user-attachments/assets/f14c54b7-e45d-4331-ba03-fc29de539760" />

```
df.describe
```
<img width="641" height="677" alt="image" src="https://github.com/user-attachments/assets/3dffd782-26d8-4cc5-b35e-bb268189fb87" />

```
df.dtypes
```

<img width="212" height="223" alt="image" src="https://github.com/user-attachments/assets/b5d4f819-8908-42f3-8468-957e8ec02caa" />

```
df.shape
```

<img width="993" height="26" alt="image" src="https://github.com/user-attachments/assets/2fac7418-5c9b-4d1b-b3f4-b5e0e6bd27eb" />


```
df['Age'].value_counts()
```

<img width="317" height="210" alt="Screenshot 2025-09-15 114357" src="https://github.com/user-attachments/assets/5d115f15-4d1f-44c3-9e5e-9a045d782ad5" />


```
df.set_index("PassengerId",inplace=True)
df
```

<img width="968" height="375" alt="image" src="https://github.com/user-attachments/assets/f6afc91c-7f97-4efc-9ba3-ae15157c3637" />

```
df.nunique()
```

<img width="205" height="210" alt="image" src="https://github.com/user-attachments/assets/adec7dd9-f15d-4fac-baf8-3ddf011e5a61" />

```
sns.countplot(data=df,x='Age')
```

<img width="715" height="461" alt="image" src="https://github.com/user-attachments/assets/0c3ad714-64d7-4214-8b0d-0eef78894457" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```


# RESULT
        <<INCLUDE YOUR RESULT HERE>>
