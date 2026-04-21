# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Input dataset (X, Y)
2.Reshape X to 2D
3.Create Linear Regression model
4.Train model using fit()
5.Obtain slope and intercept
6.Take new input
7.Predict output using model
8.Plot actual data and regression line
9.Display graph 

## Program:
```
Developed by: Sifiz A
RegisterNumber:  212225040414

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Sample data

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

# Create model
model = LinearRegression()

# Train model
model.fit(X, Y)

# Get slope and intercept
m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

# ---- Prediction ----
x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

# ---- Plot ----
Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:
<img width="1631" height="826" alt="Screenshot (403)" src="https://github.com/user-attachments/assets/6b34d67e-4d34-406d-8628-4eb7f930546c" />

<img width="1580" height="784" alt="Screenshot (404)" src="https://github.com/user-attachments/assets/a1cd55c4-4d2e-4973-9182-fcff75ff0c6c" />




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
