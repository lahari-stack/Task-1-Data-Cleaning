# Task-1-Data-Cleaning
Data Analyst Internship Task 1 - Data Cleaning and Preprocessing

## Objective:
Clean and prepare a raw dataset by handling missing values, duplicates, inconsistent formats, and ensuring proper data types.

## Dataset Used:
**Customer Personality Analysis** from Kaggle  
[Kaggle Link](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)

---

## Steps Performed:

### 1. Loaded the Dataset
- Used `pandas.read_csv()` to load the CSV file.

### 2. Handled Missing Values
- Used `.isnull().sum()` to identify missing values.
- Filled missing `Income` values with column mean using `fillna()`.

### 3. Removed Duplicates
- Removed duplicate rows using `.drop_duplicates()`.

### 4. Standardized Text Values
- Converted column values like `Education`, `Marital_Status` to lowercase and removed extra spaces.

### 5. Converted Date Formats
- Converted `Dt_Customer` to `datetime` type using `pd.to_datetime()`.

### 6. Renamed Column Headers
- Used `.str.lower().str.replace(" ", "_")` to format column names.

### 7. Checked and Fixed Data Types
- Ensured numerical columns were correct type (e.g., `Income` as `float`, `Kidhome` as `int`).

##  Debug Notes
- Faced a `KeyError: 'Income'` → Solved by checking correct column names with `df.columns`
- `ValueError` when converting date → Used `errors='coerce'` in `pd.to_datetime()`

---

## Tools Used:
- Python 3.10
- Pandas
- Jupyter Notebook
