# <ins>Conditional Statements</ins>
## **AIM**
To study and implement conditional logic, including if, elif, and else statements, in Python to control the flow of program execution. 
## **OBJECTIVES**
* To understand the concept of conditional execution and boolean expressions.
* To perform basic conditional checks using the if statement.
* To apply multi-way branching using elif to handle multiple conditions.
* To implement else blocks to handle default scenarios when no prior conditions are met.
* To understand nested conditional statements and their application in complex decision-making processes.
* To apply comparison and logical operators (e.g., and, or, not) within conditional statements.
* To utilize conditional expressions (ternary operator) for concise assignments. 
## **THEORY**
**Conditional statements** in Python are the **"decision-making" tools** that allow your code to **execute different actions** based on whether a specific **condition is True or False**.
### 1. Fundamental Keywords & Syntax
Python relies on three primary keywords for branching logic: 
* **if:** The entry point. If the condition following it is True, the indented block of code runs.
* **elif:** (short for "else if"): Checks another condition if the previous if was False. You can have multiple elif blocks.
* **else:** The "catch-all" block. It runs only if all preceding if and elif conditions were False. 
* **Key Syntax Rule:** Python uses indentation (usually four spaces) instead of curly braces to define the scope of a code block
### 2. Core Concepts
* **Boolean Evaluation:** Every condition must evaluate to a boolean (True or False). In Python, certain values are "falsy" (evaluated as False), including 0, None, empty strings "", and empty collections like [] or {}.
* **Comparison Operators:** Used to form conditions: == (equal), != (not equal), < (less than), > (greater than), <= (less than or equal), and >= (greater than or equal).
* **Logical Operators:** Used to combine multiple conditions:</br>
**and:** Returns True if both conditions are True.</br>
**or:** Returns True if at least one condition is True.</br>
**not:** Inverts the boolean result.</br>
### 3. Theoretical Differences & Selection Guide
Choosing the right statement depends on the nature of the decision  
|Statement 	|        Core Mechanism	|        Best For...	              |                Key Difference|
 |:--- |:--- |:--- |:--- |
if	    |          Boolean evaluation	   | Simple, single-condition checks	  | Runs only if True; has no fallback.|
if-else     |     	Binary branching	 |Mutually exclusive binary outcomes (e.g., Pass/Fail). |	Guarantees that exactly one of two blocks will run. |
 |if-elif-else	 |Sequential checking	 |Categorizing values into ranges (e.g., Grade A, B, C). |	Stops at the first True condition; more efficient than multiple ifs. |
Ternary |	Conditional  expression |	Simple inline value assignments. |	It is an expression that returns a value, whereas others are statements. |
 |match-case	 |Structural pattern | matching	Complex data structures (lists, dicts) or "switch" logic. |	Matches the shape/structure of data, not just its value.  |
 ### 4. Advanced Structuring
* **Nested Statements:** You can place an if block inside another if block to handle complex, hierarchical decisions.
* **Ternary Operator (Conditional Expression):** A one-line shorthand for simple if-else logic: value_if_true if condition else value_if_false.
* **Match-Case (Structural Pattern Matching):** Introduced in Python 3.10, this acts like a "switch-case" statement, matching a variable against specific patterns for cleaner multi-way branching.
* **The pass Statement:** Because Python code blocks cannot be empty, pass is used as a placeholder when you want to define a branch but haven't written the code for it yet.
 ### 5. Applications in Real-World Software
* **User Authentication & Authorization:** Verifying if a password is correct or if a user has "Admin" rights before showing a dashboard.
* **Business Logic & E-commerce:** Calculating shipping costs based on cart totals or applying tiered discounts for loyal customers.
* **Data Cleaning & AI:** In Data Science, if statements are used to filter outliers, handle missing values, and form the basis of decision tree algorithms.
* **Automation:** Sorting files into folders based on extensions or triggering system alerts if a server’s temperature exceeds a safety threshold.
### 6. Programming Tips
* **Keep conditions simple:** Complex logic should be broken down into multiple lines or helper functions for readability.
* **Use elif for efficiency:** Python stops checking once it finds the first True condition in an if-elif-else ladder, making it faster than a series of independent if statements.
## **CONCLUSION**  
Conditional statements (if, elif, else) in Python efficiently direct program flow by evaluating boolean expressions, making them essential for dynamic decision-making and data manipulation. They enable automation, input validation, and complex logical branching, allowing programs to adapt to varying inputs and scenarios. 
