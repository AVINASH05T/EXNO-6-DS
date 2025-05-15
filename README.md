# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
## NAME : AVINASH T
## REG NO  : 212223230026
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
 ```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/cc82d482-980e-4a00-91b3-733d49adafcb)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/6ff1fd4a-4405-4bd3-b692-b05ceae48fe6)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/user-attachments/assets/19525764-0a2e-4051-94bb-5488af55c5ce)
```
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
![image](https://github.com/user-attachments/assets/a90610a7-e17b-48e4-a16d-bdc6dd869cb1)
```
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
![image](https://github.com/user-attachments/assets/d2380dde-e181-416b-9b80-a276ad46c954)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/e6f5975f-8c1a-47a4-b740-fdc9c21d237c)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/2d6aefa9-b982-4649-9e0e-0de98a1a1522)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/9a074118-6366-40e8-8b89-f406b287beaa)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/742748c3-4edc-4945-8f14-8689760abba3)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/e8c8fc92-9254-4c46-af7d-a9697547eae8)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/9ae22c69-5016-4773-9eec-18430a13b4ec)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/bb0cfee3-6b89-4e80-8d70-e0cbba167a58)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/b20257e8-e015-4370-a5e1-73435b75bc4c)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/322c8a37-65f1-4792-9ea8-56bbe1620ef2)
```
df=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/2cf7e821-0f9d-435c-b777-7562c9b90c1f)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/358cf33c-a772-4211-8c75-8b21cfa02ab1)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/d380a5f4-fcae-4ded-bd71-7b75a92f0977)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/26d618b2-d6c6-41b1-bfed-93f72d43d2b6)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/7ec0f45b-e666-42ea-b3cb-cacef7fc9875)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/2beb9150-fda1-46d7-a7ff-df74c4ef2deb)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/36b6b56e-d80d-405e-b257-9f7607d884e7)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/931dc78a-c4c7-4991-a64a-4423283e6083)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/cda2a59b-8c33-4722-8376-9a96c2b3998b)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/b5b86156-595a-46bc-93d3-a199f028135f)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/73ea5694-3bae-4dc7-ba82-bfc3f7c9bad0)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/213ab2e1-ef09-42fb-ab94-fd634d50d2c1)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/cffd2b8d-06b4-4e7f-beb2-4937cf84b26a)

# Result:
 Thus, all the data visualization technique of seaborn has been implemented.
