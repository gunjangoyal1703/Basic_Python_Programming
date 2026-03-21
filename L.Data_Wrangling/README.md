
# <ins>Data_Wrangling</ins>
## **AIM** </br>
The aim of this experiment is to understand data preprocessing techniques and learn how to identify, handle, and clean missing values in a dataset using Python and the Pandas library.
## **OBJECTIVES** </br>
* To identify missing values using **isna()** and **isnull()** functions.</br>
* To handle missing data through deletion **(dropna())** or imputation using mean, median, and mode.</br>
* To standardize inconsistent text data (e.g., case conversion) and correct data types.</br>
* To export cleaned data into CSV format for further analysis.</br>
## **THEORY** </br>
Data Wrangling is the process of transforming and mapping data from one "raw" data form into another format with the intent of making it more appropriate and valuable for a variety of downstream purposes such as analytics. Key techniques include:</br>

### 1. Handling Missing Data (Null Values)
Missing data is a common occurrence in real-world datasets, often represented as NaN (Not a Number) or NaT (Not a Time). Theory dictates two main strategies:</br>
* **Deletion:** Using **dropna()** to remove rows or columns with missing values. This is preferred when the dataset is large and the missingness is random.</br>
* **Imputation:** Filling in missing values to preserve data volume.</br>
**Mean Imputation:** Best for normally distributed numerical data (e.g., Average Age).</br>
**Median Imputation:** Best for numerical data with outliers, as it is more robust (e.g., Exam Marks).</br>
**Mode Imputation:** Essential for categorical data, where the most frequent occurrence (e.g., AirBag type) fills the gap.</br>
### 2. Data Type Coercion
Raw data often imports as "objects" (strings) even if they represent numbers or dates.</br>
* **Numeric Conversion:** Functions like **pd.to_numeric** with **errors='coerce'** are used to force strings into floats, turning unparseable data into **NaN** for standardized handling.</br>
* **Temporal Standardization:** Converting various date strings into a unified **datetime64** format ensures that time-series analysis can be performed accurately.</br>
### 3. Data Normalization and Consistency
Inconsistent data entry (e.g., "cse" vs. "CSE") can lead to fragmented analysis where one category is treated as two. Theoretical best practice involves:</br>
* **Case Uniformity:** Using **.str.upper()** or **.str.lower()** to ensure categorical strings match perfectly.</br>
* **Placeholder Replacement:** Identifying non-standard nulls (like a dash -) and replacing them with a computer-readable **np.nan**.</br>
### 4. Verification and Validation
The final phase of the theory involves programmatic verification. By using **isna().sum()**, a practitioner confirms that the **"Dirty Data"** has been successfully mitigated before the dataset is exported for final use.</br>

## **DATASET CONTAINS**
* Numerical and categorical columns</br>
* Missing values in different fields</br>
* Real-world structured data for preprocessing practice</br>
* The dataset is used to demonstrate various data cleaning and preprocessing techniq</br>

## **ALGORITHM**
#### 1. **Load Dataset:** Import the raw data using **pd.read_csv()**.</br>
#### 2. **Initial Inspection:** Check for missing values using **.isna().sum()**.</br>
#### 3. **Data Cleaning:**</br>
* Replace placeholder symbols (like "-") with **NaN**.</br>
* Convert object columns to appropriate numeric or datetime types.</br>
#### 4. **Handle Missing Values:**</br>
* Apply **fillna()** using mean for continuous data and mode for categorical data.</br>
* Use **dropna()** if the analysis requires only complete records.</br>
#### 5. **Standardization:** Use string methods like **.str.upper()** to ensure uniform text formatting.</br>
#### 6. **Export:** Save the processed DataFrame to a new CSV file using **.to_csv()**.</br>

## **REAL-LIFE APPLICATIONS**</br>
* **Healthcare Records:** Filling in missing patient biometric data based on average demographic stats to predict health risks.</br>
* **E-commerce:** Standardizing product names and categories from different vendors to create a unified search experience.</br>
* **Finance:** Cleaning transaction history and date formats to detect fraudulent activity patterns across different time zones.</br>
  
## **CONCLUSION**  </br>
By implementing data wrangling techniques, we successfully transformed messy, incomplete datasets into structured, clean formats ready for analysis. The experiment demonstrates that statistical imputation is a powerful tool for retaining data volume while maintaining the integrity of the dataset 
