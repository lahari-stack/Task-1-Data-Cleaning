# Interview Questions – Task 1: Data Cleaning


**1. What are missing values and how do you handle them?**  
Missing values are empty or NaN entries in a dataset. They are handled by either:
- Removing them (`dropna()`)
- Filling them (`fillna()`) using mean, median, or custom logic.


**2. How do you treat duplicate records?**  
Use `.drop_duplicates()` in Pandas to remove rows that appear more than once.



**3. Difference between `dropna()` and `fillna()` in Pandas?**  
- `dropna()` removes rows/columns with missing values.
- `fillna()` replaces missing values with a specified value (like 0, mean, etc).



**4. What is outlier treatment and why is it important?**  
Outliers are unusually high or low values. They can skew analysis and models. Treatment methods include:
- IQR method
- Z-score method
- Capping/extreme value replacement


**5. Explain the process of standardizing data.**  
Standardization ensures consistency in formatting:
- Text: lowercase, strip spaces
- Dates: consistent format (e.g., YYYY-MM-DD)
- Columns: clean naming, no special characters



**6. How do you handle inconsistent data formats (e.g., date/time)?**  
Use parsing functions like `pd.to_datetime()` with proper formats, and clean string-based fields with `.str.strip()` and `.str.lower()`.



**7. What are common data cleaning challenges?**  
- Missing or incorrect data
- Inconsistent formatting
- Duplicates
- Mixed data types
- Typos in categorical values



**8. How can you check data quality?**  
- `.info()` for data types and non-null counts
- `.isnull().sum()` for missing values
- `.describe()` for statistical summary
- Checking for duplicates and inconsistencies

