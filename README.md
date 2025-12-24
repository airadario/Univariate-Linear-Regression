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

Program to develop to implement univariate Linear Regression to fit a straight line using least squares.

Developed by : A.Aira Dario
Register no : 25016155
```
import numpy as np
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)
print(f"Slope : {m}\nIntercept : {b}")
Y_Pred=(m*X)+b
print(f"Predicted values are : \n{Y_Pred}")
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()




```
## Output
<img width="990" height="802" alt="Screenshot 2025-12-24 211544" src="https://github.com/user-attachments/assets/d47e27f0-5b46-4d92-a485-9d3c3b5d26a0" />
<img width="819" height="542" alt="Screenshot 2025-12-24 211621" src="https://github.com/user-attachments/assets/f8a04923-955a-4b79-98b9-0fb03dfcca63" />
<img width="1068" height="332" alt="Screenshot 2025-12-24 211652" src="https://github.com/user-attachments/assets/3b2cc6ec-8e91-4d90-b951-656a0737d2b5" />
<img width="913" height="671" alt="Screenshot 2025-12-24 211701" src="https://github.com/user-attachments/assets/1ed6730a-fbd0-4220-87de-662e6150d4f7" />






## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
