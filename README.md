# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
## Data cleaning
### 1) Read and display DataFrame
```
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/dac5644e-3a35-44f2-94f6-2ce9cdf54967)

### 2) Display head
```
df.head(4)
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/ec48870c-92dc-4dab-be14-3fce58c52903)
###  3) Display tail
```
df.tail(4)
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/48872df1-0baf-44f9-898b-6b4184455bfd)
### 4) Info of datafram
```
df.info(3)
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/467a4c65-3abd-4c08-9fa0-a9f29fe52773)
### 5) Describe about the dataframe
```
df.describe()
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/a6d2db4a-730a-4b63-b071-f348fa8cf32a)
### 6) Shape of the datafram
```
df.shape
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/a6b940dd-6770-48a1-a2e2-d0cf89a77387)
### 7) Checking tha NUll values
```
df.isnull().sum()
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/489eee5e-3421-4086-bbf8-be7c69ea94f5)
### 8) Drop the Null values
```
df.nunique()
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/42e3c59b-1999-45e9-914c-4a7eb8b59307)
### 9) Finding the mean value
```
mn=df.TOTAL.mean()
mn
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/103262c2-7239-4b13-86c8-5d8fe798ad73)
### 10) Fill Null value with Mean value
```
df.TOTAL.fillna(mn,inplace=True)
df
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/0c9e4db4-5785-4444-aec4-808e08876d25)
### 11) Finding minimum value
```
mn=df.M4.min()
mn
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/cd7988c1-3ece-4a02-8641-9b4af3127ca8)
### 12) Printing only Date of Birth
```
df['cd']=pd.to_datetime(df['DOB'])
df['cd']
```
![image](https://github.com/Nishanth-018/exno1/assets/149347651/d8b1cefe-0244-4f1b-ba90-44b97139c819)
## Result:
Thus the program for data cleaning using python has executed successfully.


