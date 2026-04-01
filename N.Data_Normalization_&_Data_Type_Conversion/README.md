
# <ins>Data Normalization & Data Type Conversion</ins>

## **AIM** 
* To study and perform data normalization and convert categorical variables into quantitative variables using various Python functions and operations.</br>
* To study the preprocessing techniques and Natural Language Processing (NLP) techniques used for analyzing text data.</br>

## **OBJECTIVES** 
* Understanding Normalization Techniques</br>
* Categorical Data Encoding</br>
* Avoiding Multicollinearity</br>
* Hands-on Data Preprocessing on Real Datasets</br>

## TOOLS
* **Python 3** — Primary language used for data manipulation and preprocessing</br>
* **Pandas** **(pandas)** — For creating and manipulating DataFrames, and applying get_dummies() for encoding</br>
* **NumPy** **(numpy)** — For numerical computations and array operations</br>
* **Scikit-learn** **(sklearn.preprocessing)** — Specifically LabelEncoder class for converting categorical labels into numeric form</br>

## DATASET USED
* **Custom Product Dataset** — Manually created dictionary-based DataFrame (Laptop, Mobile, Tablet, etc.) </br>
* **Amazon Products Dataset (amazon_products_dataset_Expt-14.csv)** — 50-row CSV file with fields like Price, Rating, Units_Sold</br>
* **Student Dataset (Student-Dataset.csv)** — 10-row CSV file with fields like CGPA, Department, Placement_Status, Salary</br>
  
## **THEORY** 
In real-world datasets, data is often collected from various sources and exists in different formats, scales, and types. Before applying any machine learning algorithm, it is essential to preprocess this raw data. Two of the most fundamental preprocessing steps: </br>
A. Data Normalization </br>
B. Data Type Conversion. </br>
These techniques ensure that the data is consistent, comparable, and suitable for further analysis or model building.</br><br>

### PART A : DATA NORMALIZATION<br>
Data Normalization is the process of rescaling numerical data so that it fits within a specific range or follows a particular distribution. It prevents features with larger magnitudes from dominating those with smaller magnitudes during model training.</br>
### 1. Min-Max Normalization
Min-Max Normalization scales the data to a fixed range, typically [0, 1]. It preserves the original distribution of the data and is useful when the algorithm requires bounded input values.</br>
#### FORMULA:</br>
#### X' = (X - Xmin) / (Xmax - Xmin)</br>
* **Xmin** = minimum value of the feature</br>
* **Xmax** = maximum value of the feature</br>
* **Result:** all values lie between 0 and 1</br>
### 2. Z-Score Normalization (Standardization)
Z-Score Normalization transforms data so that it has a mean of 0 and a standard deviation of 1. It is useful when the data follows a Gaussian (normal) distribution and is preferred for algorithms like SVM and Linear Regression.</br>
#### FORMULA:</br>
#### X' = (X - μ) / σ</br>
* **μ** = mean of the feature</br>
* **σ** = standard deviation of the feature</br>
* **Result:** values are centered around 0</br>
### 3. Decimal Scaling
Decimal Scaling normalizes data by dividing each value by an appropriate power of 10, such that the maximum absolute value becomes less than 1. It is the simplest normalization technique.</br>
#### FORMULA:</br>
#### X' = X / 10^j</br>
* **j** = smallest integer such that max|X'| < 1</br><br>

### PART B — DATA TYPE CONVERSION <br>
Machine learning algorithms work only with numerical data. However, many real-world datasets contain categorical (text-based) variables. Data Type Conversion refers to the process of transforming these categorical variables into numerical representations.</br>
### 1. Label Encoding
* **Label Encoding:** assigns a unique integer to each category in a column. It is suitable for binary or ordinal categorical variables where the order matters.</br>
* **Limitation:** For nominal categories with no natural order, label encoding can introduce unintended ordinal relationships.</br>
### 2. One-Hot Encoding
* **One-Hot Encoding:** creates a new binary column for each unique category in a variable. Each row gets a value of 1 in the column corresponding to its category and 0 in all others. It is used for nominal categorical variables.</br>
* **Limitation:** Can significantly increase the number of columns if a variable has many unique categories (known as the curse of dimensionality).</br>
### 3. Dummy Encoding
* **Dummy Encoding:** is similar to One-Hot Encoding but drops one of the created columns using drop_first=True. This avoids the Dummy Variable Trap, where two or more columns become perfectly correlated (multicollinearity), which can negatively affect regression models.</br>
* **Limitation:** When **drop_first=True** is used, one category is dropped and treated as the reference/baseline category. This can sometimes make interpretation of results difficult, especially when all categories are equally important.</br><br>

### Key Features of Scikit-learn
* Simple and efficient tools for data mining and data analysis</br>
* Accessible to everybody and reusable in various contexts</br>
* Built on NumPy, SciPy, and Matplotlib</br>
* Open source and commercially usable under BSD license</br><br>

### Advantages of Scikit-learn
* **Consistent API** — All classes follow the same **fit(), transform(), fit_transform()** pattern making it easy to learn and use.
* **Pipeline Compatibility** — Preprocessing tools can be integrated into sklearn Pipelines, combining preprocessing and model training into a single streamlined workflow.
* **Handles Unseen Data** — Once fitted on training data, the same encoder or scaler can transform new unseen data consistently, which is critical during model deployment.
* **Scalability** — Works efficiently on both small and large datasets without requiring manual coding of transformation logic.
* **Well Documented** — Extensive official documentation and a large community make it easy to learn and troubleshoot.

### API Methods
|Method|Description|
|:---|:---|
|fit(X)|Learns parameters (mean, min, max etc.) from the data|
|transform(X)|Applies the learned transformation to the data|
|fit_transform(X)|Performs fit and transform together in a single step|
|inverse_transform(X)|Reverses the transformation back to original values|


## **REAL-LIFE APPLICATIONS**
* **Healthcare** — Patient vitals like blood pressure, heart rate, and glucose levels are normalized before being input into diagnostic ML models
* **Finance** — Stock prices of different companies are normalized to compare their performance on the same scale
* **Fraud Detection** — Banks use Z-Score standardization to detect unusual transaction amounts that deviate significantly from a customer's normal spending pattern
* **Medical Diagnosis** — Z-scores are used in medical tests like bone density scans to compare a patient's result against the population average
* **Quality Control in Manufacturing** — Industries use Z-scores to identify defective products that fall outside acceptable ranges<br>
## **CONCLUSION**  
* Data normalization and categorical variable transformation techniques were successfully studied using various Python functions and operations.
* The preprocessing techniques and NLP techniques used for analyzing text data were studied successfully.
