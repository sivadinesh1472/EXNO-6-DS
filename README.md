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

```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
```
```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
<img width="564" height="424" alt="image" src="https://github.com/user-attachments/assets/7d255a33-5f1e-40f1-8471-4e4e929f2fa1" />

```
df = sns.load_dataset("tips")
df
```
<img width="476" height="374" alt="image" src="https://github.com/user-attachments/assets/4b0e5a50-71d7-417e-be83-63aade2e2ef6" />

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```

<img width="639" height="449" alt="image" src="https://github.com/user-attachments/assets/c472129b-70f4-
49c6-a3af-ec62a7050ed5" />

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
<img width="577" height="455" alt="image" src="https://github.com/user-attachments/assets/1877b2d3-7086-42c7-8284-25291629610f" />

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

<img width="663" height="525" alt="image" src="https://github.com/user-attachments/assets/9833251d-d581-4b53-bbc9-1b7adf588c72" />

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

<img width="575" height="392" alt="image" src="https://github.com/user-attachments/assets/9cf82d5c-b4a2-41f0-bea4-89477f57674d" />

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

<img width="593" height="396" alt="image" src="https://github.com/user-attachments/assets/7413ae88-9151-4105-b45b-7791647192d5" />

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

<img width="621" height="456" alt="image" src="https://github.com/user-attachments/assets/0ff80c3b-b1fd-4934-8eb3-aad16537314f" />

```
import pandas as pd
tit=pd.read_csv("titanic_dataset.csv")
tit
```
<img width="1088" height="365" alt="image" src="https://github.com/user-attachments/assets/caa59915-3eba-466d-94f5-954a196cf38b" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```

<img width="627" height="440" alt="image" src="https://github.com/user-attachments/assets/96049ce7-963f-429f-a0e1-94fb1f01f8b4" />
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

<img width="630" height="428" alt="image" src="https://github.com/user-attachments/assets/860af233-7c32-42ea-bea2-e170e899dd0c" />

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

<img width="592" height="466" alt="image" src="https://github.com/user-attachments/assets/19c45920-bc8b-481f-b324-47e2a423cfd6" />


```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

<img width="406" height="192" alt="image" src="https://github.com/user-attachments/assets/9cd6f0f1-31b0-49da-be2b-0b6e76be5e00" />

```
sns.histplot(data = num_var, kde = True)
```

<img width="652" height="427" alt="image" src="https://github.com/user-attachments/assets/691b6fe6-a9e5-4017-82ed-bbfed3a828ec" />


```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

<img width="635" height="432" alt="image" src="https://github.com/user-attachments/assets/ad5a73de-2163-4227-ae2a-008ce541e587" />


```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

<img width="622" height="419" alt="image" src="https://github.com/user-attachments/assets/d1de5cdb-d4f9-49ed-9605-25a3ea079211" />


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

<img width="580" height="430" alt="image" src="https://github.com/user-attachments/assets/5426ff39-ed62-4732-a888-3d374c022da2" />

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

<img width="612" height="442" alt="image" src="https://github.com/user-attachments/assets/1edcf29a-a481-435c-90cf-a3beb6851740" />

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

<img width="1030" height="369" alt="image" src="https://github.com/user-attachments/assets/39a25205-6da8-4dfd-ba3c-9d123ebd20b8" />

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```

<img width="778" height="307" alt="image" src="https://github.com/user-attachments/assets/d4efde0f-ba19-4bbb-aef4-30cae16df156" />

```
sns.kdeplot(data=mart,x='PassengerId')
```

<img width="621" height="429" alt="image" src="https://github.com/user-attachments/assets/60781fc2-c817-4c1a-ae6f-b17fe1ea2db2" />


```
sns.kdeplot(data=mart,x='Age')
```

<img width="634" height="428" alt="image" src="https://github.com/user-attachments/assets/2e3e9d62-a2dc-4c59-b1dc-368bf0fc0090" />

```
sns.kdeplot(data=mart)
```

<img width="627" height="413" alt="image" src="https://github.com/user-attachments/assets/f0229881-977a-48c2-9abb-97d0e73162dd" />

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

<img width="619" height="435" alt="image" src="https://github.com/user-attachments/assets/6d90fda7-eb79-4bd8-a394-d56529ea061f" />


```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

<img width="635" height="431" alt="image" src="https://github.com/user-attachments/assets/b6c45c2e-70ea-48d8-9f32-1081ee160876" />


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

<img width="550" height="369" alt="image" src="https://github.com/user-attachments/assets/e4665340-ab00-4160-8b05-5dd78534e18a" />


```
hm=sns.heatmap(data=data)
```


<img width="539" height="403" alt="image" src="https://github.com/user-attachments/assets/9bf250ba-2839-47d7-8621-b110f3a62b7e" />

# Result:
 Include your result here
