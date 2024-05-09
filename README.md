# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
### Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:

STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Developed By : Shriram S
Reg.no: 212222240098
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/e26bea1d-1d65-49bd-a57d-68f683a7df75)


### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/6662762c-b6e3-4bcb-8f82-8b2168d815f8)

### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/d1ed3870-1415-4502-b39d-954ea93c44ce)


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/c6bdb7c4-a7e1-4115-8eb2-dd8f16018609)

### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/1e35948b-bfd8-45e4-becf-afcfa57d7bf8)

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/1023b92a-4f23-4978-a429-9a3dc8c9d888)

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/e5baaaff-58df-4053-85ec-6feed4d3fb4b)

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/79501a9c-6a75-4885-9f9e-cd15ad29c7b3)

### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/a66d284d-cbe4-4755-9415-d6a4fe51a8cc)

### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/9d17fb39-2d8b-4c9a-85cf-c7b8db2446f1)

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/ShriramGH/EXNO-6-DS/assets/117991122/39f3be24-1f1d-4242-ae4d-14ac508342fc)


## Result:
  
  ### Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

