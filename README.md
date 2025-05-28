# EX-1 : IMPLEMENTATION OF UNIVARIANT LINEAR REGRESSION TO FIT A STRAIGHT LINE USING LEAST SQUARES
### Name : R.Jayasree
### R.No : 212223040074

## AIM:


To implement univariate Linear Regression to fit a straight line using least squares.




## EQUIPMENTS REQUIRED:


1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook




## ALGORITHM:


1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
   
   <img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
   
4. Compute the y -intercept of the line by using the formula:
   
   <img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
   
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.



## PROGRAM:








```
import numpy as np
import matplotlib.pyplot as plt
#preprocessing input data
x=np.array(eval(input()))
y=np.array(eval(input()))
#mean
x_mean=np.mean(x)
y_mean=np.mean(y)
num=0 #for slope
denom=0 #for slope
#to find sum of (x-x') % (y-y') & (x-x')(y-y')
for i in range(len(x)):
  num+=(x[i]-x_mean)*(y[i]-y_mean)
  denom+=(x[i]-x_mean)**2
#calculate slope
m=num/denom
#calculate intercept
b=y_mean-m*x_mean
print("Slope :",m);
print("Y-intercept :",b);
#line equation
y_predicted=m*x+b
print("y=",y_predicted);
#to plot graph
plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()

```






## OUTPUT:



   ![Screenshot 2025-02-24 162755](https://github.com/user-attachments/assets/0bcd19b7-e55d-4046-a63c-a2ae420ee592)







## RESULT:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming is executed successfully.
