****************************************
NumPy: The Absolute Basics for Beginners
****************************************

This is a working outline for a future section introducing NumPy to absolute beginners. If you have comments or suggestions, please don’t hesitate to reach out!



How to install NumPy
--------------------
  
To install NumPy, we strongly recommend using a scientific Python distribution. If you're looking for the full instructions for installing NumPy on your operating system, you can find all of the details `here: <https://www.scipy.org/install.html>`_.

If you don't have Python yet, you might want to consider using Anaconda. It's the easiest way to get started. The good thing about getting this distribution is is the fact that you don’t need to worry too much about separately installing NumPy or any of the major packages that you’ll be using for your data analyses, such as pandas, Scikit-Learn, etc.
  
If you already have Python, you can install NumPy with

::

  conda install numpy
  
or 

::

  pip install numpy
  
You can find all of the installation details in the `Installation <https://www.scipy.org/install.html>`_ section at scipy.org.

How to import NumPy
-------------------

If you want to use a package or library in your code, you first need to make it accessible. In order to start using NumPy, you'll need to import it. To make use of the functions available in NumPy, you'll need to import it with an import statement. This can be easily done with:

::

  import numpy as np 

We shorten "numpy" to "np" in order to save time and also to keep code standardized so that anyone working with your code can easily understand and run it.

What is an array?
-----------------

An array is a central data structure of the NumPy library. It's a grid of values and it contains information about the raw data, how to locate an element, and how to interpret an element. It has a grid of elements that can be indexed in `various ways <https://numpy.org/devdocs/user/quickstart.html#indexing-slicing-and-iterating>`_. The elements are all of the same type, referred to as the array `dtype`. 

All of the values in an array should be the same type. An array can be indexed by a tuple of nonnegative integers, by booleans, by another array, or by integers. The **rank** of the array is the number of dimensions. The **shape** of the array is a tuple of integers giving the size of the array along each dimension.

One way we can initialize NumPy arrays is from nested Python lists. 

We can access the elements in the array using square brackets.

When you're accessing elements, remember that indexing starts at 0. That means that, if you want to access the first element in your array, you'll be accessing element "0".

- How to create an array (ndarray object)

How to create a basic array
---------------------------

To create a NumPy array, you can use the function `np.array()`

All you need to do to create a simple array is pass a list to it. If you choose to, you can also specify the type of data in your list. You can find more information about data types `here <https://numpy.org/devdocs/user/quickstart.html#arrays-dtypes>`_.

::

    import numpy as np

    # create a 1-D array
    a = np.array([1,2,3])

You can visualize your array this way:

.. image:: images/np_array.png

More information about arrays
-----------------------------

What else might an array be called?

You might occasionally hear an array referred to as an "ndarray," which is shorthand for "N-dimensional array." You might also hear **1-D**, or one-dimensional array, **2-D**, or two-dimensional array, and so on. The numpy `ndarray` class is used to represent both matrices and vectors. A vector is an array with a single column, while a matrix referrs to an array with multiple columns.

- What are the attributes of an array?

What’s the difference between a Python List and a NumPy array? 
--------------------------------------------------------------
  
While a Python list can contain different data types within a single list, all of the elements in a NumPy array should be homogenous. The mathematicl operations that are meant to be performed on arrays wouldn't be possible if the arrays weren't homogenous. 

Why use NumPy?
--------------

NumPy arrays are faster and more compact than Python lists. An array consumes less memory and is convenient to use. NumPy uses much less memory to store data and it provides a mechanism of specifying the data types, which allow the code to be optimisted even further. 

How do you know the shape and size of an array?
-----------------------------------------------

**ndarray.ndim** will tell you the number of axes, or dimensions, of the array.

**ndarray.shape** will display a tuple of integers that indicate the number of elements stored along each dimension of the array. If, for example, you have a 2D-array with 2 rows and 3 columns, the shape of your array is (2,3).

**ndarray.size** will tell you the total number of elements of the array. This is, in other words, the product of the elements of the array's shape.

For example:

::

      import numpy as np
      array_example = np.array([[[0, 1, 2, 3]
                                 [4, 5, 6, 7]],

                                 [[0, 1, 2, 3]
                                  [4, 5, 6, 7]],

                                  [0 ,1 ,2, 3]
                                  [4, 5, 6, 7]]])

  array_example.ndim
  array_example.size
  array_example.shape

