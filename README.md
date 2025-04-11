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

    import pandas as pd
    import seaborn as sns
    import matplotlib.pyplot as plt
    df=pd.read_csv("titanic_dataset.csv")
    df.head()
![image](https://github.com/user-attachments/assets/840888bd-44e9-4d1c-8151-8f8a407fd733)

1.Line Plot

    x=[1,2,3,4,5]
    y=[3,6,2,7,1]
    sns.lineplot(x=x,y=y)
    plt.title('Line Plot')
![image](https://github.com/user-attachments/assets/514d4586-9258-4c3a-ac02-1ff71dae71bd)

2.Multi Line Plot
  
    x=[1,2,3,4,5]
    y1=[3,5,2,6,1]
    y2=[1,6,4,3,8]
    y3=[5,2,7,1,4]
    sns.lineplot(x=x,y=y1)
    sns.lineplot(x=x,y=y2)
    sns.lineplot(x=x,y=y3)
    plt.title('Multi Line Plot')
![image](https://github.com/user-attachments/assets/9dacbfa5-0d1f-4ec0-80e3-10c183ead4dc)

TO VISUALIZE RELATIONSHIPS
  1.Bar Chart
  
    plt.figure(figsize=(8,5))
    sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
    plt.title("Fare Of Passenger By Embarked Town")
![image](https://github.com/user-attachments/assets/d14dd144-75b7-4ab3-8223-ae2c14e5f9e7)

2.Scatter Plot

    sns.scatterplot(x="Age", y="Fare", data=df)
    plt.title('Scatterplot of Age vs Fare')
    plt.show()
![image](https://github.com/user-attachments/assets/50d17c75-9331-420d-876b-2d3053978ef5)

3.Bubble Chart

    sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
    plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
    plt.show()
![image](https://github.com/user-attachments/assets/6082df3c-fa49-4965-bc21-491a77debec0)

TO CAPTURE DISTRIBUTIONS
1.Histogram

    sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
![image](https://github.com/user-attachments/assets/08ba6960-3f47-4356-8804-8419542d5076)

2.Box Plot

    sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
    plt.title("Age By Passenger Class")
![image](https://github.com/user-attachments/assets/6f54b401-3588-444f-8d11-315103b825c1)

3.Violin Plot

    sns.violinplot(x="Pclass", y="Fare", data=df)
    plt.title('Violin Plot of Fare by Passenger Class')
    plt.show()
![image](https://github.com/user-attachments/assets/efd0bee1-93ae-4f4f-888d-719bb83b3d11)


4.Density Plot

    sns.kdeplot(data=df['Age'], shade=True)
    plt.title('Density Plot of Passenger Ages')
    plt.show()
![image](https://github.com/user-attachments/assets/a4535061-bc65-4958-a362-360729051841)

5.Heatmap

    numeric_df = df.select_dtypes(include=['float64', 'int64'])
    corr_matrix = numeric_df.corr()
    sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
    plt.title('Heatmap of Titanic Dataset')
    plt.show()
![image](https://github.com/user-attachments/assets/b2c8b7f7-b572-46fa-be06-53466fc939e9)
# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
