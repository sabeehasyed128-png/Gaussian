# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy
2. Impport sys
3. Solve using for loop
4. Print th output

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: SABEEHA PARVEEN K
RegisterNumber: 25016301
*/
import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j] == 0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio*a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i] = x[i]-a[i][j]*x[j]
    x[i] = x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]), end = ' ')
```

## Output:
<img width="968" height="862" alt="EXP 6 Q" src="https://github.com/user-attachments/assets/fde7d1da-8477-404b-914d-79000666814e" />

<img width="968" height="862" alt="EXP 6 A" src="https://github.com/user-attachments/assets/71c8e726-2539-457a-8132-f0d9e6c98bc9" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

