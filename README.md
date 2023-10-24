# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2.Import Decision tree classifier
3.Fit the data in the model
4.Find the accuracy score


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SANDHIYA R 
RegisterNumber: 212222230129  
*/
```
```
import pandas as pd
data=pd.read_csv("salary.csv")
data.head()
data.info()
data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
data.info()
x=data[["Position","Level" ]]
x.head()
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=100)
x_train.shape
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
### df.head()
![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/91b9c4a1-fb7c-41a5-aa1e-5f35a14e4cf5)

### df.info()

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/8485e4e9-12d3-4ab8-8506-7e81301bbbb9)

### df.isnull.sum()

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/c9d7decf-4b46-4ba8-b66f-43c1a45dce8d)

### after lable encoding

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/4f3b818a-f717-4a9f-8a78-1f1978a7dc70)

### x_train.shape

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/e2a522c9-ce29-44e4-93f9-3e78cf025649)

### y_pred

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/4c6fa12e-6f09-4c96-81d6-507774f5d6f0)

### MSE

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/37997899-18a5-42f0-95ac-5f09ac36420a)

### R2

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/5131da2c-8d49-4599-8d40-0e645acf86c4)

### predicted value

![image](https://github.com/SandhiyaR1/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497571/8a2fae35-dee2-41e9-89fa-7262f9b31f6d)






## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
