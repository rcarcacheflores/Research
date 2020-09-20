None
# Post 2: Basics with Python

Much like the previous post, I will keep things very simple in this first
tutorial using Python. To be honest, this is also a tutorial for me since it's
my first time using JupyterLab and GitHub together.

For those who are new to Python (like me), be sure to visit:
<a> href="https://jupyterlab.readthedocs.io/en/stable/" >Overview of
JupyterLab</a>.

Additionally, this is a good tutorial on using Markdown with Jupyter Noteboks:
<a> href="https://www.datacamp.com/community/tutorials/markdown-in-jupyter-
notebook" >Markdown tutorial</a>

## Part 1: Basic Calculations
In this section we will look use Python as a simple calculator. I have found
JupyterLab much more friendly to use and its flow reminds me a bit of RStudio.
We will also introduce a few basic built-in functions:

```{.python .input  n=26}
#first we will perform basic math
2+2
```

```{.json .output n=26}
[
 {
  "data": {
   "text/plain": "4"
  },
  "execution_count": 26,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=27}
6-1
```

```{.json .output n=27}
[
 {
  "data": {
   "text/plain": "5"
  },
  "execution_count": 27,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=28}
4*8
```

```{.json .output n=28}
[
 {
  "data": {
   "text/plain": "32"
  },
  "execution_count": 28,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=29}
#Next we will use some built-in functions Python has
#for example, pow() allows us to perform (81/9)^2 
pow((81/9),2)+20
```

```{.json .output n=29}
[
 {
  "data": {
   "text/plain": "101.0"
  },
  "execution_count": 29,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=30}
#for the square root of 64 we first import the math module and then call the function:
import math
math.sqrt(64)
#note that in Python 3 the syntax is module.function(argument)
```

```{.json .output n=30}
[
 {
  "data": {
   "text/plain": "8.0"
  },
  "execution_count": 30,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=31}
#suppose we wanted to change the base to find log(36), i.e. base 10
math.log(36,10)
```

```{.json .output n=31}
[
 {
  "data": {
   "text/plain": "1.556302500767287"
  },
  "execution_count": 31,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=32}
#for ln(36) we do:
math.log(36)
```

```{.json .output n=32}
[
 {
  "data": {
   "text/plain": "3.58351893845611"
  },
  "execution_count": 32,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

## Part 2: Working with Vectors

In this section we will use Python to create and manipulate vectors, using
different functions. The basis for any array manipulation is NumPy. For a much
more thorough tutorial on arrays and using NumPy please consult:<a>
href="https://jakevdp.github.io/PythonDataScienceHandbook/02.00-introduction-to-
numpy.html" > Introduction to NumPy </a>

```{.python .input  n=33}
#suppose we wanted to create a vector called x to contain the numbers 45. 31, 60, 80, 32
#first we have to import numpy:
import numpy as np
#now we create the vector using the array function:
x = np.array([45,31,60,80,32])
#when we call for x we can use the function print() to see the numbers x contains:
print(x)
```

```{.json .output n=33}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "[45 31 60 80 32]\n"
 }
]
```

```{.python .input  n=34}
#suppose we wanted to find the mean of x, we simply do:
x.mean()
```

```{.json .output n=34}
[
 {
  "data": {
   "text/plain": "49.6"
  },
  "execution_count": 34,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=35}
#for the standard deviation we perform:
x.std()
```

```{.json .output n=35}
[
 {
  "data": {
   "text/plain": "18.48891559827131"
  },
  "execution_count": 35,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=39}
#now suppose we want to create another vector called y:
y = np.array([28,90,45,60,70])
#we can add the elements of these vectors together by performing:
x+y 
```

```{.json .output n=39}
[
 {
  "data": {
   "text/plain": "array([ 73, 121, 105, 140, 102])"
  },
  "execution_count": 39,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=40}
#we can also multiply the elements of these vectors by doing:
x*y
```

```{.json .output n=40}
[
 {
  "data": {
   "text/plain": "array([1260, 2790, 2700, 4800, 2240])"
  },
  "execution_count": 40,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=41}
#finally, we can create the vector z which adds x and y and get its mean:
z=x+y
z.mean()
```

```{.json .output n=41}
[
 {
  "data": {
   "text/plain": "108.2"
  },
  "execution_count": 41,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

## Part 3: Working with Matrices

For this last section we will work with matrices using Python. The logic is
quite similar as to the previous section since we are also operating with arrays
using NumPy. The idea here is to perform basic linear algebra which can serve as
a foundation for deeper analysis:

```{.python .input  n=42}
#Suppose we want to create a 2x3 matrix called a with the same numbers from the previous post:
a = np.array([[1., 2., 3.], [4., 5., 6.]])
#here we can manually separate each row and we can see we have created a 2x3 matrix
a
```

```{.json .output n=42}
[
 {
  "data": {
   "text/plain": "array([[1., 2., 3.],\n       [4., 5., 6.]])"
  },
  "execution_count": 42,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=43}
#now we can create a 3x2 matrix and call it b:
b = np.array([[6., 23.], [-1, 7], [8, 9]])
b
```

```{.json .output n=43}
[
 {
  "data": {
   "text/plain": "array([[ 6., 23.],\n       [-1.,  7.],\n       [ 8.,  9.]])"
  },
  "execution_count": 43,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=44}
#to multiply axb we use de dot function and can shorten our code by doing:
a.dot(b)
```

```{.json .output n=44}
[
 {
  "data": {
   "text/plain": "array([[ 28.,  64.],\n       [ 67., 181.]])"
  },
  "execution_count": 44,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=45}
#to use more matrix functions we can create a 3x3 matrix and call it c
c= np.array([[1., 8., 10.], [2., 5., 11.],[9.,4.,12.]])
#to access these matrix functions we will use linalg which comes with mumpy:
from numpy.linalg import inv,det
```

```{.python .input  n=46}
#to find the inverse of c we use inv()
inv(c)
```

```{.json .output n=46}
[
 {
  "data": {
   "text/plain": "array([[ 0.06504065, -0.22764228,  0.15447154],\n       [ 0.30487805, -0.31707317,  0.03658537],\n       [-0.1504065 ,  0.27642276, -0.04471545]])"
  },
  "execution_count": 46,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=47}
#to find the determonant of c we use det()
det(c)
```

```{.json .output n=47}
[
 {
  "data": {
   "text/plain": "246.00000000000014"
  },
  "execution_count": 47,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

## Conclusions

I hope this simple tutorial was useful if you are unfamiliar with Python. There
are subtle differences with how R and Python read the matrix imputs but it is
still fairly similar. Thank you for coming along!
