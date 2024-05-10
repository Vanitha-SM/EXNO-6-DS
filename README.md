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
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/40059c7b-cd89-4217-bf4a-88fffed5345e)

### 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/0219dc4e-562c-4b51-b325-5de466e8d91d)

#### 2.Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/ea75dce9-a958-409d-9458-a5f2897644ed)

## TO VISUALIZE RELATIONSHIPS

### 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/45f5480a-8cb3-4c87-9b7d-321e4a8276d5)
### 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/02351a22-a3d8-4fc0-b107-e697742695a3)

### 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/4687c962-5273-49dd-a80f-82e825996bf6)

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/cd1b48d0-9e48-47dd-b27d-b840b639cb7b)


### 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/52c99a1e-5dc4-4bba-b6c3-e3f4cd49880e)

### 3.Violin Plot

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/a14a9831-59e4-4ad0-8ef6-badac2797813)

### 4.Density Plot

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/f7634781-9ca4-4228-8521-20eaa590c426)

### 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/Vanitha-SM/EXNO-6-DS/assets/119557985/32d6cc60-28b4-4839-88f6-19bb1b2d629c)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

