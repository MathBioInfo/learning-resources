NumPy (short for Numerical Python) is a powerful Python library used for numerical and scientific computing. It provides high-performance multidimensional arrays and matrices, as well as a wide range of mathematical functions to operate on these arrays.

NumPy is optimized for performance, making it an essential library for tasks that involve large-scale data manipulation and computation. It provides a convenient interface to work with data in various formats, including CSV, TSV, and SQL databases.

Some of the key features of NumPy include:
- Multidimensional arrays with efficient indexing and slicing
- Broadcasting capabilities to apply operations to arrays with different shapes and sizes
- Mathematical functions for array manipulation, including linear algebra, Fourier analysis, and random number generation
- Integration with other libraries, including Matplotlib for data visualization and Pandas for data analysis and manipulation.

Overall, NumPy is an essential tool for anyone working with scientific computing or data analysis in Python.
The source code for NumPy is located at this github repository [https://github.com/numpy/numpy](https://github.com/numpy/numpy).

## Installing NumPy
Resource: [Installing NumPy](https://numpy.org/install/)

NumPy can be installed in several ways depending on your operating system and Python environment. Here are some general steps to install NumPy:
- Ensure that you have Python installed on your computer. You can download Python from the official website: https://www.python.org/downloads/
- Open a command prompt or terminal window on your computer.
- Install NumPy using a package manager such as pip. Type the following command:
```Python
pip install numpy
```

This will download and install the latest version of NumPy available on PyPI (Python Package Index).

Alternatively, you can install NumPy using Anaconda, a popular distribution of Python and scientific computing packages.
```python
# Best practice, use an environment rather than install in the base env
conda create -n my-env
conda activate my-env
# If you want to install from conda-forge
conda config --env --add channels conda-forge
# The actual install command
conda install numpy
```
Once the installation is complete, you can use NumPy in your Python code by importing it:
```Python
import numpy as np
```
This will allow you to use the NumPy functions and arrays in your code with the "np" alias.

### A tutorial to get you started with NumPy
Import NumPy

Start by importing NumPy into your Python code using the following line:

```Python
import numpy as np
```

This line imports the NumPy library and assigns the alias "np" to it, which is a common convention.

#### Creating NumPy arrays

NumPy arrays are the main data structure in NumPy. You can create a NumPy array using the ```numpy.array()``` function. For example, to create a 1D array of integers from a list, you can do the following:
```Python
A = np.array([1, 2, 3, 4, 5])
print(A)
```

This will create a NumPy array a and print it to the console:
```
[1 2 3 4 5]
```

One can also create a 2D array by passing a list of lists to the ```numpy.array()``` function. For example:
```Python
B = np.array([[1, 2, 3], [4, 5, 6]])
print(B)
```

This will create a 2D array b and print it to the console:

```
[[1 2 3]
 [4 5 6]]
```

#### Array indexing and slicing

NumPy arrays can be indexed and sliced just like regular Python lists. For example, to access the first element of array A, you can use:
```Python
print(a[0])
```

This will print the first element of a, which is 
```
1
```

You can also slice an array using the colon : operator. For example, to get the first three elements of a, you can use:
```Python
print(a[:3])
```
This will print the first three elements of A, which are 
```
[1 2 3]
```

#### Array arithmetic

NumPy provides a wide range of arithmetic operations that can be performed on arrays. For example, you can add, subtract, multiply, and divide arrays element-wise using the arithmetic operators +, -, *, and /. For example:

```Python
x = np.array([1, 2, 3])
y = np.array([4, 5, 6])
print(x + y)
print(x - y)
print(x * y)
print(x / y)
```
This will print the element-wise sum, difference, product, and quotient of arrays x and y.

#### Array aggregation

NumPy provides many functions to aggregate arrays, such as sum(), mean(), min(), max(), and std(). For example, to compute the sum, mean, minimum, maximum, and standard deviation of an array a, you can do the following:

```Python
print(np.sum(A))
print(np.mean(A))
print(np.min(A))
print(np.max(A))
print(np.std(A))
```

This will print the sum, mean, minimum, maximum, and standard deviation of array A.


