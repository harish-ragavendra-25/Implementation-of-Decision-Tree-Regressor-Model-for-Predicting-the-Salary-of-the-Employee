# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree inport DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: HARISH RAGAVENDRA S
RegisterNumber:  212222230045
*/
```
```
import pandas as pd
data=pd.read_csv("/content/Salary(1).csv")
print('data.head():')
data.head()
print('data.info():')
data.info()
print('isnull() and sum():')
data.isnull()
print('data.head() for salary:')
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
print('MSE value:')
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
print('r2 value:')
r2 = metrics.r2_score(y_test,y_pred)
r2
print('data prediction:')
dt.predict([[5,6]])
```

## Output:
![Screenshot 2023-11-11 170219](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/b76ed29c-0198-451b-9834-775b0e136c01)

![Screenshot 2023-11-11 170214](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/bdad626e-b236-4575-9613-a63fdd0f8be4)

![Screenshot 2023-11-11 170210](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/f7d1b826-10d0-4439-905c-c35004c7950e)

![Screenshot 2023-11-11 170206](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/91e4e187-44dd-4a86-bf1a-6f6872f99bf2)

![Screenshot 2023-11-11 170202](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/042dc4a6-77c0-42d1-8dd0-7e603f48c926)

![Screenshot 2023-11-11 170156](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/d0febd40-cb73-43bb-aa7a-e40022392651)

![Screenshot 2023-11-11 170150](https://github.com/harish-ragavendra-25/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/114852180/eea3ad61-31fe-42de-a0db-beba5b11af40)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
