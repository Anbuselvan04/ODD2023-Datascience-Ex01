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

## CODE
```
import pandas as pd
df = pd.read_csv("SampleDS.csv")
df

df.shape

df.describe()

df.info()

df.isnull().sum()

df.dropna(how='any').shape

x = df.dropna(how='any')
x

df.dropna(how='all').shape
df

tot = df.dropna(subset=['TOTAL'],how='any')
tot

tot = df.dropna(subset=['M1','M2','M3','M4'],how='any')
tot

df.fillna(0)
df

df.fillna(method='ffill')

df.interpolate()

mn = df.TOTAL.mean()
mn

df.TOTAL.fillna(mn,inplace=False)

td = df.TOTAL.fillna(mn,inplace = True)

df

l = df.M1.interpolate()
l
df.isnull()

df.notnull()

df.dropna()

df.head()

df.tail()

df.info()

df.describe()
df

df.duplicated()
df

df.drop_duplicates(inplace=True)
df

df['cd']=pd.to_datetime(df['DOB'])
df

for x in df.index:
  if df.loc[x,'AVG']>100:
    df.drop(x,inplace = True)
df

```
## OUTPUT
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/4df3b6d2-cc6c-4ee9-b01c-767a9b301764)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/1021fe95-5f7c-4ff6-be8e-6ede7a04fcbd)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/221d615a-e441-4cd5-816b-379f7405e7c9)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/5330e261-8ab3-4325-b964-fae1e97ccc80)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/351727d0-0d53-4531-85c2-6c1a3871a323)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/efea802a-2750-40e2-82b8-5220b703109d)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/380bcaa6-743f-4198-99ab-813ef07730e4)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/efe55b67-41a9-461b-bfa0-5110d462bc68)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/78bbb74c-2b91-4c5b-b208-80f51d0c1012)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/6cc5cea9-84f5-45a2-9155-0bf4211517e3)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/d23c859d-6152-4d41-91f3-84db4ffc7b0c)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/82da517c-c833-4495-bef6-b9e937b4f661)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/bcfb21a4-9ac8-4d7a-85cc-5a54e6ab055e)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/919a3f18-e722-44fa-93e5-6de66093a0cd)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/fc93ffef-acaa-488b-a983-fd1597310ed5)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/cc6cc3be-3af3-4b39-adc5-67c2bb0fdffe)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/471f7175-b436-40f1-af0b-173314ad4943)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/057a0eaf-816d-4db5-aefc-73d91958b239)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/356c3a44-9b46-44ab-994c-288cb1bfcdd2)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/e6bb97ca-550e-4dec-87e4-a9e501d1b247)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/88746d3a-5545-4160-8be8-2af7cae504eb)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/16446e5f-3aa8-4007-844c-1dc1e2744873)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/a449ebbe-4b1a-414a-9141-66a36418d012)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/5dd36de7-0b62-4430-ae4c-82fbe9433760)
![image](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex01/assets/119410896/bfe93cbe-35c3-42e5-8aa6-a1802aeb997f)
