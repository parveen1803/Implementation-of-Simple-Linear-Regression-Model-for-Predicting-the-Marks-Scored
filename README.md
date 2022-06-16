# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to implement the simple linear regression model for predicting the marks scored.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the standard Libraries.
2. Set variables for assigning dataset values.
3. Import linear regression from sklearn.
4. Assign the points for representing in the graph.
5. Predict the regression for marks by using the representation of the graph.
6. Compare the graphs and hence we obtained the linear regression for the given datas.
 

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Parveen Fathima.M
RegisterNumber:212219040103  
*/
import pandas  as pd
import matplotlib.pyplot as plt
dataset=pd.read_csv('/content/student_scores - student_scores.csv')
dataset.head()
X=dataset.iloc[:,:-1].values
Y=dataset.iloc[:,1].values
print(X)
print(Y)
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(X,Y,test_size=1/3,random_state=0)
from sklearn.linear_model import LinearRegression
regressor=LinearRegression()
regressor.fit(X_train,Y_train)
Y_pred=regressor.predict(X_test)
plt.scatter(X_train,Y_train,color='purple')
plt.plot(X_train,regressor.predict(X_train),color='green')
plt.title("hours vs scores(training set)")
plt.xlabel("hours")
plt.ylabel("scores")
plt.show()
Y_pred=regressor.predict(X_test)
plt.scatter(X_test,Y_test,color='brown')
plt.plot(X_train,regressor.predict(X_train),color='blue')
plt.title("hours vs scores(test set)")
plt.xlabel("hours")
plt.ylabel("scores")
plt.show()
```

## Output:
![Screenshot (3)](https://user-images.githubusercontent.com/87666371/173984353-87eb7615-c6f6-4c0c-8316-84120ce48dfa.png)

![Screenshot (5)](https://user-images.githubusercontent.com/87666371/173984500-4b522b0e-eab8-4f8a-9d15-ef212b8a6d2b.png)




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
