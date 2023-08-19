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
### LOAN_DATA_CSV
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
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

### DATA_SET.CSV
```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
# OUTPUT
## FOR LOAN_DATA:
#### DATA
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
```
![261023526-2a6c2342-4f9d-465a-b0c9-6b34d3c0036a](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/5e950834-9ca4-4422-b9c9-920d6c7e662e)

## NON NULL BEFORE
```
df.info
```
![261024564-d2eb26c9-1a50-490e-b5eb-916682eccc34](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/174c518c-46ce-4737-a5bd-104a0bb7ff84)

## MODE
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![261025266-ceb9d14e-ce00-47d6-b1dd-c175745c1dd5](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/8856a967-f478-4c7c-87e9-3416e31cb4aa)

## MEAN
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![261026074-5e393bb6-7958-47b6-821d-4248b6c0393c](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/b96d1f12-e128-48eb-8d4c-2b410e437b10)

## MEDIAN
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![261026497-ea74ab58-1c5b-4021-9a6f-226c2a04b18b](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/1ae6e95d-5752-4fa8-9376-0f40a89f9694)

## NON NULL AFTER
```
df.info()
```
![261026978-b532b301-1fad-436c-bf15-3ee2535e4e90](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/e0f9387e-170f-4c8c-9e64-bc9ac5ecd33a)

```
df.isnull().sum()
```
![261027321-3dd82ddd-f3b6-438c-af5c-b5faada58070](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/948461fd-dbef-4110-98a7-25d23af5858b)

# FOR DATA_SET:
### DATA
```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
```
![261037224-3a57bf29-ca7f-447e-84a6-8c4de79cc6c4](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/77d617c6-1167-4db1-a074-1bb62ded4062)

## NON NULL BEFORE
```
df.info()
```
![261037838-404c5862-d322-411f-a7e5-74006a11526a](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/8ab7f078-1843-4e49-83c2-356ac0653b32)

```
df.isnull()
```
![261038196-8771c2a8-5e00-47ba-950f-5910087c86a6](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/97f25a5b-5524-4703-a20f-0f3d71bcae9f)

```
df.isnull().sum()
```
## MODE
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![261039081-73f49e75-e6f9-4bff-80a1-b94529a931ee](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/1e4538f0-b049-4ae4-882f-2a0d1d8e8090)

## MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![261039612-b62342d9-97fa-44f1-ac58-fe1396bfeb16](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/1ee02f2b-cd0f-40da-96d1-07cb512c01ae)

## MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![261040052-e4fb6a1b-4ab6-4187-96b6-fd2659276687](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/492fc25f-09cd-4c49-a5b8-d9fae3f2c462)

## NON NULL AFTER
```
df.info()
```
![261042558-97d0c270-a76d-4c88-8eeb-84d45f40110c](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/16a37c11-b4ac-4f75-bfed-39179e9f16e8)
```
 df.isnull()
```
![261042976-cb5c56ff-529e-4d4d-8896-d48595d29636](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/5da302fb-fc71-4baa-9566-24811ede6975)
```
df.isnull().sum()
```
![261043279-918a4cc2-154d-40ac-99f2-da647104206b](https://github.com/Rohithravi333/ODD2023-Datascience-Ex01/assets/119394126/e7d8752f-8504-4506-ae7f-d260d6bd8808)

# RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
