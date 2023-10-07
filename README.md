# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
```
Name:MOHAMMED IMTHIYAS
Reg no:212222230083
```
```
import pandas as pd
df=pd.read_csv("SAMPLEDS - Sheet1 (2).csv")
df.shape
```

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/cbe5e940-c557-4cbf-a569-6a8e6caf35bd)
df.dropna(how='any').shape

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/285e85ee-2cea-4348-93d9-e2f011d7544e)
df.head()

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/5fba4320-3bb9-497d-ad85-c4216daf13de)
df.tail()

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/33555598-e151-41ca-8d6f-9c576c849a6c)
x=df.dropna(how='any')
x

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/24293499-83d4-426f-95fb-063f81f1a87a)
df.dropna(how='any').shape

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/b769a864-eb42-484a-87b5-8f2f2f74c8e0)
df.dropna(how='all').shape

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/615827d6-f4e4-4100-9a7a-168c90c8a751)
tot=df.dropna(subset=['TOTAL'],how='any')
tot

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/b9a006e0-1e52-488a-b9ed-88a2f5e2f677)
tot=df.dropna(subset=['M1','M2','M3','M4'],how='any')
tot

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/52a3abfd-3d97-4f27-84f7-6e1a60cd58cc)
df.fillna(0)

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/53720642-91b1-4e2d-833f-c2e6803acfff)
df.fillna(method='ffill')

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/7832d03e-1bd9-4d36-87af-894517320e2b)
df.fillna(method='bfill')

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/0f00b1db-ab6f-4c1a-8f6a-523749472dfd)
m=df.TOTAL.mean()
m

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/3c1fb8c1-f72e-40f6-9a8d-2aa67a474048)
df.TOTAL.fillna(m,inplace=True)
df

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/838b3123-ea16-4886-bec0-c809e4ea7625)
df.duplicated()

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/69fa046f-2083-489f-92ad-9f37e66c979f)
df.drop_duplicates(inplace=True)
df

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/dc647a3a-f976-442a-9671-59455d4af65d)
df['cd']=pd.to_datetime(df['DOB'])
df

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/0cd18070-5f52-4aa5-8de4-4c8077029802)

for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/1b9a9896-bb52-41f6-b080-e7fd5675bb6c)
import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)

![image](https://github.com/imthiyas19/ODD2023-Datascience-Ex01/assets/120353416/10a1c9cc-e1d7-427d-802b-280b85b27cb1)
```


# Result:
Thus,the given data is read,cleansed and the cleaned data is saved into the file.

