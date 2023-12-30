# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built in function for calculation.
2. Import the sys function.Get input from the user for the matrix i and j using for loop.
3. check whether the matrix of element is divisible by zero.If divisible by zero then print zero is
   detected.And further find the ratio of the matix.
4.  End the program


## Program:
```python
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Swaminathan V
RegisterNumber: 23000747


import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in range(n):
     for j in range(n+1):
         a[i][j] = float(input())
for i in range(n):
     if a[i][i] == 0.0:
         sys.exit('Divide by zero detected!')

     for j in range(i+1,n):
         ratio = a[j][i]/a[i][i]

         for k in range(n+1):
             a[j][k] = a[j][k] - ratio* a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]

    for j in range(i+1,n):
        x[i] = x[i] - a[i][j]*x[j]

    x[i] = x[i]/a[i][i]
for i in range(n):
     print('X%d = %0.2f' %(i,x[i]), end = ' ')
*/
```

## Output:
![gaussian elimination wpp](https://github.com/SwaminathanV23000747/Gaussian/assets/148931113/df70379e-5fcd-4c74-845f-36f027190769)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

