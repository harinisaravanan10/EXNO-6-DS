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
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1225" height="202" alt="image" src="https://github.com/user-attachments/assets/41ff1a75-617a-4614-b515-b87e3b48adfd" />

1.LINE PLOT

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="616" height="451" alt="image" src="https://github.com/user-attachments/assets/40dbb437-37ca-4316-b54d-2c730c66fcd5" />

2.MULTI LINE PLOT

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

<img width="622" height="462" alt="image" src="https://github.com/user-attachments/assets/3b510493-1c71-4f2e-a20c-2e7fdb02c53b" />

## TO VISUALIZE RELATIONSHIPS

1.BAR CHART

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="787" height="517" alt="image" src="https://github.com/user-attachments/assets/85381028-e4be-4010-9dbb-4b775cf625b8" />


2.SCATTER PLOT

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="704" height="477" alt="image" src="https://github.com/user-attachments/assets/79d6364e-701b-49c6-91af-ccef1b56646a" />


3.BUBBLE CHART

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="721" height="463" alt="image" src="https://github.com/user-attachments/assets/32c742e1-bdd5-4522-ac7f-691a82d861a9" />

## TO CAPTURE DISTRIBUTIONS

1.HISTOGRAM

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="719" height="465" alt="image" src="https://github.com/user-attachments/assets/c81eaad7-f27d-44cc-881a-3d6d66d0c40a" />


2.BOX PLOT

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="699" height="501" alt="image" src="https://github.com/user-attachments/assets/a5a591c7-4aad-4fbc-980d-3e1aedb5228d" />


3.VIOLIN PLOT

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="749" height="469" alt="image" src="https://github.com/user-attachments/assets/986e45da-e0ca-4e68-af1c-04dbb317ebde" />


4.DENSITY PLOT

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="747" height="470" alt="image" src="https://github.com/user-attachments/assets/572e0465-9097-4148-940f-8e3481c26243" />


5.HEATMAP

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="695" height="511" alt="image" src="https://github.com/user-attachments/assets/0bf0f0cd-b626-446a-a021-ed4149622d05" />

## Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
