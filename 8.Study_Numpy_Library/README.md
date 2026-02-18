# <ins>Study_Numpy_Library</ins>
## **AIM** </br>
To study and implement the NumPy (Numerical Python) library to perform efficient numerical computations, manage multi-dimensional arrays, and execute high-level mathematical functions.</br>

## **OBJECTIVES** </br>
* To learn how to create arrays using functions like **np.array(), np.zeros(), np.ones(), and np.arange()**. </br>
* To perform Statistical Analysis **(mean, median, standard deviation)** and Linear Algebra operations **(dot products, transposes)**. </br>
* To explore Reshaping and Stacking techniques for **manipulating data dimensions**.</br>

## **THEORY** </br>

NumPy is the fundamental package for scientific computing in Python. It provides a high-performance multidimensional array object and tools for working with these arrays. Unlike Python lists, NumPy arrays are stored in contiguous memory locations, making them significantly faster for processing.

### 1. Universal Functions (ufuncs)
The core of NumPy's mathematical capability lies in Universal Functions (ufuncs). 
* **Theory:** A ufunc is a "vectorized" wrapper that operates on ndarrays in an element-by-element fashion.
* **Key Features:** They support broadcasting (operating on arrays of different shapes) and type casting.
* **Categories:**
**Arithmetic:** add(), subtract(), multiply(), divide(), power().</br>
**Trigonometric:** sin(), cos(), tan(), and inverse functions like arcsin(). </br>
**Logarithmic/Exponential:** exp(), log(), log10(), and log2(). 

### 2. Array Creation Functions
These routines provide efficient ways to initialize data without manually populating elements. 
* **array():** Converts Python lists or tuples into an ndarray.
* **zeros() / ones():** Creates arrays of a specified shape filled with 0s or 1s.
* **arange():** Returns evenly spaced values within a given interval, similar to Python's range().
* **linspace():** Generates a specific number of samples between two points, useful when the exact step size is less important than the count.
  
### 3. Manipulation & Transformation Functions
These functions alter the structure or arrangement of data without necessarily changing the values. 
* **reshape():** Changes the array shape (e.g., 1D to 2D) without changing its total size.
* **transpose() (or .T):** Reverses or permutes the axes of an array, turning rows into columns.
* **concatenate():** Joins a sequence of arrays along an existing axis.
* **sort():** Returns a sorted copy of an array along a specified axis. 

### 4. Statistical & Aggregation Functions
These functions reduce the dimensions of an array to provide summary metrics. 
* **Descriptive Statistics:** mean(), median(), std() (standard deviation), and var() (variance).
* **Extrema:** min(), max(), argmin(), and argmax() (returns indices of min/max values).
* **Sums & Products:** sum() for total addition and prod() for total multiplication across elements or axes. 

### 5. Specialized Domain Functions
* **Linear Algebra (numpy.linalg):** Provides low-level algorithms for matrix_rank(), inv() (inverse), and det() (determinant).
* **Random Sampling (numpy.random):** Functions like rand() or randint() to generate arrays of random data for simulations.

### 6. Fundamental Data Structure
* **ndarray (N-dimensional array):** The central feature of NumPy. It is a table of elements (usually numbers), all of the same type, indexed by a tuple of non-negative integers.
* **Dimensions (Axes):** In NumPy, dimensions are called axes. A 2D array has two axes: axis 0 (rows) and axis 1 (columns).
* **Axes & Rank:** Dimensions in NumPy are called axes. The number of axes determines the rank of the array.
* **Contiguous Memory:** Unlike lists, NumPy arrays store elements in adjacent memory locations, allowing for faster CPU access (locality of reference).
  
### 7. Core Concepts
* **Vectorization:** The practice of replacing explicit loops with array expressions. This allows operations to be performed on entire arrays at once, leveraging optimized C and Fortran code under the hood.
* **Broadcasting:** A powerful mechanism that allows NumPy to work with arrays of different shapes during arithmetic operations. The smaller array is "broadcast" across the larger array so they have compatible shapes.
* **Universal Functions (ufuncs):** Functions like np.sin(), np.exp(), and np.add() that operate element-wise on arrays.
  
### 8. Common Operations Table
|**Feature** |	**Python Lists**|	**NumPy Arrays**|
 |:---|:---|:---|
|**Data Types**	|Heterogeneous (mixed types)|	Homogeneous (same type)|
|**Size**	|Dynamic (can grow/shrink)|	Fixed size upon creation|
|**Memory**|	High overhead per element	|Memory-efficient (contiguous)|
|**Performance**|	Slower for numerical tasks|	Fast (optimized C-code)|
|**Math Operations**|	Requires explicit loops	|Supports vectorized arithmetic|

### 9. Array Manipulation & Selection
* **Reshaping:** Using reshape() to change dimensions without altering data.
* **Boolean Indexing:** Selecting data based on specific conditions (e.g., arr[arr > 0]).
* **Aggregation:** Reducing data using sum(), mean(), min(), or max() along specific axes.
  
### 10. Real-World Applications
* **Data Analysis:** Cleaning raw data and calculating statistical baselines.
* **Machine Learning:** Handling feature matrices for models in Scikit-learn or TensorFlow.
* **Image Processing:** Representing images as 3D arrays for transformations and filtering.
* **Finance:** Performing risk assessments and time-series modeling.
  
## **CONCLUSION**  </br>
We are replacing slow Python loops with vectorized operations and managing memory more effectively through ndarrays, it provides the performance and high-level syntax necessary for modern scientific research and data-driven software.
