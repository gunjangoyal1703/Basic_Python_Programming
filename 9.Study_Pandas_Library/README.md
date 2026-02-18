# <ins>Study_Pandas_Library</ins>
## **AIM** </br>
To explore the Pandas library in Python for data manipulation and analysis, focusing on its primary data structures and techniques for filtering and inspecting datasets.

## **OBJECTIVES** </br>
* To understand the importing process and environment setup for Pandas.</br>
* To learn the creation and structure of DataFrames and Series.</br>
* To convert and manipulate arrays within the Pandas ecosystem.</br>
* To implement conditional filtering and conditional statements to extract specific data subsets.</br>

## **THEORY** </br>
Pandas is an open-source library providing high-performance, easy-to-use data structures. It is built on top of NumPy, making it exceptionally fast for handling tabular data.
### 1.Importing the Library
Pandas is usually imported with the alias **pd**: <ins>import pandas as pd</ins>
###  2.Core Data Structures
* **Series:** A 1-D labeled array capable of holding any data type.
* **DataFrame:** A 2-D labeled data structure (like an Excel sheet or SQL table). It is a collection of Series objects sharing the same index.
### 3.Arrays to DataFrames
Pandas integrates seamlessly with NumPy. You can convert a NumPy array into a DataFrame using <ins>**pd.DataFrame(array_name)**</ins>, allowing for complex mathematical data to be labeled with row and column headers.
### 4.Conditional Filtering
This is the process of selecting rows based on specific criteria. Pandas uses Boolean Indexing to mask data.</br>
Example: <ins>**df[df['Age'] > 25]** </ins>returns only the rows where the 'Age' column exceeds 25.
### 5.Conditional Statements (Logic)
Beyond simple filtering, Pandas uses methods like **np.where()** or **.apply()** with lambda functions to create new data based on conditions </br>
**Example:** creating a 'Status' column that marks 'Pass' if a score is >40 and 'Fail' otherwise).
### 6.Essential Pandas Functions
|Category|	Function|	Purpose|
|:---|:---|:---|
|**Inspection**	|df.info()|	Provides a concise summary of the DataFrame, including memory usage and non-null counts.|
||df.shape	|Returns a tuple representing the dimensionality (rows, columns).|
||df.columns|	Returns the labels of the columns.|
|**Data Cleaning**	|df.isnull()	|Detects missing values (returns a boolean mask).|
||df.fillna(x)	|Replaces NaN (null) values with a specified value x.|
||df.dropna()	|Removes rows or columns that contain missing values.|
||df.rename()|	Alters axes labels (renaming specific columns or index names).|
|**Selection**|	df.unique()|	Returns unique values of a specific column.|
||df.nunique()	|Counts the number of unique entries in a column.|
||df.value_counts()|	Returns a count of unique values in descending order.|
|**Manipulation**	|df.groupby()|	Groups data using a mapper or by a series of columns (used for aggregation).|
||df.sort_values()	|Sorts the DataFrame by the values of a specific column.|
||df.pivot_table()|	Create a spreadsheet-style pivot table as a DataFrame.|
||df.merge()	|Combines two DataFrames using a database-style "join" operation.|
||df.apply()	|Applies a function (like a lambda) along an axis of the DataFrame.|
### 7. Real Life Applications
#### 1. Customer Churn Prediction (Telecommunications & SaaS)
* <ins>The Problem:</ins> Companies need to know which customers are likely to cancel their subscriptions.
* <ins>Pandas Usage:</ins> Data scientists use **df.groupby()** to analyze usage patterns and conditional filtering to identify "at-risk" customers (e.g., users who haven't logged in for 30 days).
* <ins>Action:</ins> It allows businesses to automate personalized discount offers to those specific users.
#### 2. Real-Time Sports Analytics
* <ins>The Problem:</ins> Professional teams (NBA, IPL, MLB) collect thousands of data points per second during a game.
* <ins>Pandas Usage:</ins> Coaches use Pandas to perform Exploratory Data Analysis (EDA). They use **.pivot_table()** to compare player performance under different conditions (e.g., Home vs. Away games or against specific opponents).
* <ins>Action:</ins> Helps in deciding player substitutions and tactical shifts based on historical probability.
#### 3. Supply Chain & Inventory Management
* <ins>The Problem:</ins> Retailers need to ensure products don't go out of stock without over-ordering.
* <ins>Pandas Usage:</ins> By using **df.merge()**, companies combine sales data with warehouse inventory levels. They apply conditional statements to trigger "Low Stock" alerts when inventory drops below a calculated threshold.
* <ins>Action:</ins> Automates the re-ordering process and optimizes warehouse space.
#### 4. Meteorological & Climate Study
* <ins>The Problem:</ins> Weather stations collect vast amounts of temperature, humidity, and pressure data globally.
* <ins>Pandas Usage:</ins> Pandas is used for Time-Series Analysis. Researchers use **.resample()** to convert hourly weather data into daily, monthly, or yearly averages to track global warming trends.
* <ins>Action:</ins> Enables the visualization of long-term climate shifts and helps in predicting natural disasters.
#### 5. Web Scraping & Sentiment Analysis
* <ins>The Problem:</ins> Brands want to know what people are saying about them on social media or review sites.
* <ins>Pandas Usage:</ins> After scraping data from the web, Pandas is used to clean the "noisy" text data. **df.apply()** is used to run sentiment analysis functions (scoring text as Positive/Negative) across millions of rows.
* <ins>Action:</ins> Helps marketing teams adjust their strategies based on public opinion.

## **CONCLUSION**  </br>
The study of Pandas reveals it as an indispensable tool for Data Wrangling. Its ability to handle missing data, align disparate datasets, and perform complex conditional filtering makes it superior to standard Python lists for analytical tasks. Mastery of the DataFrame structure is the first step toward professional data science and automated reporting.





