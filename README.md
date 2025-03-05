# Exno:1
Data Cleaning Process

# AIM:
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm:
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output:
```
import pandas as pd
data = pd.read_csv("SAMPLEIDS.csv")
data
```

![image](https://github.com/user-attachments/assets/888db627-ab1e-4e8b-bc01-deda9eb224ce)

```
data.head(7)
```

![image](https://github.com/user-attachments/assets/4d112426-2a1f-4640-aa47-8ba918e15bd7)

```
data.tail(7)
```

![image](https://github.com/user-attachments/assets/135d0182-d4d7-4fd9-84ba-6da22add67ab)

```
data.isnull().sum()
```

![image](https://github.com/user-attachments/assets/5476da7f-a97a-4572-86f8-914744b66914)

```
data.isnull().any()
```

![image](https://github.com/user-attachments/assets/5af91573-8de4-4d78-a12d-b5112762d237)

```
data.dropna()
```

![image](https://github.com/user-attachments/assets/e37f1190-d134-49bd-9096-a71d7e3f3948)

```
data.fillna(1000)
```

![image](https://github.com/user-attachments/assets/e99d14f6-a345-44d9-badc-35ce1b89a9b6)

```
data.fillna(method='ffill')
```

![image](https://github.com/user-attachments/assets/7fd3aab1-1d51-40f6-aa0c-5b5656e3288f)

```
data.fillna(method='bfill')
```

![image](https://github.com/user-attachments/assets/59442240-c125-4a97-8dee-908f0c896052)

```
data_dropped = data.dropna()
data_dropped
```

![image](https://github.com/user-attachments/assets/0e36902f-eced-4075-ab44-af7ed30dce92)

```
 data.fillna({'GENDER':'MALE','NAME':'SRI','ADDRESS':'POONAMALEE','M1':98,'M2':87,'M3':76,'M4':92,'TOTAL':305,'AVG':89.999999})
```

![image](https://github.com/user-attachments/assets/5b1a7f05-28fa-4717-a2eb-52864643c9c2)

# Result:
Thus to read the given data and perform data cleaning and save the cleaned data to a file done successfully.
