# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:

/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:piyush kumar 
RegisterNumber:212223220075  
*/
~~~
import pandas as pd
data=pd.read_csv("C:/Users/admin/OneDrive/Desktop/Employee (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data.head()
x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=10)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_predict)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:
![Screenshot 2024-04-02 093404](https://github.com/H515piyush/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147472999/d5e0be60-754f-428a-9a98-4cb515d141e9)

![Screenshot 2024-04-02 093422](https://github.com/H515piyush/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147472999/b7a98297-b296-41de-a863-0c3b31dcf85d)

![Screenshot 2024-04-02 093430](https://github.com/H515piyush/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147472999/6c76eaed-7a14-4b25-80d3-65f302832a04)
![Screenshot 2024-04-02 093444](https://github.com/H515piyush/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147472999/04a7039f-ed7a-4364-9f56-e0bd021b954a)

![Screenshot 2024-04-02 093455](https://github.com/H515piyush/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147472999/edf1d063-78ea-421d-825a-856e9392c166)

![Screenshot 2024-04-02 093503](https://github.com/H515piyush/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/147472999/deb48328-17d7-46d8-a29a-8d96ce5471cd)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
