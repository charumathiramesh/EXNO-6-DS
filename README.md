# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```c
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

![323212197-18a0f3c8-10a6-42b4-9eb3-45770f741ac3](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/1a0502b9-d48a-486b-ba29-560f23668f82)

```c
df = sns.load_dataset("tips")
df
```

![323212387-0124fef5-dcba-4c31-9831-db85384d9c5a](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/e767442e-6dce-4842-92cb-5617e4d0c8c1)

```c
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

```
![323212532-1bbe2d28-735c-4114-aff7-9030d334c830](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/958c4d40-03b1-443f-919f-cf5d79269f67)

```c
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")

```
![323212649-4d6c2a15-2352-4ba4-bd6b-97a54cd93ce7](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/fe62a55e-8896-4772-b87f-da622739a38b)

```c
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()

```
![323212764-86b30955-7bb2-44af-92d1-39e8be4b56ea](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/62e2fcea-1976-473c-8528-347b788793be)

```c
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

```

![323212867-27a32e9f-e734-4f47-adf1-bafddba998c3](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/19cf5fd3-5ba3-4566-b2bd-46661d9cabfb)

```c

years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```c
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)

```

![323213027-31f5b45b-5a80-4259-a259-a4cecee25ee5](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/c47a8089-d491-4bf4-a7a0-1c6fe996a2b8)

```c
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')

```

![323213184-359daca3-3920-4c78-b593-7d660c09cc36](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/7fe84c9d-a4f0-48d0-9d1b-d2a4d70cc674)

```c
tit=pd.read_csv("titanic_dataset.csv")
tit
```

![323213349-b749f1ee-b0a6-4a67-a340-f9cae8a8290a](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/191321a3-3fe1-4559-8161-9215c1f377a4)

```c
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")

```
![323213630-03dbd087-2a3e-4bfa-8847-bc2e9bbe7cc3](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/685d7037-c06e-4f6c-a895-1c12c359ba3e)

```c
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![323213737-090114ac-6d91-4117-80ca-2bb2fe72af26](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/82aa1726-38a8-48de-8a1e-cb9d2601ce72)

```c
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![323213860-b7984ccc-60c8-4cf2-ba31-0dafe6119b91](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/38b73bc2-1a89-4008-8e13-a90e902e07ec)

```c
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var

```

![323213974-5e149370-320f-4c4b-b6e9-93839011d166](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/4baba1d4-29c8-4e54-90df-a4ac4bc1e1ac)

```c

sns.histplot(data = num_var, kde = True)
```
![323214138-39b3d5fa-e8af-45f5-afb2-2875c766a5e6](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/b18d2e46-1956-418a-ae70-1b677cf64aee)

```c
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![323214244-e8b91ede-1cc0-4087-beb6-c3c56d8137ee](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/ff370859-1c3e-4dcb-a384-f6ce3c61a74d)

```c
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![323214357-c7d0ff3a-e9a0-4369-a9c9-9229d84776c3](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/1e81343b-5f9f-4a4e-8e34-e45ccbfad9b5)

```c
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

```
![323214462-dc5777c4-83cf-47d2-ba0c-b6bb81547441](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/55bb0516-cdab-4883-b988-a1bfca203693)

```c
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![323214570-8dec8878-d0bb-46ca-bc17-095aba86cffd](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/13fefd2c-10b9-4273-847b-027a7f9f8669)


```c
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![323214740-32c63c42-35dc-47df-b851-c13e54c166aa](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/ec5ccb4d-75d5-4855-bb4f-c5808200b367)

```c
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```

![323214850-bcbe61b9-5739-4853-a186-302272133266](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/d1708160-4246-4784-9309-643fe5069070)

```c
sns.kdeplot(data=mart,x='PassengerId')
```
![323214956-727482e0-5b45-47e4-8542-93ebc9cfb5b7](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/32f7592c-f03d-4590-8df8-b5af7ecec802)

```c
sns.kdeplot(data=mart,x='Age')
```

![323215089-9bb955c9-ba97-48ab-b158-35a44931ccf6](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/05cca1d7-a668-4971-af4e-118a93b2d37c)

```c
sns.kdeplot(data=mart)
```
![323215191-8cc57d95-8df2-4483-8c98-2edbcfb68b0c](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/7bd3d1b3-0cf8-407c-ac2f-3791df9d6759)

```c
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

![323215343-f56e128b-5393-46e8-acb6-33bfd6fde4a9](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/c7c220d1-d906-490f-819c-2aae2e7507bd)

```c

sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![323215571-4f66d13f-770e-4b17-b29d-74f42cb4395e](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/402508bf-20a5-4b86-8d53-56c395f3d8cc)

```c
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![323215754-5eba9f52-3c11-4640-b78f-451463d24415](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/134af5a9-8bd5-46dd-a548-7005dc6337cd)

```c
hm=sns.heatmap(data=data)
```
![323215874-4bbbf59a-e638-4c7b-bf5c-5298f9bada3b](https://github.com/charumathiramesh/EXNO-6-DS/assets/120204455/da5ee4d7-f357-429b-87c8-0120837fa15f)



## Result:

Thus, all the data visualization techniques of seaborn has been implemented.


