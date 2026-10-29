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
```
import pandas as pd
val=pd.read_csv("SAMPLEIDS.csv")
print(val)
val.shape
val.head(7)
val.tail()
val.info()
val.describe()
val.isnull()
val.notnull()
val.isnull().sum()
val.isnull().any()
val.dropna()
val.dropna(axis=1)
val.fillna(8)
val.fillna(method='ffill')
val.fillna(method='bfill')
val.fillna({'GENDER':'MALE','NAME':'RAJA'})
ir=pd.read_csv("iris.csv")
ir.isnull().sum()
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
sns.boxplot(x='sepal_length',data=ir)
Q1=ir.sepal_width.quantile(0.25)
Q3=ir.sepal_width.quantile(0.75)
IQR=Q3-Q1
print(IQR)
```
<img width="575" height="649" alt="image" src="https://github.com/user-attachments/assets/88130ec1-1db4-4c51-926b-a5a4d4b45cc2" />
<img width="923" height="625" alt="image" src="https://github.com/user-attachments/assets/c148caf4-1486-4193-9a43-db244eaaf112" />
<img width="828" height="683" alt="image" src="https://github.com/user-attachments/assets/89bf9819-fd98-4671-86ae-b4b844f47b16" />
<img width="715" height="743" alt="image" src="https://github.com/user-attachments/assets/3a54ad1a-d1a0-49fb-a0ed-fdbfec3a0328" />
<img width="861" height="561" alt="image" src="https://github.com/user-attachments/assets/2f2f81ac-14d3-4ad3-88a7-c820581bc488" />
<img width="608" height="803" alt="image" src="https://github.com/user-attachments/assets/3c95eabe-2fb7-4bbd-bcf5-65fef66bbe46" />
<img width="570" height="794" alt="image" src="https://github.com/user-attachments/assets/1aa912a6-ab45-4381-88f5-fa82488c9a9d" />
<img width="556" height="597" alt="image" src="https://github.com/user-attachments/assets/50f17c4f-0b2f-429f-b500-7feb3d11f5a7" />
<img width="572" height="561" alt="image" src="https://github.com/user-attachments/assets/928ee7d4-f160-4112-89b5-cdc9f9656f3a" />
<img width="575" height="618" alt="image" src="https://github.com/user-attachments/assets/b8bcc7f2-4604-47ed-a3d2-5e15be658c41" />
<img width="669" height="604" alt="image" src="https://github.com/user-attachments/assets/3b70b7f7-28a1-422b-9b08-7f5ef857782d" />
<img width="608" height="754" alt="image" src="https://github.com/user-attachments/assets/2a673969-7010-4c00-ba3a-7d6f9c13bad6" />

# Result
The given data has been successfully read, cleaned by handling duplicates and missing values, and saved to a new file named cleaned_data.csv.
