# Exno:1
Data Cleaning Process
## Name  : Vishnu KM
## Regno : 212223240185
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

## Data Cleaning
```
import pandas as pd
data=pd.read_csv("SAMPLEIDS.csv")
data
```

<img width="820" height="632" alt="image" src="https://github.com/user-attachments/assets/ff3152b7-0823-4949-b635-276ad8fa1a44" />

```
data.head()

```

<img width="790" height="205" alt="image" src="https://github.com/user-attachments/assets/70aca704-601b-4741-b1ca-5a44b6b57278" />

```
data.tail()
```

<img width="671" height="157" alt="image" src="https://github.com/user-attachments/assets/465c5e69-71c0-4b34-acfe-2b0c16c40200" />

```
data.isnull()
```

<img width="575" height="520" alt="image" src="https://github.com/user-attachments/assets/010e9b38-5f42-4dc5-9082-b85fdbccebb6" />

```
data.isnull().sum()
```

