# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import the numpy module to use the build - in functions for calculation
2. prepare the list from each equation and assign the array
3. using the equation , we get two results of the given matrix
4. End The Program
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
*/
import numpy as np
import sys
n = int(input())
a = np.zeros((n , n+1))
x = np.zeros(n)
for i in range (n):
    for j in range(n+1):
        a[i][j] = float(input())
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('Divide by zero detected!')
        
    for j in range (i+1 , n):
        ratio = a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2, -1 ,-1):
    x[i] = a[i][n]
    
    for j in range(i+1,n):
       x[i] = x[i] - a[i][j]*x[j]
       
    x[i] = x[i]/a[i][i]
    
for i in range (n):
    print('X%d = %0.2f' %(i, x[i]), end = ' ')
```

## Output:
![gaussian elimination]()
![image](https://github.com/Deepikasuresh05/Gaussian/assets/148514509/c92086a1-e739-47a1-ab76-a1dac63f2b0b)
![image](https://github.com/Deepikasuresh05/Gaussian/assets/148514509/2f30661d-d198-4ce6-85d0-672e17e5add5)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

