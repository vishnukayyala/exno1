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
<img width="122" height="217" alt="image" src="https://github.com/user-attachments/assets/07744a83-e508-404a-a926-605e0257457f" />
```
import numpy as np
import pandas as pd
df=pd.read_csv("heights.csv")
df
```

<img width="177" height="361" alt="image" src="https://github.com/user-attachments/assets/cfc2a520-0c69-4f46-a97b-b603453fc681" />

```
import scipy.stats as stats
q1 = df['height'].quantile(0.25)
q2 = df['height'].quantile(0.5)
q3 = df['height'].quantile(0.75)
iqr = q3-q1
iqr

```

<img width="166" height="41" alt="image" src="https://github.com/user-attachments/assets/77c50179-11e6-43bf-838e-89c9bc47baf5" />

```
low = q1 - 1.5*iqr
print(low)
high = q3 + 1.5*iqr
print(high)
```

<img width="147" height="47" alt="image" src="https://github.com/user-attachments/assets/3f4d3793-91a5-4bc9-8aa1-ef6393cea8e2" />

```
df1 = df[((df['height'] >=low)& (df['height'] <=high))]
df1
```

<img width="147" height="308" alt="image" src="https://github.com/user-attachments/assets/ba2cfbfc-ddd9-499d-aeb7-2a44f00724fa" />

```
z = np.abs(stats.zscore(df['height']))
z
```

<img width="270" height="246" alt="image" src="https://github.com/user-attachments/assets/7ce477e6-e8c8-4908-9dd9-250c2119d535" />

```
df1 = df[z<3]
df1
```

<img width="191" height="336" alt="image" src="https://github.com/user-attachments/assets/94f0399e-1f9d-4f33-b6d2-b7730079e1a2" />



# Result

Thus we have cleaned the data and removed the outliers by detection using IQR and Z-score method.

