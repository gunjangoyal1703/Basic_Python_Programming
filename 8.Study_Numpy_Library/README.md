# <ins>Study_Numpy_Library</ins>
## **AIM** </br>
To study and implement the NumPy (Numerical Python) library to perform efficient numerical computations, manage multi-dimensional arrays, and execute high-level mathematical functions.</br>

## **OBJECTIVES** </br>
* To understand the core difference between Python Lists and NumPy Arrays **(ndarrays)**. </br>
* To learn how to create arrays using functions like **np.array(), np.zeros(), np.ones(), and np.arange()**. </br>
* To master Array Indexing and Slicing for extracting **specific data points or sub-arrays**.</br>
* To implement Vectorization and Broadcasting to **eliminate the need for explicit loops in mathematical operations**. </br>
* To perform Statistical Analysis **(mean, median, standard deviation)** and Linear Algebra operations **(dot products, transposes)**. </br>
* To explore Reshaping and Stacking techniques for **manipulating data dimensions**.</br>

## **THEORY** </br>
NumPy is the fundamental package for scientific computing in Python. It provides a high-performance multidimensional array object and tools for working with these arrays. Unlike Python lists, NumPy arrays are stored in contiguous memory locations, making them significantly faster for processing.

### 1. Fundamental Data Structure
* **ndarray (N-dimensional array):** The central feature of NumPy. It is a table of elements (usually numbers), all of the same type, indexed by a tuple of non-negative integers.
* **Dimensions (Axes):** In NumPy, dimensions are called axes. A 2D array has two axes: axis 0 (rows) and axis 1 (columns).
* **Axes & Rank:** Dimensions in NumPy are called axes. The number of axes determines the rank of the array.
* **Contiguous Memory:** Unlike lists, NumPy arrays store elements in adjacent memory locations, allowing for faster CPU access (locality of reference).
### 2. Core Concepts
* **Vectorization:** The practice of replacing explicit loops with array expressions. This allows operations to be performed on entire arrays at once, leveraging optimized C and Fortran code under the hood.
* **Broadcasting:** A powerful mechanism that allows NumPy to work with arrays of different shapes during arithmetic operations. The smaller array is "broadcast" across the larger array so they have compatible shapes.
* **Universal Functions (ufuncs):** Functions like np.sin(), np.exp(), and np.add() that operate element-wise on arrays.
### 3. Common Operations Table
|**Feature** |	**Python Lists**|	**NumPy Arrays**|
 |:---|:---|:---|
|**Data Types**	|Heterogeneous (mixed types)|	Homogeneous (same type)|
|**Size**	|Dynamic (can grow/shrink)|	Fixed size upon creation|
|**Memory**|	High overhead per element	|Memory-efficient (contiguous)|
|**Performance**|	Slower for numerical tasks|	Fast (optimized C-code)|
|**Math Operations**|	Requires explicit loops	|Supports vectorized arithmetic|
### 4. Array Manipulation & Selection
* **Reshaping:** Using reshape() to change dimensions without altering data.
* **Boolean Indexing:** Selecting data based on specific conditions (e.g., arr[arr > 0]).
* **Aggregation:** Reducing data using sum(), mean(), min(), or max() along specific axes. 
### 5. Real-World Applications
* **Data Analysis:** Cleaning raw data and calculating statistical baselines.
* **Machine Learning:** Handling feature matrices for models in Scikit-learn or TensorFlow.
* **Image Processing:** Representing images as 3D arrays for transformations and filtering.
* **Finance:** Performing risk assessments and time-series modeling.
  
## **CONCLUSION**  </br>
We are replacing slow Python loops with vectorized operations and managing memory more effectively through ndarrays, it provides the performance and high-level syntax necessary for modern scientific research and data-driven software.
