# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: Mahasri P
#register number: 212223100029

import numpy as np 
import matplotlib.pyplot as plt

x_input = eval(input())
y_input = eval(input())


plt.scatter(x, y)
plt.xlabel('x')
plt.ylabel('y')
plt.title('Original Data')
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)
numerator = 0
denominator = 0
for i in range(len(x)):
    numerator += (x[i] - xmean) * (y[i] - ymean)
    denominator += (x[i] - xmean) ** 2
m = numerator / denominator
b = ymean - m * xmean
print("Slope (m):", m)
print("Y-intercept (b):", b)

ypred = m * x + b
print("Predicted y values:", ypred)

plt.scatter(x, y, color='red', label='Original Data')
plt.plot(x, ypred, color='blue', label='Regression Line')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Linear Regression')
plt.legend()
plt.show()







```
## Output

![image](https://github.com/mahasri06/Univariate-Linear-Regression/assets/139841897/56cfe586-c96f-46d6-9f98-8626a5fc1c73)


![Screenshot 2024-04-28 132824](https://github.com/mahasri06/Univariate-Linear-Regression/assets/139841897/1bfca3ae-0dfc-4b8b-acb4-87a26ea036c1)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
