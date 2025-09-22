# internship-task-1-
Data Cleaning and Preprocessing for Customer Personality Analysis Dataset
## Objective
The main goal of this task was to clean a raw dataset and make it ready for analysis.  
Raw data often has problems like missing values, duplicate rows, inconsistent text, or wrong data types.  
Cleaning data is an important step before doing any analysis or building models.

## Dataset
I used the **Customer Personality Analysis** dataset from Kaggle.  
The dataset contains information about customers, such as:

- Year of birth  
- Education level  
- Marital status  
- Income  
- Number of kids at home  
- Spending on different product categories  
- Responses to marketing campaigns  
- Date of joining as a customer  

This dataset is useful because it has **missing values, inconsistent text, and dates**, which makes it a good dataset for practicing cleaning and preprocessing.

## Steps I Followed

1. **Load the dataset**  
   - I loaded the dataset using Python and Pandas.  
   - Checked the first few rows to understand the data.

2. **Check for missing values**  
   - Some columns, like `Income`, had missing values.  
   - I filled missing values in `Income` with the **median value** because it is better than removing rows.

3. **Remove duplicates**  
   - Checked if any rows were repeated.  
   - Removed duplicates using Pandas.

4. **Standardize categorical text**  
   - `Education` column had values like "2n Cycle", "Graduation", "PhD". I made them simple:  
     - 2n Cycle → Undergraduate  
     - Graduation → Graduate  
     - PhD → Doctorate  
     - Master → Masters  
     - Basic → Basic  
   - `Marital_Status` had unusual values like "Alone", "YOLO", "Absurd". I changed all of them to **Single**.

5. **Convert date column**  
   - `Dt_Customer` column had customer joining dates in string format.  
   - Converted it to **datetime format** to make it usable in analysis.

6. **Rename columns**  
   - Made all column names lowercase and replaced spaces with underscores.  
   - This makes it easier to work with columns in Python.

7. **Fix data types**  
   - Some columns had wrong data types.  
   - Converted `year_birth` to integer and `income` to float.

8. **Save the cleaned dataset**  
   - After all cleaning, saved the dataset as `cleaned_dataset.csv`.

## Files in this Project

- `data_cleaning.ipynb` → Python notebook with all code and steps.  
- `marketing_campaign.csv` → Original raw dataset.  
- `cleaned_dataset.csv` → Final cleaned dataset after preprocessing.  
- `README.md` → This explanation file.

## Tools Used

- **Python** – main programming language  
- **Pandas** – library for data cleaning and analysis  
- **Jupyter Notebook** – to write and run Python code interactively  

## Summary
By completing this task, I learned how to:

- Identify and handle missing values  
- Remove duplicate rows  
- Standardize text columns for consistency  
- Convert dates to proper formats  
- Rename columns and fix data types  

Now the dataset is **clean, organized, and ready for analysis or modeling**.
