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
 <img width="357" height="184" alt="image" src="https://github.com/user-attachments/assets/e176da59-11b3-42e8-855d-3f6d4161ef6f" />

4.	Compute the y -intercept of the line by using the formula:
<img width="236" height="62" alt="image" src="https://github.com/user-attachments/assets/2d745847-4a29-45de-b860-91573aeb24c2" />
 
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output

<img width="828" height="626" alt="image" src="https://github.com/user-attachments/assets/a28a021f-54d1-48b0-bb11-72d6b9bc9f97" />
<img width="878" height="713" alt="image" src="https://github.com/user-attachments/assets/e89c4860-addd-49de-a4ae-21b935b0a53c" />



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
