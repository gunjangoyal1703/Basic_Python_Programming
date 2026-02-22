# <ins>Sets and Dictionaries</ins>
## **AIM**
To study and implement set data structure in Python and perform various set and Dictionary operations.</br>
## **OBJECTIVES**
•	To understand the concept of sets</br>
•	To perform set creation and basic operations</br>
•	To apply mathematical set operations</br>
•	To understand dictionary structure</br>
•	To perform insertion, deletion, and access of data</br>
•	To apply dictionary methods</br>
## **THEORY**
### **# SETS**
A set in Python is an unordered collection of unique elements.
Sets are defined using curly braces {} or the set() constructor.</br>
### 1. Characteristics 
**Unordered:** Elements have no fixed position; they cannot be accessed by index.</br>
**Unique:** Duplicate values are automatically removed during creation or when adding new items.</br>
**Mutable:** You can add or remove elements after creation, but the elements themselves must be immutable (like strings, numbers, or tuples).</br>
**Hashing:** Internally, Python uses hash tables to store sets, making membership tests (in operator) extremely fast.</br>
### 2. Operations on Sets
<pre>
<ins>Operation</ins> 	              <ins>Operator</ins>	       <ins>Method</ins>	                       <ins>Description</ins>
Union	                     |	           union()	             Elements present in either or both sets.
Intersection	             &	        intersection()	         Elements present in both sets.
Difference	                 -	        difference()     	     Elements in the first set but not the second.
Symmetric Difference	     ^	    symmetric_difference()	     Elements in exactly one set, but not both.</pre>
### 3. Modification Methods
**add(element):** Adds a single item.</br>
**update(iterable):** Adds multiple items from another collection.</br>
**remove(element):** Deletes an item; raises a KeyError if not found.</br>
**discard(element):** Deletes an item; does not raise an error if not found.</br>
**pop():** Removes and returns an arbitrary element.</br>
### 4. Frozen Sets
A frozen set is an immutable version of a set. Once created, it cannot be modified (no add or remove). Because they are immutable, they are hashable and can be used as keys in a dictionary or as elements in another set. </br>
### 5. Applications of Sets
* Algorithm Optimization</br>
* Data Cleaning and Deduplication</br>
* Efficient Membership Testing</br>
* Mathematical Data Analysis</br>
* Database Management</br>

### **# DICTIONARIES**</br>
A dictionary is an unordered collection of key-value pairs.
Each key must be unique, while values may be duplicated.</br>
### 1. Characteristics</br>
**Unique & Immutable Keys:** Keys must be unique to prevent overwriting. They must also be hashable, meaning they must be immutable types like strings, numbers, or tuples.</br>
**Mutable Values:** Values can be any Python object, including lists or other dictionaries, and can be modified after creation.</br>
**Ordered:** Modern Python dictionaries preserve insertion order, meaning they remember the sequence in which items were added.</br>
**Key-Based Access:** Instead of using numeric indices (like lists), dictionaries use keys to retrieve value</br>
### 2. Internal Implementation</br>
**Hashing:** When a key is inserted, Python applies a hash function to generate a unique integer hash.</br>
**Indexing:**This hash is used to determine a specific "bucket" or index in an internal array where the value is stored.</br>
**Collision Handling:** If two different keys produce the same hash (hash collision), Python uses a technique called open addressing (specifically pseudo-random probing) to find the next available slot.</br>
### 3. Key Methods</br>
**get(key, default):** Safely retrieves a value; returns a default value instead of raising a KeyError if the key is missing.</br>
**items(), keys(), values():** Return dynamic view objects that reflect the dictionary's current state.</br>
**update():** Merges another dictionary or iterable into the existing one.</br>
### 4. Applications</br>
* JSON & Web Development</br>
* Caching & Memoization</br>
* Data Analysis & Frequency Counting</br>
* Mapping & Switch-Case Logic</br>
* Representing Complex Objects</br>
 
## **CONCLUSION**  
Sets efficiently handle unique data and support mathematical operations, making them useful for data processing tasks.
Dictionaries provide efficient storage and retrieval of data using keys, making them essential for real-world applications.