**Output:**

::

  3
  24
  (3,2,4)

Can you reshape an array?
-------------------------
  
You can! 

::

  numpy.reshape() 

will give a new shape to an array without changing the data. Just remember that when you use the reshape method, the array you want to produce needs to have the same number of elements as the original array. If you start with an array with 12 elements, you'll need to make sure that your new array also has a total of 12 elements.

For example:

::

  a = np.arange(6)
  print('Original array:')
  print(a)
  print('\n')

  b = a.reshape(3,2)
  print('Modified array:')
  print(b)

**Output:**

::

  Original array:
  [0 1 2 3 4 5]

  Modified array:
  [[0 1]
   [2 3]
   [4 5]]

Optional parameters you can specify are:

::

  numpy.reshape(a, newshape, order)

**a** is the array to be reshaped.

**newshape** is the new shape you want. You can specify an integer or a tuple of integers. If you specify an integer, the result wil be an array of that length. The shape should be compatible with the original shape.

**order** 'C' means to read/write the elements using C-like index order,  ‘F’ means to read / write the elements using Fortran-like index order, ‘A’ means to read / write the elements in Fortran-like index order if a is Fortran contiguous in memory, C-like order otherwise.

How to create an array from existing data
-----------------------------------------

  - reading in a CSV

::

  import pandas as pd

  # If all oof your columns are the same type:
  x = pd.read_csv('music.csv').values

  # You can also simply select the columns you need:
  x = pd.read_csv('music.csv', columns=['float_colname_1', ...]).values

.. image:: images/np_pandas.png

- **How to create a new array from an existing array**
- **How to specify the datatype**
  
- Examples of commonly used NumPy dtypes

Indexing and Slicing
--------------------

::

   # create a 1-D array
    a = np.array([1,2,3])

    # print the first element of the array
    print(a[0])

**Output:**

::

    1

We can index and slice NumPy arrays in the same ways we can slice Python lists:

.. image:: images/np_indexing.png

- **Basic array operations(np.sum, np.dot)**

  - Operations on a single array

  - Unary operators

  - Binary operators

nce you've created your arrays, you can start to work with them. Let's say, for example, that you've created two arrays, one called "data" and one called "ones": 

.. image:: images/np_array_dataones.png

You can easily add arrays together with the plus sign.

::

  data + ones

.. image:: images/np_data_plus_ones.png

Of course, you can do more than just addition!

::

  data - ones
  data * data
  data / data

.. image:: images/np_sub_mult_divide.png

Broadcasting
------------

There are times when you might want to carry out an operation between an array and a single number (also called *an operation between a vector and a scalar*). Your  "data" array might, for example, contain information about distance in miles but you want to convert the information to kilometers. You can perform this operation with 

::

  data * 1.6

.. image:: images/np_multiply_broadcasting.png

NumPy understands that the multiplication should happen with each cell. That concept is called **broadcasting**.

How do I find the mean, median, maximum, and more?
--------------------------------------------------

NumPy also performs aggregation functions. In addition to `min`,  `max`, and `sum`, you can easily run `mean` to get the average, `prod` to get the result of multiplying the elements together, `std` to get the standard deviation, and more.

::

  data.max()
  data.min()
  data.sum()

.. image:: images/np_aggregation.png

It's very common to want to aggregate along a row or column. By default, every NumPy aggregation function will return the aggregate of the entire array:

::

  A = np.random.random((3, 4))
  print(A)

  # Result
 [[0.45053314 0.17296777 0.34376245 0.5510652 ]
 [0.54627315 0.05093587 0.40067661 0.55645993]
 [0.12697628 0.82485143 0.26590556 0.56917101]]

  A.sum()

  A.min()

**Output:**

::

  # Sum
  4.8595783866706

  # Minimum
  0.050935870838424435

You can easily specify which axis you want the aggregation function to be computed. For example, you can find the minimum value within each column by specifying `axis=0`.

::

  A.min(axis=0)

**Output:**

::

  array([0.12697628, 0.05093587, 0.26590556, 0.5510652 ])

The four values listed above correspond to the number of columns in your array. With a four-column array, you can expect to get four values as your result.

- **How to inspect the size and shape of a NumPy array**

