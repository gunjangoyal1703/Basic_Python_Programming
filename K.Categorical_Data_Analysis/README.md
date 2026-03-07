
# <ins>Categorical Data Analysis</ins>
## **AIM** </br>
To perform categorical data analysis on structured datasets using Python's pandas library to derive meaningful insights through frequency counts, cross-tabulations, and data grouping.

## **OBJECTIVES** </br>
* To understand the handling of non-numerical (categorical) data in Python.</br>
* To implement various statistical functions such as **value_counts()** and **crosstab()**.</br>
* To filter and sort data based on specific categorical attributes.</br>
* To analyze relationships between different categories (e.g., Department vs. Grade).</br>

## **THEORY** </br>
Categorical Data Analysis involves the study of variables that represent distinct groups or categories rather than continuous measurements. In Python, the pandas library is the primary tool for this analysis.</br>
* **Frequency Distribution:** Uses <ins>value_counts()</ins> to find how often each category occurs.</br>
* **Cross-Tabulation:** Uses <ins>pd.crosstab()</ins> to compute a simple frequency table of two or more factors, showing the relationship between variables.</br>
* **Normalization:** Scaling data to a range (like 0-100) to find percentage distributions.</br>

### <ins>**Logic for Key Tasks**</ins>
|No.	|Task	|Logic|
|:---|:---|:---|
|1|	Frequency Count|	Select the target column → Apply .value_counts() → Output the number of occurrences for each unique label. |
|2|	Cross-Tabulation|	Identify two categorical columns → Use pd.crosstab(column1, column2) → Generate a matrix of counts. |
|3|	Percentage Dist.	|Apply .value_counts(normalize=True) → Multiply by 100 → Return the relative frequency in %. |
|4|	Data Filtering|	Define a condition (e.g., Category == 'Electronics') → Apply condition as an index to the DataFrame → Return matching rows.| 
|5|	Data Grouping	|Group by a specific column → Perform an aggregate or count function on a sub-column → View hierarchical results.| 

### <ins>**Applications**</ins>
#### A. E-Commerce & Retail Analytics</br>
* **Payment Gateway Optimization:** By using pd.crosstab(df['Category'], df['Payment_Method']), retailers can identify which payment methods are most popular for specific product types. For example, if "Electronics" are predominantly bought via "UPI," the company can partner with UPI providers for targeted cashback offers.</br>
* **Logistics & Supply Chain:** Analyzing Delivery_Type vs. Customer_Type helps in warehouse management. If "Returning Customers" consistently choose "Express Delivery," the company can prioritize their orders in the fulfillment centers to maintain loyalty.</br>
* **Inventory Categorization:** Using value_counts() on product categories allows managers to see which departments (Clothing vs. Grocery) have the highest turnover, helping them decide where to allocate more shelf space or digital advertising spend.</br>
#### B. Educational Institutions & Academic Research</br>
* **Performance Benchmarking:** By performing a Gender Vs Grade Analysis, educators can identify if there are significant performance gaps between different demographics. This data-driven approach allows for the implementation of specialized bridge programs where needed.</br>
* **Departmental Resource Allocation:** Using Department.value_counts() helps university administrators understand student density. A department with 20 students (like CSE in the dataset) might require more lab equipment or faculty members compared to a department with 11 (like ECE).</br>
* **Curriculum Effectiveness:** Cross-tabulating Department vs. Grade reveals if certain subjects are "scoring" or "difficult." If the "Mechanical" department has 0 'A' grades, it might signal a need to review the curriculum or the examination pattern.</br>
#### C. Healthcare & Medical Studies</br>
* **Patient Demographic Analysis:** Hospitals use categorical analysis to track the number of patients in different age groups or genders across various departments (Cardiology, Orthopedics, etc.).</br>
* **Treatment Effectiveness:** Researchers use cross-tabulation to compare "Treatment Type" against "Recovery Status" (Recovered, Improving, No Change) to determine which medicine or procedure is most effective for a specific group.
D. Human Resources & Corporate Management</br>
* **Diversity and Inclusion (D&I) Metrics:** As shown in the Department Vs Gender analysis in the experiment, HR departments use these tools to ensure a balanced gender ratio across all technical and non-technical wings of an organization.
* **Employee Retention:** Categorical grouping can be used to analyze "Resignation Reasons" across different "Experience Levels," helping companies build better retention strategies for mid-level vs. entry-level employees.</br>
#### E. Marketing & Customer Relationship Management (CRM)</br>
* **Market Segmentation:** By filtering data (e.g., df[df['Customer_Type'] == 'New']), marketing teams can create personalized email campaigns. A "New" customer might receive a "Welcome Discount," while a "Returning" customer receives a "Loyalty Reward."</br>
* **Trend Analysis:** Using value_counts(normalize=True) over different months allows brands to see if their market share is growing or shrinking relative to competitors.</br>


## **Algorithms**
### **Program 1: Frequency Distribution of Product Categories**</br>
  * **Logic:** Access the 'Category' column of the DataFrame and apply the value_counts() method.</br>
  * **Algorithm:**</br>
Load the dataset into df.</br>
Identify the target categorical column ('Category').</br>
Invoke df['Category'].value_counts().</br>
Display the resulting counts (e.g., Electronics: 4, Clothing: 3, Grocery: 3) (p. 2).</br>
### **Program 2: Multi-Variable Cross-Tabulation (Payment vs. Category)**</br>
* **Logic:** Create a contingency table to see which payment methods are favored by which product categories.</br>
* **Algorithm:**</br>
Select two columns: 'Category' and 'Payment_Method'.</br>
Pass them into the pd.crosstab() function.</br>
Generate a matrix where rows are categories and columns are payment types.</br>
Result shows Electronics is 100% UPI-based in this sample.</br>
### **Program 3: Percentage Distribution of Student Grades**</br>
* **Logic:** Determine what portion of the total student body falls into each grade bracket.</br>
* **Algorithm:**</br>
Select the 'Grade' column from the second dataset.</br>
Use value_counts(normalize=True).</br>
Multiply the result by 100.</br>
** **Result:** Grade B (40.0%), Grade A (36.67%), Grade C (23.33%) .</br>
### **Program 4: Conditional Data Filtering (Electronics Orders)**</br>
* **Logic:** Isolate a specific segment of the data for deep-dive analysis.</br>
* **Algorithm:**</br>
Define the mask: df['Category'] == 'Electronics'.</br>
Pass this mask into the DataFrame index: df[mask].</br>
Return only the rows where the category matches the criteria.</br>
### **Program 5: Hierarchical Grouping (Departmental Student Lists)**</br>
* **Logic:** Organise the entire dataset based on one primary category to view sub-details.</br>
* **Algorithm:**</br>
Invoke df.groupby('Department').</br>
Apply .value_counts() to the grouped object.</br>
Display a nested list of students, their gender, and grades, sorted by their respective departments </br>

## **CONCLUSION**  </br>
The experiment provided hands-on experience in handling categorical data using Python. </br>
Key takeaways include the ability to quickly summarize large datasets using value_counts and the power of crosstab in revealing hidden relationships between variables. For instance, the data revealed that standard delivery is predominantly used by new customers, while returning customers favor express delivery. </br>
Such insights are vital for data-driven decision-making in any technical or business environment.</br>


