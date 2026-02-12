# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.

2.Upload and read the dataset

3.Check for any null values using the isnull() function.

4.Form sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

5.Find the accuracy of the model and predict the required values by importing the required module from sklearn
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: RAAGAVI R M
RegisterNumber: 212224220074

import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()

data.info()

data.isnull().sum()

data['left'].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data.head()

x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()

y=data['left']

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_predict)
accuracy

dt.predict([[0.5,0.8,9,206,6,0,1,2]]) 
*/
```

## Output:

### DATA HEAD:
<img width="1363" height="227" alt="image" src="https://github.com/user-attachments/assets/874a4bd1-1436-4151-ba9c-a2aedfe322e2" />

### DATA SET INFO:
<img width="2230" height="590" alt="image" src="https://github.com/user-attachments/assets/336975bf-c9c6-4206-b804-ac24683a856a" />

### NULL SET:
<img width="2230" height="406" alt="image" src="https://github.com/user-attachments/assets/1debad86-ceb2-498f-95b4-e83cb51568da" />

### VALUES COUNT:
<img width="2230" height="178" alt="image" src="https://github.com/user-attachments/assets/d4432517-8c52-423a-85e5-273e0dc91bdb" />

### DATASET TRANSFORMED HEAD:
<img width="2230" height="410" alt="image" src="https://github.com/user-attachments/assets/844949fe-6b40-4f42-ad0e-2453a9340bca" />

### X.HEAD:
<img width="2230" height="354" alt="image" src="https://github.com/user-attachments/assets/f7ba4b7c-4852-4b9a-8ba5-f3201f4b7b72" />

### ACCURACY:
<img width="2230" height="86" alt="image" src="https://github.com/user-attachments/assets/b039a871-e6ee-4eb5-990b-d65b04b2ba53" />

### DATA PREDICTION:
<img width="651" height="482" alt="image" src="https://github.com/user-attachments/assets/2fc393b1-4ded-4c1f-8a36-ece1bc55bfba" />

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
