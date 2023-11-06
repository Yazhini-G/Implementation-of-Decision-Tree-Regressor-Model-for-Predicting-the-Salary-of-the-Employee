# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2.

## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Yazhini G
RegisterNumber:  212222220060

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:

## Data.Head():
![279486017-17219e1b-9545-45e2-bb45-dd459016cbf9](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/baf96a7b-5e70-46df-b9ca-366997863921)

## Data.info():
![279486035-6c499887-944a-476d-b365-f406cc541e6f](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/799a243c-55a7-4097-96dd-d3352c2d2054)

## isnull() and sum():
![279486050-e97ab81f-f8b9-4813-83de-327da3214afe](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/de72594f-5ac8-4c1d-bfb2-f5d27b0b614b)

## Data.Head() for salary:
![279486068-ffc344dd-39b6-4370-9282-468f4642736c](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/038b359e-28bb-4e5a-bc1a-c0a38a64c077)

## MSE Value:
![279486086-d063c559-f82f-4a52-b1fd-74c153c7d36e](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/2c273ac1-8188-4924-b209-ad755f9e0da5)

## r2 Value:
![279486100-2956ebf4-c1b2-4a45-9365-21f67717ebc4](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/5ea2ad9a-8d8a-489a-b745-32df6e999dcf)

## Data Prediction:
![279486119-516cbe0b-9937-4dd6-a5a8-1ac01a6673eb](https://github.com/Yazhini-G/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120244201/08b1abba-7d24-4a5c-93c0-de7cc6c43fef)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
