None
# Post 2: Basics with Python

Much like the previous post, I will keep things very simple in this first tutorial using Python. To be honest, this is also a tutorial for me since it's my first time using JupyterLab and GitHub together. 

For those who are new to Python (like me), be sure to visit: 
<a> href="https://jupyterlab.readthedocs.io/en/stable/" >Overview of JupyterLab</a>. 

Additionally, this is a good tutorial on using Markdown with Jupyter Noteboks: 
<a> href="https://www.datacamp.com/community/tutorials/markdown-in-jupyter-notebook" >Markdown tutorial</a>

## Part 1: Basic Calculations
In this section we will look use Python as a simple calculator. I have found JupyterLab much more friendly to use and its flow reminds me a bit of RStudio. We will also introduce a few basic built-in functions:

```{.python .input  n=26}
#first we will perform basic math
2+2
```

<div class='outputs' n=26>

</div>

```{.python .input  n=27}
6-1
```

<div class='outputs' n=27>

</div>

```{.python .input  n=28}
4*8
```

<div class='outputs' n=28>

</div>

```{.python .input  n=29}
#Next we will use some built-in functions Python has
#for example, pow() allows us to perform (81/9)^2 
pow((81/9),2)+20
```

<div class='outputs' n=29>

</div>

```{.python .input  n=30}
#for the square root of 64 we first import the math module and then call the function:
import math
math.sqrt(64)
#note that in Python 3 the syntax is module.function(argument)
```

<div class='outputs' n=30>

</div>

```{.python .input  n=31}
#suppose we wanted to change the base to find log(36), i.e. base 10
math.log(36,10)
```

<div class='outputs' n=31>

</div>

```{.python .input  n=32}
#for ln(36) we do:
math.log(36)
```

<div class='outputs' n=32>

</div>

## Part 2: Working with Vectors 

In this section we will use Python to create and manipulate vectors, using different functions. The basis for any array manipulation is NumPy. For a much more thorough tutorial on arrays and using NumPy please consult:<a> href="https://jakevdp.github.io/PythonDataScienceHandbook/02.00-introduction-to-numpy.html" > Introduction to NumPy </a>


```{.python .input  n=33}
#suppose we wanted to create a vector called x to contain the numbers 45. 31, 60, 80, 32
#first we have to import numpy:
import numpy as np
#now we create the vector using the array function:
x = np.array([45,31,60,80,32])
#when we call for x we can use the function print() to see the numbers x contains:
print(x)
```

<div class='outputs' n=33>
[45 31 60 80 32]

</div>

```{.python .input  n=34}
#suppose we wanted to find the mean of x, we simply do:
x.mean()
```

<div class='outputs' n=34>

</div>

```{.python .input  n=35}
#for the standard deviation we perform:
x.std()
```

<div class='outputs' n=35>

</div>

```{.python .input  n=39}
#now suppose we want to create another vector called y:
y = np.array([28,90,45,60,70])
#we can add the elements of these vectors together by performing:
x+y 
```

<div class='outputs' n=39>

</div>

```{.python .input  n=40}
#we can also multiply the elements of these vectors by doing:
x*y
```

<div class='outputs' n=40>

</div>

```{.python .input  n=41}
#finally, we can create the vector z which adds x and y and get its mean:
z=x+y
z.mean()
```

<div class='outputs' n=41>

</div>

## Part 3: Working with Matrices

For this last section we will work with matrices using Python. The logic is quite similar as to the previous section since we are also operating with arrays using NumPy. The idea here is to perform basic linear algebra which can serve as a foundation for deeper analysis:

```{.python .input  n=42}
#Suppose we want to create a 2x3 matrix called a with the same numbers from the previous post:
a = np.array([[1., 2., 3.], [4., 5., 6.]])
#here we can manually separate each row and we can see we have created a 2x3 matrix
a
```

<div class='outputs' n=42>

</div>

```{.python .input  n=43}
#now we can create a 3x2 matrix and call it b:
b = np.array([[6., 23.], [-1, 7], [8, 9]])
b
```

<div class='outputs' n=43>

</div>

```{.python .input  n=44}
#to multiply axb we use de dot function and can shorten our code by doing:
a.dot(b)
```

<div class='outputs' n=44>

</div>

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

<div class='outputs' n=46>

</div>

```{.python .input  n=47}
#to find the determonant of c we use det()
det(c)
```

<div class='outputs' n=47>

</div>

## Conclusions

I hope this simple tutorial was useful if you are unfamiliar with Python. There are subtle differences with how R and Python read the matrix imputs but it is still fairly similar. Thank you for coming along!
