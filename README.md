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

import numpy as np
import pandas as pd
import seaborn as sns
data=pd.read_csv("/content/titanic_dataset.csv")
data

<img width="1402" height="766" alt="image" src="https://github.com/user-attachments/assets/e28e9afa-33cc-44c9-8b3d-aca8ed3b8036" />

data.info()

<img width="1346" height="488" alt="image" src="https://github.com/user-attachments/assets/b7239978-f507-47b2-8f93-4fbdfe63708b" />

data.describe()

<img width="1264" height="450" alt="image" src="https://github.com/user-attachments/assets/25d7bf1b-a017-47e8-a5bd-fc7840b47680" />

data.dtypes

<img width="480" height="620" alt="image" src="https://github.com/user-attachments/assets/fd8aa045-ddf9-463e-a235-94c7aa7e435a" />

data.shape

<img width="1028" height="95" alt="image" src="https://github.com/user-attachments/assets/a9325027-b10d-4e38-90b1-554326f610bb" />

data['Age'].value_counts()

<img width="600" height="680" alt="image" src="https://github.com/user-attachments/assets/19c00d0a-4af9-43b1-86f2-d44ace700ec8" />

data.set_index('PassengerId',inplace=True)
data

<img width="1552" height="638" alt="image" src="https://github.com/user-attachments/assets/30945aa1-549a-459d-9d73-5aa28ffa64fc" />

data.nunique()

<img width="443" height="651" alt="image" src="https://github.com/user-attachments/assets/b20e7081-c6f8-493b-8e56-38150d9cb0d5" />

sns.countplot(data=data,x='Survived')

<img width="1075" height="629" alt="image" src="https://github.com/user-attachments/assets/b0b2b0b7-fbac-4afd-a962-5531b8beeac1" />

data.rename(columns={'sex':'Gender'},inplace=True)
data

<img width="1543" height="609" alt="image" src="https://github.com/user-attachments/assets/ee1b756c-cb16-4247-a1ae-4059bead2cfc" />

sns.catplot(x="Sex",col="Survived",kind="count",data=data,height=6,aspect=.7)

data.boxplot(column="Age",by="Survived")

<img width="1043" height="687" alt="image" src="https://github.com/user-attachments/assets/d8ee5b9c-d87d-4758-be49-0467649c2b83" />

sns.scatterplot(x=data["Age"],y=data["Fare"])

<img width="1095" height="631" alt="image" src="https://github.com/user-attachments/assets/736f2eb8-2901-4504-a21e-24ff8b60280e" />

plt=sns.boxplot(x='Pclass',y='Age',hue='Sex',data=data)

<img width="939" height="616" alt="image" src="https://github.com/user-attachments/assets/81b8fd66-a069-4df2-aec3-3ea6bbc04645" />

sns.catplot(data=data,col="Survived",x="Sex",hue='Pclass',kind='count')

<img width="1561" height="723" alt="image" src="https://github.com/user-attachments/assets/7149a716-8150-4227-8872-6ee7e232e2fe" />

corr=data.corr(numeric_only=True)
sns.heatmap(corr,annot=True)

<img width="1045" height="729" alt="image" src="https://github.com/user-attachments/assets/2d5c5cb0-0873-4f11-8ab6-8be4eb4f3f0f" />


# RESULT

Thus,the program is excitued successfully.