You can get the dimensions of a NumPy array any time using ndarray.shape and NumPy will return the dimensions of the array as a tuple.

For example, if you created this array:

::

  np_arr = np.array([[1 , 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
 
  print(np_arr)

**Output:**

::

  [[ 1  2  3  4]
  [ 5  6  7  8]
  [ 9 10 11 12]]

Use `.shape` if you want to quickly find the shape of your array:

::

  np_arr.shape

**Output**

::

  (3, 4)

You can find the number of rows with:

::

  # np_arr.shape[0]

  num_of_rows = np_arr.shape[0]
 
  print('Number of Rows : ', num_of_rows)

**Output:**

::

  Number of Rows :  3

Or the number of columns:

::

  # np_arr.shape[1]

  num_of_columns = np_arr.shape[1]
 
  print('Number of Columns : ', num_of_columns) 

**Output:**

::
  
  Number of Columns :  4

It's also easy to find the total number of elements in your array:

::

  # np_arr.shape[0] * np_arr.shape[1]

  print('Total number of elements in array : ', np_arr.shape[0] * np_arr.shape[1])

**Output:**

::

  Total number of elements in array:  12

You can also use np.shape() with a 1D array, of course.

::

  # Create an array
  arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

  print('Shape of 1D array: ', arr.shape)
  print('Length of 1D array: ', arr.shape[0])

**Output:**

::

  Shape of 1D array:  (8,)
  Length of 1D array:  8


You can get the dimensions of an array using np.size()

::

  # get number of rows in array
  num_of_rows2 = np.size(np_arr, 0)
 
  # get number of columns in 2D numpy array
  num_of_columns2 = np.size(np_arr, 1)
 
  print('Number of Rows : ', num_of_rows2)
  print('Number of Columns : ', num_of_columns2)

**Output:**

::

  Number of Rows :  3
  Number of Columns: 4

You can print the total number of elements as well:

::
  
  print('Total number of elements in  array : ', np.size(np_arr))

**Output:**

::

  Total number of elements in  array :  12

This also works for 3D arrays:

::

  arr3D = np.array([ [[1, 1, 1, 1], [2, 2, 2, 2], [3, 3, 3, 3]],
                 [[4, 4, 4, 4], [5, 5, 5, 5], [6, 6, 6, 6]] ])
 
  print(arr3D)

**Output:**

::

  [[[1 1 1 1]
    [2 2 2 2]
    [3 3 3 3]]

  [[4 4 4 4]
    [5 5 5 5]
    [6 6 6 6]]]

You can easily print the size of the axis:

::

  print('Axis 0 size : ', np.size(arr3D, 0))
  print('Axis 1 size : ', np.size(arr3D, 1))
  print('Axis 2 size : ', np.size(arr3D, 2))

**Output:**

::

  Axis 0 size :  2
  Axis 1 size :  3
  Axis 2 size :  4

You can print the total number of elements:

::

  print('Total number of elements in 3D Numpy array : ', np.size(arr3D))

**Output:**

::

  Total number of elements in 3D Numpy array :  24

You can also use np.size() with 1D arrays:

::

  # Create a 1D array
  arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

  # Determine the length
  print('Length of 1D numpy array : ', np.size(arr))

**Output:**

::

  Length of 1D numpy array :  8

- **How to check whether a list is empty or not**
- **How to represent missing values and infinite values**

- **Sorting an array**

- **How to concatenate two arrays**
  
  - column-wise

  - row-wise

  - np.concatenate, np.stack, np.vstack, np.hstack

- **How to sort an array**
  
  - based on one (or more) columns
    
    - np.sort
    
    - np.argsort

    - np.argmin

    - np.argsort

  - based on two or more columns
    
    - np.lexsort


Creating Matrices
-----------------

You can pass Python lists of lists to create a matrix to represent them in NumPy.

::

  np.array([[1,2],[3,4]])

.. image:: images/np_create_matrix.png

Indexing and slicing operations can be useful when you're manipulating matrices:

::

  data[0,1]
  data[1:3]
  data[0:2,0]

.. image:: images/np_matrix_indexing.png

You can aggregate matrices the same way you aggregated vectors:

::

  data.max()
  data.min()
  data.sum()

.. image:: images/np_matrix_aggregation.png

You can aggregate all the values in a matrix and you can aggregate them across columns or rows using the `axis` parameter:

::
  
  data.max(axis=0)
  data.max(axis=1)


.. image:: images/np_matrix_aggregation_row.png

Once you've created your matrices, you can add and multiply them using arithmetic operators if you have two matrices that are the same size.

::

  data + ones

.. image:: images/np_matrix_arithmetic.png

You can do these arithmetic operations on matrices of different sizes, but only if the different matrix has only one column or onw row. In this case, NumPy will use its broadcast rules for the operation.

::

  data + ones_row

.. image:: images/np_matrix_broadcasting.png

- How to extract specific items from an array
- How to create sequences, repetitions, and random numbers

NumPy can do everything we've mentioned in any number of dimensions, that's why it's called an N-Dimensional array.

Be aware that when NumPy prints N-Dimensional arrays, the last axis is looped over the fastest while the first axis is the slowest. That means that 

::

  np.ones((4,3,2))

**Output:**

::

  array([[[1., 1.],
        [1., 1.],
        [1., 1.]],

       [[1., 1.],
        [1., 1.],
        [1., 1.]],

       [[1., 1.],
        [1., 1.],
        [1., 1.]],

       [[1., 1.],
        [1., 1.],
        [1., 1.]]])

 
There are often instances where we want NumPy to initialize the values of an array. NumPy offers methods like ones(), zeros() and random.random() for these instances. All you need to do is pass in the number of elements you want it to generate.

::

  np.ones(3)
  mp.zeros(3)
  np.random.random((3)
  
.. image:: images/np_ones_zeros_random.png

- np.linspace
  
- np.logspace

- np.tile
  
- np.zeros

- np.ones

- Random Number Generation (update below to numpy.random.Generator)

  - np.random.randn
  
  - np.random.randint
  
  - np.random.random
  
  - np.random.choice
  
  - np.random.RandomState, np.random.seed

You can also use the `ones()`, `zeros()`, and `random()` methods to create a matrix if you give them a tuple describing the deminsions of the matrix.

::

  np.ones(3,2)
  mp.zeros(3,2)
  np.random.random((3,2)

.. image:: images/np_ones_zeros_matrix.png

- How to get the unique items and the counts
- How to get index locations that satisfy a given condition 

Transposing and reshaping a matrix
----------------------------------

It's common to need to rotate your matrices. NumPy arrays have the property `T` that allows you to transpose a matrix.

.. image:: images/np_transposing_reshaping.png

You may need to switch the dimensions of a matrix. This can happen when, for example you have a model that expects a certain input shape that might be different from your dataset. This is where the `reshape` method can be useful. You pass in the new dimensions that you want for the matrix.

::

  data.reshape(2,3)
  data.reshape(3,2)

.. image:: images/np_reshape.png

- How to reverse
 
  - How to reverse the rows
 
  - How to reverse the whole array

- Reshaping and Flattening multidimensional arrays
  
  - flatten vs ravel

- How to import and export data as a CSV
- How to save and load NumPy objects
- How to apply a function column-wise or row-wise
- How to convert a 1D array into a 2D array (how to add a new axis)

Formulas:
---------

Implementing mathematical formulas that work on matrices and vectors is one of the things that make NumPy so highly regarded in the scientific Python community. 

For example, this is the mean square error formula (a central formula used in supervised machine learning models that deal with regression):

.. image:: images/np_MSE_formula.png

Implementing this formula is simple and straightforward in NumPy:

.. image:: images/np_MSE_implementation.png

What makes this work so well is that `predictions` and `labels` can contain one or a thousand values. They only need to be the same size. 

You can visualize it this way:

.. image:: images/np_mse_viz1.png

In this example, both the predictions and labels vectors contain three values, meaning `n` has a value of three. After we carry out subtractions the values in the vector are squared. Then NumPy sums the values, and your result is the error value for that prediction and a score for the quality of the model.

.. image:: images/np_mse_viz2.png

.. image:: images/np_MSE_explanation2.png

- **How to plot arrays, very basic with Matplotlib**
- **How to read a docstring with `?` and source code with `??` in IPython/Jupyter**

- **More useful functions:**

  - np.clip
  
  - np.digitize
  
  - np.bincount
  
  - np.histogram





-------------------------------------------------------

*Image credits: Jay Alammar http://jalammar.github.io/*

