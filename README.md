**# BrightTV_Viewership_Analytics_Python**
## Metadata Description

**Project Title:** BrightLearn Viewership Analysis  

**Purpose:**  
To explore and understand viewership data collected from the BrightLearn platform. This analysis focuses on identifying trends in user engagement, viewing behavior, and platform performance. It also aims to assess the completeness and consistency of the data before conducting deeper analytical or predictive modeling work.  

---

### Goal
The primary goal of this project is to:
- Evaluate the **quality and structure** of the dataset.  
- Identify **missing values**, **inconsistencies**, and **outliers**.  
- Understand **patterns and relationships** across key metrics.  
- Generate insights that can guide **data cleaning**, **feature engineering**, or **business decisions** related to user engagement.  

---

### Dataset Overview
**Source:**  
Data was loaded from the Spark table:  
`workspace.brightlearn.viewership_analysis`

**Columns:**  
| Column | Description |
|--------|-------------|
| `DateID` | The date of the view in YYYYMMDD format |
| `CustomerID` | Unique identifier for each viewer |
| `TotalTimeWatched` | Total seconds or minutes the user watched a video |
| `Platform` | Device or environment used (e.g., iOS, Leanback, Web) |
| `PlayEventType` | The viewing context (e.g., LiveTV, Catch Up, Other) |
| `VideoTitle` | The title of the video content watched |

---

### Libraries Used
- **pandas:** For working with structured data (tables), performing data cleaning, and running exploratory analysis.  
- **numpy:** For handling numerical computations, statistical summaries, and missing values.  
- **spark (PySpark):** For loading and managing large-scale datasets efficiently before converting them to pandas for analysis.  

---

### Main Tasks

1. **Data Loading:**  
   Load the dataset from the Spark table `workspace.brightlearn.viewership_analysis` and convert it into a pandas DataFrame for easier exploration.

2. **Initial Inspection:**  
   Preview the top few records (`df.head()`) to understand the data’s structure, layout, and column types.

3. **Dataset Overview:*  
   Use `df.info()` to check dataset dimensions, column names, and data types — this helps identify numerical, categorical, and object columns.

4. **Summary Statistics:**  
   Generate descriptive statistics using `df.describe()` to understand key measures such as count, mean, standard deviation, and range for numeric variables.

5. **Missing Value Analysis:**  
   Identify columns with missing data using `df.isnull().sum()` so that they can be handled or imputed appropriately later.

6. **Duplicate Detection:**  
   Check for duplicate rows with `df.duplicated().sum()` and remove them using `df.drop_duplicates()` to ensure data integrity.

7. **Data Preparation for Analysis:**  
   After cleaning (handling missing values and duplicates), prepare the dataset for deeper analysis, visualization, or modeling.

---

### Expected Outcome
By the end of this analysis, the dataset will be:
- **Cleaned:** Missing or inconsistent values addressed.  
- **Structured:** Correct data types and standardized formats.  
- **Understood:** Key patterns, trends, and potential issues identified.  

This will enable smooth progression into **data visualization**, **feature engineering**, or **predictive modeling** phases.

---
