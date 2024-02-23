# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import the standard Libraries.
2.  Set variables for assigning dataset values.
3.  Import linear regression from sklearn.
4.  Assign the points for representing in the graph.
5.  Predict the regression for the marks by using the representation of the graph.
6.  Hence we obtained the linear regression for the given dataset.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by:Shaik Shoaib Nawaz 
RegisterNumber: 212222240094 
*/
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
df=pd.read_csv('/content/ex1_os.csv')
df.head(10)
plt.scatter(df['x'],df['y'])
plt.xlabel('x')
plt.ylabel('y')
x=df.iloc[:,0:-1]
y=df.iloc[:,-1]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LinearRegression
lr=LinearRegression()
lr.fit(x_train,y_train)
x_train
y_train
lr.predict(x_test.iloc[0].values.reshape(1,1))
plt.scatter(df['x'],df['y'])
plt.xlabel('x')
plt.ylabel('y')
plt.plot(x_train,lr.predict(x_train),color='orange')
lr.coef_
lr.intercept_
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
### 1.) Dataset:

![Screenshot 2024-02-23 053956](https://github.com/shoaib3136/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/117919362/a16b8f1b-ef2e-4c85-8d8a-d089ae0b86e2)

### 2.) Graph of plotted data:

![Screenshot 2024-02-23 054041](https://github.com/shoaib3136/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/117919362/cb1ed93e-db66-41ad-826e-4c27af01de79)

### 3.) Performing Linear Regression:

![Screenshot 2024-02-23 054228](https://github.com/shoaib3136/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/117919362/dc82b3f8-58cd-46e1-82da-255fd2d03e24)

### 4.) Trained data:

![Screenshot 2024-02-23 054319](https://github.com/shoaib3136/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/117919362/e7d650b1-e8a9-4a6f-8a2a-0862e87fe743)

### 5.) Predicting the line of Regression:

![Screenshot 2024-02-23 054405](https://github.com/shoaib3136/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/117919362/716140d3-f7d4-44b1-9e54-7babdd3ef31f)

### 6.) Coefficient and Intercept values:

![Screenshot 2024-02-23 054444](https://github.com/shoaib3136/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/117919362/4224182d-10a0-4792-ba0e-5b4148c2c3ad)








## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
