# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: AKASH CT
RegisterNumber: 24901150 
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
dt.predict([[5,6]])
```


## Output:
![image](https://github.com/user-attachments/assets/120eeeff-0691-472f-a981-0fdef94d443e)
![image](https://github.com/user-attachments/assets/961583ff-5022-41e4-bd78-c85c94659dfd)
![image](https://github.com/user-attachments/assets/45f76a52-7094-42a7-86fc-697a1b5509e7)
![image](https://github.com/user-attachments/assets/052bcf86-1039-4d8e-8805-06c064fbeb5e)
![image](https://github.com/user-attachments/assets/5a9eb3fa-a559-488a-bd3b-15fb60de11f8)





## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
