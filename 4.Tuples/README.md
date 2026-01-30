# <ins>Tuples</ins>
## **AIM** </br>
To understand Python tuples and perform operations such as creation, indexing,
slicing, and use of built-in functions. </br>
## **OBJECTIVES** </br>
 To understand the concept of tuples in Python </br>
 To study characteristics and advantages of tuples </br>
 To perform indexing and slicing on tuples </br>
 To apply built-in tuple functions </br>
 To understand immutability of tuples </br>
## **THEORY** </br>
### **1. Introduction to Tuples** </br> 
A tuple is an ordered collection of elements in Python, similar to a list, but immutable
in nature. </br>
Tuples are written using parentheses ( ) and elements are separated by
commas. </br>
### **2.Key Characteristics** </br>
**Immutable:** Once created, elements cannot be modified, added, or removed. </br>
**Ordered:** Items maintain their insertion order, which remains constant throughout the tuple's lifetime. </br>
**Heterogeneous:** A single tuple can contain multiple data types, such as integers, strings, and even mutable objects like lists. </br>
**Hashable:** Tuples can be used as keys in dictionaries if all their elements are also immutable. </br>
**Memory Efficient:** Tuples consume less memory than lists because they have a fixed size and do not require overhead for dynamic resizing. </br>
### **3. Essential Syntax** </br>
**Creation:** Use parentheses () or the tuple() constructor. </br>
**Empty Tuple:** t = (). </br>
**Single Item:** Must include a trailing comma (e.g., t = (5,)) or Python will treat it as a standard integer in parentheses. </br>
**Accessing Elements:** Use zero-based indexing tuple[0] or negative indexing tuple[-1] for the last item. </br>
**Slicing:** Retrieve a subset of elements using tuple[start:stop:step]. </br>
**Operators:** </br>
+ for concatenation (creates a new tuple). </br>
* for repetition. </br>
in or not in for membership testing </br>
### **4. Packing and Unpacking** </br>
**Tuple Packing:** Assigning multiple values to a single variable without parentheses (e.g., t = 1, 2, 3). </br>
**Tuple Unpacking:** Extracting values from a tuple directly into variables in a single line.  </br>
**Extended Unpacking:** Use the * operator to capture multiple remaining values into a list.  </br>
### **5. Performance & Use Cases**  </br>
**Speed:** Iterating through a tuple is generally faster than iterating through a list.  </br>
**Data Integrity:** Ideal for fixed data that should not change, such as coordinates (lat, long), database records, or configuration constants.  </br>
**Function Returns:** Commonly used to return multiple values from a single function call.   </br>
### **6. Why Tuples are Used**  </br>
 Faster than lists  </br>
 Data integrity (values cannot be modified)  </br>
 Used for fixed data such as coordinates, days of week, database records  </br>
### **7. Built-in Functions for Tuples**
**len()** **:**              Number of elements </br>
**max()** **:**              Maximum value </br>
**min() :**                Minimum value </br>
**sum() :**                Sum of elements </br>
**count() :**             Count occurrences </br>
**index() :**              Find index of element  </br>
  </br>
## **QUESTIONS**  </br>
### **a. A student’ s exam result is stored in a tuple containing three fixed fields:**
Subject name, marks obtained, and grade.  </br>
Write a Python program to:  </br>
 Store the exam result using a tuple.  </br>
 Unpack the tuple elements into separate variables.   </br>
 Display the subject, marks, and grade.  </br>
 Check whether the student has scored 75 or more marks and print  </br>
“Distinction” if the condition is satisfied.  </br>
### **b. An organization records an employee’ s daily attendance for a week using a tuple,** 
where: </br>
"P" represents Present, 
"A" represents Absent  </br>
Write a Python program to:  </br>
 Store the attendance record in a tuple.  </br>
 Count and display the total number of present days.  </br>
 Count and display the total number of absent days.  </br>
 Check whether the employee was absent at least once  </br>
 during the recorded period and display an appropriate message.   </br>
## **CONCLUSION**  </br>
Thus, Python tuples were studied and operations such as creation, indexing, slicing,
packing, unpacking, and built-in functions were successfully implemented.  </br>




