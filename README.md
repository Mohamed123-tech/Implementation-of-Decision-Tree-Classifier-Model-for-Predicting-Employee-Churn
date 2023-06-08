# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print dataset info

2.check for null value

3.Map numerical values for salary feature

4.Assign x and y values

5.Split the dataset into train and test sets

6.Import decisiontree classifier and fit it in the dataset

7.Find accuracy and predict values

## Program:
```
/*
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: 212220040081
RegisterNumber:logeshwaran s

##program##
import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=10)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)

accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/ 
*/
```

## Output:
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/67da969d-f754-4826-b5d3-0fffd7ef29d0)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/7293cb3d-b719-48d8-925e-05f775c587ce)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/f21f5a7b-7afb-4619-bb59-f93c2b0ef683)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/d815db0a-5218-4831-b1c1-0a2cd4d8478d)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/5c49cf8d-23de-4c46-85fd-22c1308c3bde)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/53a6fa75-128e-4a54-be9d-b4e66ccd1f5a)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/3a3505ed-c7a7-4691-bcac-0cf7feb9e2c9)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/fdf53597-7be5-473c-95aa-b852fa965c86)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/84709944/2a846a2d-0104-4c62-acbc-6e10a48b36a5)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
