# Practical_3
Practical_3

File: /home/ubuntu/practical3dsl.py Page 1 of 1
'''Experiment No. 3: Write a Python Program to compute following computation on matrices :
a)Addition of two matrices
b)Subtraction of two matrices
c)Multiplication of two matrices
d)Transpose of a matix
'''
import numpy
# initializing matrices
x = numpy.array([[1, 2], [4, 5]])
y = numpy.array([[7, 8], [9, 10]])
# using add() to add matrices
print("The element wise addition of matrix is : ")
print(numpy.add(x, y))
# using subtract() to subtract matrices
print("The element wise subtraction of matrix is : ")
print(numpy.subtract(x, y))
# using dot() to multiply matrices
print ("The product of matrices is : ")
print (numpy.dot(x,y))
# using "T" to transpose the matrix
print("The transpose of given matrix is : ")
print(x.T)
#############################################################################
Output : -
ubuntu@ubuntu-Vostro-460:~/DSL$ /bin/python3 /home/ubuntu/DSL/Practical3b.py
The element wise addition of matrix is :
[[ 8 10]
[13 15]]
The element wise subtraction of matrix is :
[[-6 -6]
[-5 -5]]
The product of matrices is :
[[25 28]
[73 82]]
The transpose of given matrix is :
[[1 4]
[2 5]]
