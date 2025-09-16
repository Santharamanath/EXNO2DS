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

<img width="962" height="381" alt="image" src="https://github.com/user-attachments/assets/0e0ee461-50c0-4a0a-a650-9529f16b4a2f" />

```
sns.catplot(x="Gender",col="Age",kind="count",data=df,height=5,aspect=.7)
```

<img width="983" height="62" alt="image" src="https://github.com/user-attachments/assets/e0970852-493a-48cb-92f4-9df66649b04d" />

```
df.boxplot(column="Age",by="Survived")
```

<img width="701" height="497" alt="image" src="https://github.com/user-attachments/assets/0c47402d-4cc2-4ff1-ba87-fd8283e1c1ba" />

```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```

<img width="671" height="462" alt="image" src="https://github.com/user-attachments/assets/83d00ba6-842d-4b08-bb4b-0017490ab391" />

```
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```

<img width="590" height="426" alt="image" src="https://github.com/user-attachments/assets/4f59b55c-88f2-4ba6-b862-27fd28cd2963" />


```
sns.catplot(x='Pclass',y="Age",hue="Gender",col="Survived",kind="box",data=df)
```

<img width="990" height="482" alt="image" src="https://github.com/user-attachments/assets/e74918b5-0890-400c-a01d-dda71ab8f4a3" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
```

<img width="601" height="442" alt="image" src="https://github.com/user-attachments/assets/fbd31324-7999-4088-9ea0-08dfd335f6f2" />


# RESULT
        Thus,this is To perform Exploratory Data Analysis on the given data set.
