# <ins>asic Charts & Visual Encoding</ins>
## **AIM**
To implement and analyze various data visualization techniques using Matplotlib and Seaborn libraries in Python to represent different types of datasets effectively.
## OBJECTIVE
* To understand the fundamental principles of visual encoding (marks, colors, and markers).</br>
* To master the creation of basic charts such as Line, Bar, Histogram, and Scatter plots.</br>
* To explore advanced statistical visualizations including Violin plots, Heatmaps, and FacetGrids.</br>
* To develop a multi-chart dashboard for comprehensive data analysis.</br>
## THEORY
### 1. Principles of Visual Encoding
Visual encoding is the process of mapping data values to graphical properties (aesthetics). In this experiment, you used:
* Marks: The basic geometric elements like Points (Scatter plots), Lines (Line charts), and Areas (Bar charts/Histograms).
* Channels: Characteristics that control the appearance of marks, such as Position (x and y coordinates), Color (to distinguish categories like 'Food' or 'Electronics'), and * Shape/Markers (using stars, squares, or circles to differentiate data series).
### 2. Libraries Used
* Matplotlib: The foundation for plotting in Python. It offers granular control over every figure element (axes, labels, titles). It is best for "pixel-perfect" plots and custom layouts.
* Seaborn: A statistical data visualization library. It is "dataset-oriented," meaning it works seamlessly with Pandas DataFrames and provides sophisticated defaults for complex plots like Violin plots (showing distribution density) and Heatmaps (showing correlation).
### 3. Key Chart Types and Their Utility
* **Line Chart:** Best for showing trends over time or ordered categories.
* **Bar Chart:** Ideal for comparing discrete quantities across categories.
* **Histogram:** Used to visualize the frequency distribution of a single numerical variable.
* **Scatter Plot:** Primary tool for identifying correlations or relationships between two variables.
* **KDE (Kernel Density Estimation):** A way to visualize the probability density of a continuous variable, creating a "smooth" version of a histogram.
## ALGORITHM
To replicate the visualizations found in your journal, you can follow this structured logic:
#### 1.Start.
#### 2.Environment Setup: Import essential libraries: matplotlib.pyplot, seaborn, pandas, and numpy. (p. 1)
#### 3.Data Acquisition:
#### 4.Define the data using a dictionary (e.g., Student Marks or Sales Data).
#### 5.Convert the dictionary into a Pandas DataFrame for structured handling. (pp. 1, 13)
#### 6.Data Pre-processing:
Perform aggregations (like .mean() or .sum()) if the chart requires summary statistics (e.g., mean sales by region). (pp. 34-35)
#### 7.Visualization Selection:
* For Trends: Invoke plt.plot() or sns.lineplot().
* For Comparisons: Invoke plt.bar() or sns.barplot().
* For Distributions: Invoke plt.hist(), sns.histplot(), or sns.violinplot().
* For Relationships: Invoke plt.scatter(), sns.scatterplot(), or sns.heatmap().
#### 8.Visual Styling:
* Assign Colors and Markers to differentiate categories.
* Apply Conditional Formatting (e.g., different colors for 'Pass' vs 'Fail'). (p. 10)
#### 9.Plot Enhancement:
* Add Titles, X-axis labels, and Y-axis labels.
* Include a Legend if multiple data series are present.
* Enable Grid lines for better readability. (pp. 6, 17)
#### 10.Output Generation: Call plt.show() to render the visual on the screen.
#### 11.End.

## APPLICATIONS
* **Academic Performance Tracking:** Visualizing study hours vs. marks to find correlations.</br>
* **Business Intelligence:** Analyzing sales performance and profit trends across different regions and product categories.</br>
* **Statistical Analysis:** Using histograms and box plots to understand the distribution and spread of data, such as profit or student marks.</br>
* **Relationship Mapping:** Identifying correlations between multiple numerical variables (Sales, Profit, Customers, Rating) using heatmaps.</br>
## CONCLUSION
Through this experiment, various charts were successfully implemented to visualize three distinct datasets (p. 36). It was observed that while simple charts like Line and Bar plots are excellent for trends and comparisons, advanced tools like Heatmaps and Violin plots provide deeper insights into data distributions and correlations. The ability to combine multiple visualizations into a single dashboard significantly enhances the capability to perform holistic data storytelling and decision-making 
