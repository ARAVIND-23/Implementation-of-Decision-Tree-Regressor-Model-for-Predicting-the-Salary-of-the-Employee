# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null values using .isnull()
function.
3. Import LabelEncoder and encode the dataset.
4. Import DecisionTreeRegressor from sklearn and apply the model on
the dataset
5. Predict the values of arrays.
6. Import metrics from sklearn and calculate the MSE and R2 of the
model on the dataset.
7. Predict the values of array.
8. Apply to new unknown values.


## Program & Output:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: ARAVIND G
RegisterNumber: 212223240011
/*

import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()
```
![Screenshot 2024-10-16 145037](https://github.com/user-attachments/assets/28caa432-0e4d-4fe0-bc4e-6c83bb3b9219)
```
data.info()
```
![Screenshot 2024-10-16 145239](https://github.com/user-attachments/assets/d172288e-2e70-4e9e-b6a2-ea41c9f3505b)
```
data.isnull().sum()
```
![Screenshot 2024-10-16 145325](https://github.com/user-attachments/assets/a8bc0bba-6e4d-40e4-9abe-d683bf361bc6)
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
![Screenshot 2024-10-16 145416](https://github.com/user-attachments/assets/f1b5afe5-b4b9-4a41-891d-ae690605cd1c)
```
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y, test_size=0
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
```
![Screenshot 2024-10-16 145517](https://github.com/user-attachments/assets/87bf8739-655e-4228-84c2-34613f04eb15)
```
r2=metrics.r2_score(y_test,y_pred)
r2
```
![Screenshot 2024-10-16 145556](https://github.com/user-attachments/assets/d3816757-af0e-4985-967f-92c78dd56513)
```
dt.predict([[5,6]])
```
![Screenshot 2024-10-16 145714](https://github.com/user-attachments/assets/44e54d9f-3f68-4272-8d8f-641b0031366d)
```


```




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
