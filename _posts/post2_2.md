{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Post 2: Basics with Python\n",
    "\n",
    "Much like the previous post, I will keep things very simple in this first tutorial using Python. To be honest, this is also a tutorial for me since it's my first time using JupyterLab and GitHub together. \n",
    "\n",
    "For those who are new to Python (like me), be sure to visit: \n",
    "<a> href=\"https://jupyterlab.readthedocs.io/en/stable/\" >Overview of JupyterLab</a>. \n",
    "\n",
    "Additionally, this is a good tutorial on using Markdown with Jupyter Noteboks: \n",
    "<a> href=\"https://www.datacamp.com/community/tutorials/markdown-in-jupyter-notebook\" >Markdown tutorial</a>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Part 1: Basic Calculations\n",
    "In this section we will look use Python as a simple calculator. I have found JupyterLab much more friendly to use and its flow reminds me a bit of RStudio. We will also introduce a few basic built-in functions:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "4"
      ]
     },
     "execution_count": 26,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#first we will perform basic math\n",
    "2+2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "5"
      ]
     },
     "execution_count": 27,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "6-1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "32"
      ]
     },
     "execution_count": 28,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "4*8"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "101.0"
      ]
     },
     "execution_count": 29,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#Next we will use some built-in functions Python has\n",
    "#for example, pow() allows us to perform (81/9)^2 \n",
    "pow((81/9),2)+20"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "8.0"
      ]
     },
     "execution_count": 30,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#for the square root of 64 we first import the math module and then call the function:\n",
    "import math\n",
    "math.sqrt(64)\n",
    "#note that in Python 3 the syntax is module.function(argument)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1.556302500767287"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#suppose we wanted to change the base to find log(36), i.e. base 10\n",
    "math.log(36,10)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "3.58351893845611"
      ]
     },
     "execution_count": 32,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#for ln(36) we do:\n",
    "math.log(36)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Part 2: Working with Vectors \n",
    "\n",
    "In this section we will use Python to create and manipulate vectors, using different functions. The basis for any array manipulation is NumPy. For a much more thorough tutorial on arrays and using NumPy please consult:<a> href=\"https://jakevdp.github.io/PythonDataScienceHandbook/02.00-introduction-to-numpy.html\" > Introduction to NumPy </a>\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[45 31 60 80 32]\n"
     ]
    }
   ],
   "source": [
    "#suppose we wanted to create a vector called x to contain the numbers 45. 31, 60, 80, 32\n",
    "#first we have to import numpy:\n",
    "import numpy as np\n",
    "#now we create the vector using the array function:\n",
    "x = np.array([45,31,60,80,32])\n",
    "#when we call for x we can use the function print() to see the numbers x contains:\n",
    "print(x)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 34,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "49.6"
      ]
     },
     "execution_count": 34,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#suppose we wanted to find the mean of x, we simply do:\n",
    "x.mean()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "18.48891559827131"
      ]
     },
     "execution_count": 35,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#for the standard deviation we perform:\n",
    "x.std()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([ 73, 121, 105, 140, 102])"
      ]
     },
     "execution_count": 39,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#now suppose we want to create another vector called y:\n",
    "y = np.array([28,90,45,60,70])\n",
    "#we can add the elements of these vectors together by performing:\n",
    "x+y "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1260, 2790, 2700, 4800, 2240])"
      ]
     },
     "execution_count": 40,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#we can also multiply the elements of these vectors by doing:\n",
    "x*y"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "108.2"
      ]
     },
     "execution_count": 41,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#finally, we can create the vector z which adds x and y and get its mean:\n",
    "z=x+y\n",
    "z.mean()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Part 3: Working with Matrices\n",
    "\n",
    "For this last section we will work with matrices using Python. The logic is quite similar as to the previous section since we are also operating with arrays using NumPy. The idea here is to perform basic linear algebra which can serve as a foundation for deeper analysis:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1., 2., 3.],\n",
       "       [4., 5., 6.]])"
      ]
     },
     "execution_count": 42,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#Suppose we want to create a 2x3 matrix called a with the same numbers from the previous post:\n",
    "a = np.array([[1., 2., 3.], [4., 5., 6.]])\n",
    "#here we can manually separate each row and we can see we have created a 2x3 matrix\n",
    "a"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 6., 23.],\n",
       "       [-1.,  7.],\n",
       "       [ 8.,  9.]])"
      ]
     },
     "execution_count": 43,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#now we can create a 3x2 matrix and call it b:\n",
    "b = np.array([[6., 23.], [-1, 7], [8, 9]])\n",
    "b"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 28.,  64.],\n",
       "       [ 67., 181.]])"
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#to multiply axb we use de dot function and can shorten our code by doing:\n",
    "a.dot(b)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "metadata": {},
   "outputs": [],
   "source": [
    "#to use more matrix functions we can create a 3x3 matrix and call it c\n",
    "c= np.array([[1., 8., 10.], [2., 5., 11.],[9.,4.,12.]])\n",
    "#to access these matrix functions we will use linalg which comes with mumpy:\n",
    "from numpy.linalg import inv,det"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 0.06504065, -0.22764228,  0.15447154],\n",
       "       [ 0.30487805, -0.31707317,  0.03658537],\n",
       "       [-0.1504065 ,  0.27642276, -0.04471545]])"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#to find the inverse of c we use inv()\n",
    "inv(c)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "246.00000000000014"
      ]
     },
     "execution_count": 47,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#to find the determonant of c we use det()\n",
    "det(c)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Conclusions\n",
    "\n",
    "I hope this simple tutorial was useful if you are unfamiliar with Python. There are subtle differences with how R and Python read the matrix imputs but it is still fairly similar. Thank you for coming along!"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
