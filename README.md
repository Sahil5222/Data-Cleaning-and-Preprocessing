##  Objective
To clean and prepare the raw `marketing_campaign.csv` dataset by handling missing values, duplicates, inconsistent formats, and incorrect data types using Python (Pandas).

---

##  Summary of Data Cleaning Steps

### 1. Load the Dataset
- Loaded the dataset using `pandas.read_csv()` with `sep='\t'` since the file is tab-separated.

### 2. Clean Column Headers
- Converted all column names to lowercase.
- Replaced spaces with underscores for consistency.
  - Example: `'Year_Birth'` → `'year_birth'`.

### 3. Handle Missing Values
- Removed rows with any missing values using `dropna()`.

### 4. Remove Duplicates
- Checked for and dropped any duplicate rows using `drop_duplicates()`.

### 5. Standardize Text Values
- Standardized categorical values in `education` and `marital_status` columns:
  - Trimmed whitespace
  - Applied title case formatting
  - Example: `'graduation '` → `'Graduation'`

### 6. Convert Date Formats
- Converted `dt_customer` column to datetime format using `pd.to_datetime()` with `dayfirst=True`.

### 7. Fix Data Types
- Ensured numerical fields had appropriate types:
  - `income` → float
  - `year_birth` → int

### 8. Save the Cleaned Dataset
- Exported the final cleaned dataset to:
  ```
  cleaned_marketing_campaign.csv
  ```

---

##  Final Output
A cleaned and well-formatted dataset ready for Exploratory Data Analysis (EDA), Modeling, or Dashboarding.

---

##  Tools Used
- Python 3
- Pandas Library
