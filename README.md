# Implementation-of-Logistic-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the the Logistic Regression Using Gradient Descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the the Logistic Regression Using Gradient Descent.
Developed by: Vimalesh kanna MK
RegisterNumber:  212225230303

/*
Program to implement the the Logistic Regression Using Gradient Descent.
Developed by: THARUN DP
RegisterNumber:25018717
import numpy as np
import pandas as pd
data = pd.read_csv("/mnt/data/Placement_Data.csv")

data['status'] = data['status'].map({'Placed': 1, 'Not Placed': 0})

X = data[['ssc_p', 'hsc_p', 'degree_p', 'etest_p', 'mba_p']].values
y = data['status'].values

X = np.c_[np.ones(X.shape[0]), X]

theta = np.zeros(X.shape[1])

def sigmoid(z):
    return 1 / (1 + np.exp(-z))

def compute_cost(X, y, theta):
    m = len(y)
    h = sigmoid(X @ theta)
    cost = (-1/m) * np.sum(y*np.log(h) + (1-y)*np.log(1-h))
    return cost

def gradient_descent(X, y, theta, alpha, iterations):
    m = len(y)
    for i in range(iterations):
        h = sigmoid(X @ theta)
        gradient = (1/m) * (X.T @ (h - y))
        theta -= alpha * gradient
        
        if i % 100 == 0:
            print(f"Iteration {i}, Cost: {compute_cost(X, y, theta)}")
    
    return theta

alpha = 0.001
iterations = 1000

theta = gradient_descent(X, y, theta, alpha, iterations)

print("Final Parameters:", theta)
 
*/
*/
```

## Output:
<img width="1321" height="242" alt="image" src="https://github.com/user-attachments/assets/85a37c08-b7f4-41ef-8969-598771f17424" />



## Result:
Thus the program to implement the the Logistic Regression Using Gradient Descent is written and verified using python programming.

