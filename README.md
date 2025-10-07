# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3. Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Annie Jenifsika A
RegisterNumber:  212224230019



import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No_of_Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segment")

*/
```

## Output:
<img width="921" height="272" alt="image" src="https://github.com/user-attachments/assets/f45fc44f-f72a-42d9-8c46-07d4ffb0c417" />
<img width="390" height="294" alt="image" src="https://github.com/user-attachments/assets/88dfcefe-e781-45ea-8f00-095be6065b20" />
<img width="615" height="260" alt="image" src="https://github.com/user-attachments/assets/e2031291-7ace-4a56-ad0d-cba393462cb8" />
<img width="962" height="638" alt="image" src="https://github.com/user-attachments/assets/4ea7a84e-77ec-42cf-a8a4-a4ecbe1d3cd2" />
<img width="387" height="116" alt="image" src="https://github.com/user-attachments/assets/cd9d8bd7-827a-4b3f-9958-ad8820250f2e" />
<img width="910" height="241" alt="image" src="https://github.com/user-attachments/assets/6802ffc0-3262-4773-ace4-06801ca3fa89" />
<img width="804" height="596" alt="image" src="https://github.com/user-attachments/assets/68977e39-f8c6-4fc2-9d15-db3675e72770" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
