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

# Name : C R SUDEEP RAJ
# Register No: 212224040333

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

df=pd.read_csv("titanic_dataset.csv")

df.head()

<img width="800" height="500" alt="Screenshot 2025-10-27 105329" src="https://github.com/user-attachments/assets/d8f4915b-c008-4001-982e-dbc5637993e8" />


### 1.Line Plot

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

plt.title('Line Plot')

<img width="534" height="435" alt="download (10)" src="https://github.com/user-attachments/assets/249798ca-86cb-4fdf-a861-da2e4e0decfb" />

### 2.Multi Line Plot

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3)

plt.title('Multi Line Plot')

<img width="534" height="435" alt="download (1)" src="https://github.com/user-attachments/assets/e449cc3d-ed31-4208-bd06-18bdf6ae3031" />


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')

plt.title("Fare Of Passenger By Embarked Town")

<img width="686" height="470" alt="download (2)" src="https://github.com/user-attachments/assets/4cef31df-14cb-4ca5-b94b-497f5b5bb681" />

### 2.Scatter Plot

sns.scatterplot(x="Age", y="Fare", data=df)

plt.title('Scatterplot of Age vs Fare')

plt.show()

<img width="571" height="455" alt="download (3)" src="https://github.com/user-attachments/assets/68d4e22b-3e59-4606-9fc9-826473214187" />

### 3.Bubble Chart

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))

plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')

plt.show()

<img width="571" height="455" alt="download (4)" src="https://github.com/user-attachments/assets/d12b6aa1-cc98-4279-8bae-7c4539233c0e" />

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

<img width="571" height="432" alt="download (5)" src="https://github.com/user-attachments/assets/80cefd7b-f85c-480c-b202-583ba944c45d" />

### 2.Box Plot

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')

plt.title("Age By Passenger Class")

<img width="562" height="455" alt="download (6)" src="https://github.com/user-attachments/assets/a6e199cd-0b63-4b51-b127-fa33dea32e5f" />

### 3.Violin Plot

sns.violinplot(x="Pclass", y="Fare", data=df)

plt.title('Violin Plot of Fare by Passenger Class')

plt.show()

<img width="571" height="455" alt="download (7)" src="https://github.com/user-attachments/assets/4ca17139-d860-4861-80c6-994cd168af08" />

### 4.Density Plot

sns.kdeplot(data=df['Age'], shade=True)

plt.title('Density Plot of Passenger Ages')

plt.show()

<img width="584" height="455" alt="download (8)" src="https://github.com/user-attachments/assets/2ccf2bf9-6856-47d3-9ab8-b83e8235259e" />

### 5.Heatmap

numeric_df = df.select_dtypes(include=['float64', 'int64'])

corr_matrix = numeric_df.corr()

sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')

plt.title('Heatmap of Titanic Dataset')

plt.show()

<img width="596" height="505" alt="download (9)" src="https://github.com/user-attachments/assets/7c55ec84-6dff-42ab-a524-0cd059853d49" />

# Result:
  
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
