EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
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
```python
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
<img width="638" height="447" alt="image" src="https://github.com/user-attachments/assets/b48e3ecd-0460-4034-bfd1-e6ac5c8e322b" />

```python
df=sns.load_dataset("tips")
df
```
<img width="552" height="404" alt="image" src="https://github.com/user-attachments/assets/04fdc321-572e-4f99-a639-765bd0737eae" />

```python
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
<img width="655" height="461" alt="image" src="https://github.com/user-attachments/assets/2365489f-a567-417e-ba89-be740ce38b94" />

```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-:Line Plot')
plt.xlabel('X-Label')
plt.ylabel('Y-Label')
```
<img width="654" height="492" alt="image" src="https://github.com/user-attachments/assets/60c09586-ca17-4684-839d-bcc6012112a6" />

```python
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
<img width="859" height="658" alt="image" src="https://github.com/user-attachments/assets/3dfad6a9-c54b-40ff-ac39-995b90ace889" />

```python
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
<img width="877" height="540" alt="image" src="https://github.com/user-attachments/assets/d38999a6-d5a9-4c9a-9041-de506966fb43" />

```python
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
<img width="616" height="445" alt="image" src="https://github.com/user-attachments/assets/5d2bf1b3-6429-463c-9a41-ee0e9752e97e" />

```python
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
<img width="689" height="484" alt="image" src="https://github.com/user-attachments/assets/bec75f60-0201-4ce3-b834-6c559dabb6f6" />

```python
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (2).csv")
tit
```
<img width="871" height="750" alt="image" src="https://github.com/user-attachments/assets/328d4d02-0dab-4291-be43-f66fc9c3ae04" />

```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
<img width="882" height="594" alt="image" src="https://github.com/user-attachments/assets/edf2a04d-147d-432d-8c08-34c4c3672e8e" />

```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')
plt.title("Fare of Passenger by Embarked Town,Divided by Class")
```
<img width="834" height="501" alt="image" src="https://github.com/user-attachments/assets/6e8e45d2-0ea6-4f5e-afc6-9cd77da8cc7e" />

```python
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
<img width="697" height="492" alt="image" src="https://github.com/user-attachments/assets/0fef0b71-dbf3-42ae-9882-6f3d57a2e886" />

```python
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
```
<img width="272" height="446" alt="image" src="https://github.com/user-attachments/assets/03ce6f2c-901c-46fb-8924-472e09d46764" />

```python
sns.histplot(data=num_var,kde=True)
```
<img width="688" height="463" alt="image" src="https://github.com/user-attachments/assets/dc9631bd-900e-400d-9842-8d0ee5e54632" />

```python
sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)
```
<img width="659" height="455" alt="image" src="https://github.com/user-attachments/assets/1badfbfd-fc93-45e1-943d-2995aa84fc47" />

```python
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
```
<img width="659" height="367" alt="image" src="https://github.com/user-attachments/assets/be4e1cb9-2afc-4a3a-bc7e-32228d588103" />

```python
sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Student Marks')
```
<img width="859" height="500" alt="image" src="https://github.com/user-attachments/assets/295484bb-3dc5-4e1f-83ec-220e4c1a1621" />

```python
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
<img width="648" height="463" alt="image" src="https://github.com/user-attachments/assets/39548197-234e-49a1-9a1f-6376d79a810f" />

```python
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
<img width="691" height="475" alt="image" src="https://github.com/user-attachments/assets/370b6aa9-6741-4913-bad1-ce3d64830c14" />

```python
sns.boxplot(x='Pclass',y='Age',data=tit,palette='rainbow')
plt.title("Age by Passenger Class,Titanic")
```
<img width="830" height="576" alt="image" src="https://github.com/user-attachments/assets/2472fd51-af7d-4630-82e0-fdf850c6ce7a" />

```python
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
<img width="676" height="472" alt="image" src="https://github.com/user-attachments/assets/18660361-e2ba-4f7a-aad8-48fabb3d5a03" />

```python
import seaborn as sns
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip)
```
<img width="710" height="476" alt="image" src="https://github.com/user-attachments/assets/572d6087-b610-4dc7-8b91-bdeaae146e84" />

```python
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
<img width="640" height="467" alt="image" src="https://github.com/user-attachments/assets/100fb89c-549a-416e-a402-88775f1903ef" />

```python
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x="tip",y="day",data=tip)
```
<img width="736" height="461" alt="image" src="https://github.com/user-attachments/assets/97dc4182-12c9-44aa-8391-3a08e1804d38" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)
```
<img width="730" height="462" alt="image" src="https://github.com/user-attachments/assets/672b953a-cfc4-479d-80e0-f1223e501984" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```
<img width="719" height="487" alt="image" src="https://github.com/user-attachments/assets/c8b368f1-db83-4548-bdb7-7fb45accd765" />

```python
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```
<img width="719" height="487" alt="image" src="https://github.com/user-attachments/assets/7b3d691d-25a7-4b69-80ef-6c981c7ed2ff" />

```python
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted:\n")
print(data)
```
<img width="342" height="220" alt="image" src="https://github.com/user-attachments/assets/300e6b09-b027-4f49-93ce-1975525fe204" />

```python
hm=sns.heatmap(data=data)
```
<img width="631" height="423" alt="image" src="https://github.com/user-attachments/assets/9af67844-bc8e-4785-9443-f70e66de0430" />

```python
tips=sns.load_dataset('tips')
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)
```
<img width="614" height="450" alt="image" src="https://github.com/user-attachments/assets/3e5e4647-ac33-460c-a03d-046ebae1b9d3" />

# Result:
Data Visualization using seaborn python library for the given datas has been performed successfully. 
