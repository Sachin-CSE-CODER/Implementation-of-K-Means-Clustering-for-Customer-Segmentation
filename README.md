# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplot libraries.

2.import Kmeans algorithm to solve customer segmentation.

3.Using the for loop cluster the given data

4.Predict the output and plot data graphs.

5.Display the outputs

## Program:

Program to implement the K Means Clustering for Customer Segmentation.

Developed by: SACHIN S

RegisterNumber: 212224040283  
```python
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers.csv")
data
data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:, 3:])

y_pred = km.predict(data.iloc[:, 3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"] == 0]
df1 = data[data["cluster"] == 1]
df2 = data[data["cluster"] == 2]
df3 = data[data["cluster"] == 3]
df4 = data[data["cluster"] == 4]
plt.scatter(df0["Annual Income (k$)"], df0["Spending Score (1-100)"], c = "red", label = "cluster0")
plt.scatter(df1["Annual Income (k$)"], df1["Spending Score (1-100)"], c = "black", label = "cluster1")
plt.scatter(df2["Annual Income (k$)"], df2["Spending Score (1-100)"], c = "blue", label = "cluster2")
plt.scatter(df3["Annual Income (k$)"], df3["Spending Score (1-100)"], c = "green", label = "cluster3")
plt.scatter(df4["Annual Income (k$)"], df4["Spending Score (1-100)"], c = "magenta", label = "cluster4")
plt.legend()
plt.title("Customer Segments")
```

## Output:
![{75875D7C-57F1-48B3-850E-7233626FE559}](https://github.com/user-attachments/assets/9fac72c9-6631-4279-98a7-aa1eb0b12790)

![{31617A02-1E45-48C2-A0E5-4FF7D80ECF8A}](https://github.com/user-attachments/assets/9e9094b0-60f5-4b2a-b366-532891e3ec5f)

![{9AF32C9F-6B20-4341-A6FA-DE23BC5A6F69}](https://github.com/user-attachments/assets/0e3da521-ed85-4a53-af11-56d21dd4d3e4)

![{23DE1924-AD9E-43BF-A631-93799D702E1C}](https://github.com/user-attachments/assets/926e2af6-bb63-4aad-92fa-69d2fabfbfa0)

![{0FC9F28C-B92F-4E04-8BB2-02F8F00E13F6}](https://github.com/user-attachments/assets/b4c6edbc-c040-480d-804e-fd22cfc0540a)

![{B4D2192D-FE33-4121-86BB-5E6A191AACBD}](https://github.com/user-attachments/assets/d86df8f3-8c82-4e39-b39a-831a4068350e)

![{D1189DF3-7A26-4F1C-BD68-EE6EC4EEA8E2}](https://github.com/user-attachments/assets/e56337de-9f45-46fa-b2c6-8f9ec07e8104)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
