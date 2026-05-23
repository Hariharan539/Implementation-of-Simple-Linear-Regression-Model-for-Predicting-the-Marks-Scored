# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary libraries
2. Store the independent variable (hours studied) in array x and the dependent variable (marks obtained) in array y.write
3. Reshape the input array to required format.
4. Create and train the Linear Regression model using least squares.
5. Predict output values using the trained model.
6. Plot actual data points and the regression line.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Hariharan V
RegisterNumber:  212224220032
*/
import numpy as np
from sklearn.linear_model import LinearRegression
import matplotlib.pyplot as plt

x=np.array([1,2,2.5,3,4,5,6]).reshape(-1,1)
y=np.array([12,34,51,66,79,86,97])

model=LinearRegression()

model.fit(x,y)

y_pred=model.predict(x)

print("Predicted values:",y_pred)
print("Actual values:",y)

plt.scatter(x,y, color='green', label='Actual mark')
plt.plot(x,y_pred, color='red', label='Regression line')
plt.title("Hours vs Marks")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Obtained")
plt.legend()
plt.show()
```

## Output:
<img width="934" height="706" alt="image" src="https://github.com/user-attachments/assets/f73b9572-8c5a-4af7-9501-5629a23c55f3" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
