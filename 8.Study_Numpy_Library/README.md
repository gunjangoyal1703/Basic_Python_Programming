# <ins>Study_Numpy_Library</ins>
## **AIM** </br>
To study the fundamentals of the NumPy (Numerical Python) library in Python, focusing on its core data structure, the n-dimensional array (ndarray), and its primary functionalities for numerical computation.

## **OBJECTIVES** </br>
* To learn the declaration and installation of the NumPy library.</br>
* To understand the creation and manipulation of NumPy arrays.</br>
* To explore different data types (dtype) supported by NumPy.</br>
* To implement various inbuilt functions for mathematical and statistical operations.</br>
  
## **THEORY** </br>

NumPy is the foundational package for scientific computing in Python. It provides a high-performance multidimensional array object and tools for working with these arrays.

### 1.Declaration & Installation
NumPy can be installed using the command <ins>pip install numpy</ins>.  </br>
To use it in a script, it is typically imported with an alias:<ins>import numpy as np</ins>  </br>
### 2.NumPy Arrays (ndarray)
The primary object is the **ndarray**, a homogeneous multidimensional array. Unlike Python lists, NumPy arrays must contain elements of the **same data type**, which allows for more efficient memory storage and faster processing.</br>
* **Creation:** Arrays can be created from Python lists using np.array().</br>
* **Dimensions:** They can be 0-D (scalars), 1-D (vectors), or multi-dimensional (matrices).</br>
### 3.Data Types (dtype)
NumPy supports a wide range of numerical data types, including **int32**, **int64**, **float64**, **bool**, and **complex**. </br>
The data type can be explicitly defined during array creation using the **dtype** parameter.</br>
### 4.Inbuilt Functions
NumPy includes a vast library of functions for:
* **Array Creation:** np.zeros(), np.ones(), np.arange(), and np.linspace().
* **Mathematical Operations:** np.add(), np.sqrt(), np.exp(), and np.sin().
* **Statistical Analysis:** np.mean(), np.median(), np.std(), np.min(), and np.max().
* **Shape Manipulation:** np.reshape(), np.transpose(), and np.concatenate()
### 5.Commonly Used NumPy Inbuilt Functions
|Category	|Function|	Description|
|:---|:---|:---|
|Array Creation	|np.array()|	Creates an array from a list or tuple.|
||np.zeros()	|Creates an array filled with zeros of a specified shape.|
||np.ones()|	Creates an array filled with ones.|
||np.arange()	|Returns evenly spaced values within a given interval (like range).|
||np.linspace()	|Returns a specific number of even spaces between two points.|
|Shape & Size	|np.reshape()	|Changes the shape of an array without changing its data.|
||np.ndim	|Returns the number of array dimensions (axes).|
||np.size|	Returns the total number of elements in the array.|
||np.flatten()	|Collapses a multi-dimensional array into one dimension.|
|Math & Stats	|np.sum()|	Computes the sum of array elements (can be per axis).|
||np.mean()	|Computes the arithmetic mean.|
||np.sqrt()|	Calculates the non-negative square root of each element.|
||np.min() / np.max()	|Finds the minimum or maximum value in the array.|
||np.dot()	|Computes the dot product of two arrays (matrix multiplication).|
|Random	|np.random.rand()	|Creates an array of specified shape with random values [0, 1).|
||np.random.randint()|	Generates random integers within a specific range.|
### 6. Real Life Applications
#### 1. Data Science and Machine Learning
* <ins>Feature Engineering:</ins> NumPy is used to normalize data (scaling values to a common range) and handle missing values before training models.
* <ins>Model Implementation:</ins> It serves as the mathematical engine for algorithms like Linear Regression, Logistic Regression, and K-Nearest Neighbors (KNN) by calculating weights and loss functions through matrix multiplication.
* <ins>Foundational Base:</ins> Major AI frameworks like TensorFlow, PyTorch, and Scikit-learn rely on NumPy arrays as their primary data structure. 
#### 2. Image and Signal Processing
* <ins>Computer Vision:</ins> Digital images are essentially 3D arrays (Height × Width × RGB channels). NumPy is used for image manipulation such as cropping, rotating, flipping, and applying filters like Gaussian blur for noise reduction.
* <ins>Signal Analysis:</ins> Engineers use NumPy’s Fast Fourier Transform (FFT) functions to analyze frequency components in audio signals, medical data (like pulse oximeters), or sensor data.
#### 3. Financial and Business Analytics
* <ins>Risk Management:</ins> Financial analysts use NumPy to calculate volatility (via standard deviation), Value at Risk (VaR), and correlation coefficients between different assets in a portfolio.
* <ins>Predictive Simulations:</ins> It powers Monte Carlo simulations to forecast potential stock price movements by generating thousands of random price paths.
* <ins>Time Value of Money:</ins> It simplifies calculating present/future values, compound interest, and internal rates of return (IRR) without slow manual loops. 
#### 4. Scientific Research and Engineering
* <ins>Physics Simulations:</ins> Used to simulate complex physical systems, such as planetary motion or fluid dynamics, by representing physical relationships as matrices.
* <ins>Bioinformatics:</ins> Researchers utilize NumPy to analyze large-scale genetic data and predict protein structures.
* <ins>Control Systems:</ins> Essential in engineering for state-space models and circuit analysis (calculating impedance and frequency response).
## **CONCLUSION**  </br>
We are replacing slow Python loops with vectorized operations and managing memory more effectively through ndarrays, it provides the performance and high-level syntax necessary for modern scientific research and data-driven software.
