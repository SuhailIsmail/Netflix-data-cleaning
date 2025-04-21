# Netflix-data-cleaning
Netflix Titles Data Cleaning Project: This project involves cleaning and preprocessing a Netflix titles dataset by handling missing values, removing duplicates, standardizing text and date formats, and correcting data types to ensure consistency. The cleaned dataset is ready for analysis or visualization.

# 📊 **Netflix Titles - Data Cleaning Project**

## **Project Description:**

This project involves cleaning and preprocessing a **Netflix Titles** dataset to ensure consistency and readiness for further analysis or visualization. The dataset contains information about Netflix movies and TV shows, including columns like `title`, `country`, `release_year`, `rating`, and `date_added`.

### **Objective:**
The goal of this project was to:
- Handle missing data
- Remove duplicates
- Standardize text and date formats
- Correct data types for various columns
- Prepare the data for analysis and visualization

---

## **Dataset:**

- **Dataset Name**: netflix_titles.csv
- **Data Source**: Available on [Netflix dataset from Kaggle](https://www.kaggle.com/datasets/netflix).
- **Columns in the Dataset**:
  - `show_id`: Unique identifier for each show.
  - `title`: Title of the movie/show.
  - `type`: Type of content (e.g., movie, TV show).
  - `release_year`: Year the movie/show was released.
  - `rating`: Rating assigned to the movie/show.
  - `date_added`: Date when the movie/show was added to Netflix.
  - `duration`: Duration of the movie or TV show (in minutes or seasons).
  - `country`: Country where the content is available.
  - `director`: Director of the movie/show.
  - `cast`: Main cast of the movie/show.

---

## **Steps Performed:**

### 1. **Handled Missing Values**:
   - **`country`, `director`, `cast`**: Filled missing entries with `"Unknown"` where necessary to avoid null values.
   - **`date_added`**: Left null entries unchanged due to the low volume of missing values, preserving the integrity of the dataset.

### 2. **Removed Duplicates**:
   - Removed **12 exact duplicate** rows based on a combination of `show_id`, `title`, and `release_year`, ensuring there were no redundant records.

### 3. **Standardized Text**:
   - Used the `=LOWER()` formula to convert all text values in the `type`, `country`, and `rating` columns to lowercase for consistency.
   - Applied the `=TRIM()` formula to remove unnecessary leading and trailing spaces from the text fields, ensuring uniform formatting.

### 4. **Formatted Dates**:
   - Converted all values in the **`date_added`** column to the **DD-MM-YYYY** format for consistency.
   - Extracted the **year** and **month** from the `date_added` column and placed them into separate columns to facilitate future time-based analysis.

### 5. **Renamed Columns**:
   - Renamed all columns to lowercase with **underscores** to ensure uniformity (e.g., `date_added`, `release_year`), following a consistent naming convention.

### 6. **Fixed Data Types**:
   - Ensured that the `release_year` column was of the correct data type (number).
   - Split the **`duration`** column into two separate columns: 
     - **`duration_value`**: Numeric representation (e.g., 90 for minutes, 2 for seasons).
     - **`duration_unit`**: Unit (e.g., "min" or "seasons").

### 7. **Visualization**:
   - Created a **bar chart** to visualize the distribution of **content types (Movie/TV Show) by rating**. This helped identify which types of content are most common for each rating category.

---

## **Outcome:**

After performing these data cleaning steps, the dataset is now:
- **Free from duplicates**: All duplicate entries have been removed.
- **Missing values handled**: Empty or missing fields have been filled with appropriate values (e.g., `"Unknown"`).
- **Text and date formats standardized**: Ensuring consistency across the dataset.
- **Data types corrected**: Numerical and categorical data are properly formatted for analysis.
- **Ready for further analysis or visualization**: The dataset is clean, standardized, and ready for any further work (e.g., data analysis, model building, etc.).

  
## **📷 Adding a Screenshot to README (Optional)**

  
