# Ex-09-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
### Data Preprocessing
```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt
df=sns.load_dataset("tips")
print(df)
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/f649fbeb-c876-4974-a491-8287aa794eeb)

```python
df.isnull().sum()
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/993b87d4-ce6c-45b2-b659-c5070cf8a2ab)

### Handling Outliers
```python
plt.figure(figsize=(5,5))
plt.title("Data with Outliers")
df.boxplot()
plt.show()
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/2e591fd9-b43e-43b5-89c2-00306069870c)

### Removing outliers
```python
plt.figure(figsize=(5,5))
plt.title("Data with Outliers")
df.boxplot()
plt.show()
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/ce5f2080-e339-44ac-9904-1eef48114ef6)












