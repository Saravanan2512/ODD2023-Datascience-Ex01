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

# CODE 
```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
# Output
# display
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/abf2d95d-2dea-41c3-8be3-f67d80b7eda1)
# Non null before
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/a233c5d8-f01c-4470-9360-6f046b91343e)
# Mode
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/00ea7212-c5b2-4608-91bd-56f8bddfed54)
# Mean
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/67dd25e1-00ea-4b2b-a253-db775b1d9db1)
# Median
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/23df26b7-eac2-4044-b0cc-17714db2d7df)
# Isnull
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/5b535917-522f-48fe-b926-f58257e819c4)
# Non null After
![image](https://github.com/Saravanan2512/ODD2023-Datascience-Ex01/assets/144979117/e13959dc-22cd-44a1-a59e-cdbaf859115a)

## Result
Thus,the given data is read,cleansed and the cleaned data is saved into the file.





