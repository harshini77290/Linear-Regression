# Linear-Regression
import pandas as pd 
d=pd.read_csv('Salary_Data.csv')
print(d)
import numpy as np

d1=d.fillna(0)
y = d1['YearsExperience']
x=d1['Salary']
b1=10000
b0=10000
summation = 0  
n = len(y)
for i in range (0,n): 
  y_bar =(b1*y[i])+b0
  dif =(x[i])-(y_bar) 
  squared_difference = dif*dif 
  summation = summation + squared_difference  
MSE = summation/30  
print("The Mean Square Error is: " , MSE)
