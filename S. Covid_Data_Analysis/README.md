# 🦠 COVID-19 Data Analysis 
 

 
---
 
| 📂 **Dataset**  |`covid_19_data.csv` (Jan 2020 – May 2021) |
|---|---|
| 🛠️ **Tools Used** | 1. Python</br> 2. Pandas </br>3. NumPy </br>4. Plotly </br>5. Express |
 
---
 
## 📋 Table of Contents
 
1. [Objectives](#1-objectives)
2. [Dataset Description](#2-dataset-description)
3. [Tools and Technologies Used](#3-tools-and-technologies-used)
4. [Methodology](#4-methodology)
5. [Analysis and Visualisations](#5-analysis-and-visualisations)
6. [Key Insights](#6-key-insights)
 
---
 
## 1. Objectives
 
The primary objectives of this project are:
 
- ✅ To load, clean, and preprocess the global COVID-19 dataset for analysis.
- ✅ To derive meaningful metrics such as **Active Cases** from raw Confirmed, Deaths, and Recovered counts.
- ✅ To explore the dataset and understand its structure, data types, and missing values.
- ✅ To aggregate COVID-19 statistics at the country level and identify the most affected regions.
- ✅ To analyse **Spain's** COVID-19 situation in depth, including a regional (province-level) breakdown.
- ✅ To create interactive **choropleth map visualisations** using Plotly to communicate insights effectively.
- ✅ To identify the **top 20 most affected countries** globally by confirmed case count.
 
---
 
## 2. Dataset Description
 
The dataset used in this project is `covid_19_data.csv`, a publicly available COVID-19 tracking dataset. It contains daily-level observations across countries and provinces from **22 January 2020 to 29 May 2021**.
 
### 📊 Dataset Overview
 
| Attribute | Details |
|---|---|
| File Name | `covid_19_data.csv` |
| Total Records | 306,429 rows |
| Date Range | January 22, 2020 – May 29, 2021 |
| Countries / Regions | 195 unique countries |
| Provinces / States | 228,326 non-null entries |
| File Size (in-memory) | ~14.0 MB |
 
### 🗂️ Column Descriptions
 
| Column | Data Type | Description |
|---|---|---|
| `ObservationDate` | `datetime64[ns]` | Date of the observation record |
| `Province/State` | `object` (string) | Sub-national region (may be `NaN` for country-level rows) |
| `Country/Region` | `object` (string) | Name of the country or region |
| `Confirmed` | `int64` | Cumulative confirmed COVID-19 cases |
| `Deaths` | `int64` | Cumulative COVID-19 deaths |
| `Recovered` | `int64` | Cumulative recovered cases |
| `Active` *(derived)* | `int64` | `Confirmed − Deaths − Recovered` |
 
> **Note:** The `SNo` (serial number) and `Last Update` columns were dropped during preprocessing as they did not contribute to the analysis.
 
---
 
## 3. Tools and Technologies Used
 
| Tool / Library | Version / Type | Purpose |
|---|---|---|
| Python | 3.x | Core programming language |
| Pandas | Latest | Data loading, cleaning, transformation, and grouping |
| NumPy | Latest | Numerical operations and type conversions |
| Plotly Express | Latest | Interactive choropleth map visualisations |
| Plotly Graph Objects | Latest | Low-level figure customisation |
| Google Colab / Jupyter | Notebook IDE | Development and execution environment |
| CSV (`covid_19_data.csv`) | Flat file | Source dataset |
 
---
 
## 4. Methodology
 
### 4.1 Data Loading
 
The dataset was loaded using `pd.read_csv()` into a Pandas DataFrame. An initial inspection was done using `data.head()` and `data.tail()` to confirm successful loading.
 
```python
import pandas as pd
import numpy as np
 
data = pd.read_csv("/content/covid_19_data.csv")
data.head()
```
 
### 4.2 Data Cleaning & Preprocessing
 
- Dropped irrelevant columns: `SNo` and `Last Update` (`axis=1`).
- Converted `ObservationDate` from `object` dtype to `datetime64[ns]` for time-based operations.
- Cast `Confirmed`, `Deaths`, and `Recovered` from `float64` to `int64` to remove unnecessary decimal points.
- Validated data types using `data.info()` after each transformation.
 
```python
data = data.drop(['SNo', 'Last Update'], axis=1)
 
data['ObservationDate'] = data['ObservationDate'].astype('datetime64[ns]')
data['Confirmed']       = data['Confirmed'].astype('int64')
data['Deaths']          = data['Deaths'].astype('int64')
data['Recovered']       = data['Recovered'].astype('int64')
```
 
### 4.3 Feature Engineering
 
A new column, `Active`, was derived as:
 
```
Active = Confirmed − Recovered − Deaths
```
 
```python
data['Active'] = data['Confirmed'] - data['Recovered'] - data['Deaths']
```
 
This metric represents the number of people who are **currently infected** (neither recovered nor deceased).
 
### 4.4 Latest Data Extraction
 
The maximum date in the dataset (`2021-05-29`) was identified using `data['ObservationDate'].max()`. A subset, `latest_data`, was created by filtering only rows matching this date — producing **765 rows** spanning **195 unique countries**.
 
```python
latest_data = data[data['ObservationDate'] == data['ObservationDate'].max()]
```
 
### 4.5 Country-Level Aggregation
 
`latest_data` was grouped by `Country/Region` and aggregated (sum) to produce a `countries` DataFrame with total **Confirmed**, **Deaths**, and **Active** cases per country.
 
```python
countries = latest_data.groupby("Country/Region")[["Confirmed", "Deaths", "Active"]].sum()
countries = countries.reset_index()
```
 
### 4.6 Spain-Specific Analysis
 
- Filtered all records where `Country/Region == 'Spain'` to create a `spain` DataFrame (**7,718 rows**).
- Identified **20 unique provinces/states**, with **Andalusia** appearing most frequently (mode).
- Extracted Spain's latest date snapshot to analyse regional distribution.
- Ranked provinces by Confirmed cases and identified **Madrid** as the most affected region (714,616 cases).
 
```python
spain = data[data['Country/Region'] == 'Spain'].copy()
spain_latest_data = spain[spain['ObservationDate'] == spain['ObservationDate'].max()]
```
 
### 4.7 Visualisation
 
- Plotted a **global choropleth map** using `px.choropleth()` with a `YlGnBu` colour scale to show Confirmed cases by country.
- Created a **Spain-specific choropleth** using the `Magma` colour scale to highlight Spain's case count on the world map.
 
```python
import plotly.express as px
 
world_map = px.choropleth(countries, locations="Country/Region", locationmode="country names",
                          color="Confirmed", color_continuous_scale="YlGnBu")
world_map.show()
```
 
---
 
## 5. Analysis and Visualisations
 
### 5.1 Global Country-Level Statistics *(as of 2021-05-29)*
 
Top 10 countries by Confirmed cases:
 
| Rank | Country | Confirmed | Recovered |
|:---:|---|---:|---:|
| 🥇 1 | United States | 33,251,939 | 0 *(not reported)* |
| 🥈 2 | India | 27,894,800 | 25,454,320 |
| 🥉 3 | Brazil | 16,471,600 | 14,496,224 |
| 4 | France | 5,719,877 | 390,878 |
| 5 | Turkey | 5,235,978 | 5,094,279 |
| 6 | Russia | 4,995,613 | 4,616,422 |
| 7 | United Kingdom | 4,496,823 | 15,481 |
| 8 | Italy | 4,213,055 | 3,845,087 |
| 9 | Argentina | 3,732,263 | 3,288,467 |
| 10 | Germany | 3,684,672 | 3,479,700 |
 
### 5.2 Selected Country Statistics
 
| Country | Confirmed | Deaths | Active |
|---|---:|---:|---:|
| Mainland China | 91,072 | 4,636 | 319 |
| India | 27,894,800 | 325,972 | 2,114,508 |
| Spain | 3,668,658 | 79,905 | 3,438,377 |
| Germany | 3,684,672 | 88,413 | 116,559 |
 
### 5.3 Spain Regional Analysis *(Province-Level)*
 
| Province / State | Confirmed | Deaths | Recovered |
|---|---:|---:|---:|
| **Madrid** | **714,616** | 15,285 | 40,736 |
| Catalonia | 611,008 | 14,531 | 26,203 |
| Andalusia | 581,880 | 9,880 | 10,671 |
| C. Valenciana | 394,360 | 7,389 | 9,970 |
| Castilla y Leon | 230,600 | 6,882 | 8,716 |
| Pais Vasco | 197,812 | 4,429 | 16,160 |
| Castilla - La Mancha | 192,347 | 5,912 | 6,392 |
| Galicia | 126,622 | 2,402 | 9,204 |
 
> Madrid had the highest number of confirmed cases (**714,616**), followed by Catalonia (611,008) and Andalusia (581,880).
 
### 5.4 Visualisations Produced
 
| Map | Colour Scale | Description |
|---|---|---|
| 🌍 World Choropleth | `YlGnBu` | Darker shades = higher confirmed cases. USA, India & Brazil appear darkest. |
| 🇪🇸 Spain Choropleth | `Magma` | Highlights Spain's ~3.67 million cumulative confirmed cases on the world map. |
 
---
 
## 6. Key Insights
 
- 📅 The dataset spans **16 months** (Jan 2020 – May 2021) with **306,429 records** from **195 countries** — a highly comprehensive global dataset.
- 🇺🇸 As of 29 May 2021, the **United States** had the highest confirmed cases globally (**33.25 million**), more than 5 million ahead of second-place India.
- 🇮🇳 **India** showed the highest Active case count (**2.11 million**), reflecting the severe second wave during mid-2021.
- 🇨🇳 **Mainland China**, where the pandemic originated, had a relatively low final count of **91,072 confirmed** and only **319 active** cases — suggesting effective containment.
- 🇪🇸 **Spain**, with 3.67 million confirmed cases, was the 11th most affected country. **Madrid** alone accounted for ~19.5% of Spain's total cases.
- 🔢 The `Active = Confirmed − Deaths − Recovered` formula is a useful derived metric, though it depends on consistent recovery reporting across countries.
- 🇷🇺 **Russia** had the most entries in `latest_data` (83 rows), likely due to sub-national reporting, followed by the US (58) and Japan (49).
- ❓ The `Province/State` column had **78,103 missing values** (~25.5% of records) — typical for countries that report only at the national level.
 
---
 
## 7. Summary / Conclusion
 
This project successfully demonstrated **end-to-end COVID-19 data analysis** using Python's data science ecosystem. Starting from raw CSV data, the workflow covered:
 
- Data loading and inspection
- Type coercion and cleaning
- Feature engineering (`Active` cases)
- Group-level country aggregation
- Country-specific deep dives (Spain)
- Interactive geo-visualisation with Plotly
 
The analysis confirmed that the pandemic's impact was **highly unequal** across countries, with the United States, India, and Brazil bearing the heaviest burden. At the sub-national level, **Madrid** emerged as Spain's most affected region by a significant margin.
 
The use of **Plotly choropleth maps** allowed for intuitive, interactive exploration of geographic patterns. The derived `Active Cases` column provided a more meaningful measure of ongoing disease burden than raw confirmed counts alone.
 
> Overall, the project highlights the power of data-driven analysis in understanding and communicating public health emergencies.
 
---
 

