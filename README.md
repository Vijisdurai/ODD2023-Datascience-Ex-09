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

# 1) Which day of the week has the highest total bill amount ?
```python
sns.barplot(x=df['day'],y=df['total_bill'],hue=df['day'])
plt.legend(loc="center")
plt.title("Highest Total Bill Amount by day of the week")
plt.show()
```
# ouput :
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/ffb8cdb1-19c9-48c1-9e26-1dafe8118b10)

# 2) What is the average tip amount given by smokers and non_smokers?
```python
sns.boxplot(x=df['smoker'],y=df['tip'],hue=df['smoker'])
plt.title("Average Tip Amount given by Smokers and Non-smokers")
```
# output :
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/ed0166ca-bf55-4bb3-98b7-f9a087f94f95)

# 3) How does the tip percentage vary based on the size of the dining party?
```python
df["tip_percent"]=df["tip"]/df["total_bill"]
sns.scatterplot(x=df['size'],y=df['tip_percent'],data=df)
plt.title("Tip Percentage by Dining Party size")
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/148a9f12-d8d0-4717-8df0-d98999c66caa)

# 4) Which gender tends to leave higher tips?
```python
sns.boxplot(x=df['sex'],y=df['tip'],hue=df['sex'])
plt.title("Tips BAsed on gender")
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/43ba394c-372b-4633-a1c5-46f3234b613f)

# 5) Is there any relationship between the total bill amount and the day of the week?
```python
sns.scatterplot(x=df['day'],y=df['total_bill'],hue=df['day'])
plt.legend(loc="best")
plt.title("Total bill amount by day of the week")
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/e34a1607-4114-415f-b82d-436ff79f85cf)

# 6) How does the distribution of total bill amounts vary across different time periods (lunch vs. dineer)?
```python
sns.histplot(data=df,x="total_bill",hue="time",element="step",stat="density")
plt.title("Distribution of Total Bill Amounts by Time of Day")
plt.show()
```
# Output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/0dbdbfde-7864-4575-b8bb-de56e093f7c4)

# 7) Which dining party size group tends to have the highest average total bill amount?
```python
sns.barplot(x=df['size'],y=df['total_bill'],hue=df['size'])
plt.title("Average total Bill amount by Dininng party size]")
plt.show()
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/74c7dcb4-f368-49a9-8bbf-90dc0475de23)

# 8) What is the distribution of tip amounts for each day of the week?
```python
sns.boxplot(x="day",y='tip',data=df)
plt.title("Tip amount by dy of Week")
plt.show()
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/2428496f-e56f-4cfe-a1f6-f034d05eec83)

# 9) How does the amount vary based on the type of service (lunch vs. dinner)?
```python
sns.violinplot(x="time",y="tip",data=df)
plt.title("Tip Amount time Of day")
plt.show()
```
# Output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/5284120b-1f34-413a-ab7f-e8dde67acf27)

# 10) Is there any correlation between the total amount and amount and the tip amount ?
```python
sns.scatterplot(x="total_bill",y="tip",data=df)
plt.title("Correaltion between Tip Amount and Total Bill Amount")
plt.show()
```
# output:
![image](https://github.com/Vijisdurai/ODD2023-Datascience-Ex-09/assets/118343184/410a5577-4fe5-42d5-bde7-17b79e343d9a)










