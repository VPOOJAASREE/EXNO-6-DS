# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

```
NAME: V. POOJAA SREE
REG.: 212223040147

```

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

# Output:

![1](https://github.com/user-attachments/assets/0411b067-2acf-4af8-8e86-44f3c8fd2b0b)


```
df = sns.load_dataset("tips")
df

```

# Output:

![2](https://github.com/user-attachments/assets/c3f8f82c-c47e-4510-94dd-fdc61b38d7a3)


```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

```

# Output:

![3](https://github.com/user-attachments/assets/4de586b6-e509-41f8-afb1-a737683d4c75)


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

# Output:

![4](https://github.com/user-attachments/assets/45bd97d3-1316-4973-a8d9-0c72fca1f4de)


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

# Output:

![5](https://github.com/user-attachments/assets/f7475369-c23e-4489-9931-9bed3759a554)


```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

```

# Output:

![6](https://github.com/user-attachments/assets/4521a2f1-8bbe-4136-bbe4-4d454a089d66)


```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)

```

# Output:

![7](https://github.com/user-attachments/assets/c4b27dfb-197f-404e-9552-d46cc677c3d0)


```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')

```

# Output:

![8](https://github.com/user-attachments/assets/e725be90-56ca-4609-a9e6-1ee79009bcc5)


```
ti=pd.read_csv("/content/titanic_dataset (2).csv")
ti

```

# Output:

![9](https://github.com/user-attachments/assets/e1c1db48-a5b3-49fd-bda6-068c3b2663c2)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=ti, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")

```

# Output:

![10](https://github.com/user-attachments/assets/01535b4f-2c5b-4cdb-aaba-0de20caae90a)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=ti, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")

```

# Output:

![11](https://github.com/user-attachments/assets/b67780fc-0c03-4a9e-8e55-b30e3e01ae22)


```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')

```

# Output:

![12](https://github.com/user-attachments/assets/e9c37102-9416-4bba-929d-7d1f97f22e9c)


```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var

```

# Output:

![13](https://github.com/user-attachments/assets/cc61b216-079b-4ef5-8478-1b1a7fb22236)


```
sns.histplot(data = num_var, kde = True)

```

# Output:

![14](https://github.com/user-attachments/assets/c2bb40db-242e-4074-97be-77d6a0497e2a)


```
df=pd.read_csv("/content/titanic_dataset (2).csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)

```

# Output:

![15](https://github.com/user-attachments/assets/820a3f64-55bf-4e9c-8e92-5281c0aa2c8f)


```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])

```

# Output:

![16](https://github.com/user-attachments/assets/d0af21e3-4b37-470d-8d41-6846439790d9)


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

```

# Output:

![17](https://github.com/user-attachments/assets/d06c5106-a3c9-474b-8c38-44c6f9b4167d)


```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")

```

# Output:

![18](https://github.com/user-attachments/assets/035a12c8-93f8-4c7c-8c8f-7066be820856)


```
mart=pd.read_csv("/content/titanic_dataset (2).csv")
mart

```

# Output:

![19](https://github.com/user-attachments/assets/faef04d2-e590-439a-8633-da4dfedc2085)


```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10) 

```

# Output:

![20](https://github.com/user-attachments/assets/56c806ae-12f3-4595-880f-97859f65c41c)


```
sns.kdeplot(data=mart,x='PassengerId')

```

# Output:

![21](https://github.com/user-attachments/assets/d72b393f-e003-4e83-859b-a4635ca71d2a)


```
sns.kdeplot(data=mart,x='Age')

```

# Output:

![22](https://github.com/user-attachments/assets/9f34416c-fdba-4b60-9f4d-833bb8d49694)


```
sns.kdeplot(data=mart)

```

# Output:

![23](https://github.com/user-attachments/assets/c2b89ec3-9828-430b-bef0-47bc3aa24c97)


```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')

```

# Output:

![24](https://github.com/user-attachments/assets/9dcc24ca-9228-49f1-8234-fb14fbab5f4e)


```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')

```

# Output:

![25](https://github.com/user-attachments/assets/bbaad8bf-c72f-43c9-845a-0db075ddbace)


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)

```

# Output:

![26](https://github.com/user-attachments/assets/f87b8f57-2e77-4d3f-ba17-7072a70faeb3)


```
hm=sns.heatmap(data=data)

```

# Output:

![27](https://github.com/user-attachments/assets/97f1edf5-0f3a-48a0-bf3e-a9a1bc7d4666)



# Result:

```
Thus, all the data visualization techniques of seaborn has been implemented successfully.

```
