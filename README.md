# Hotel Booking Demand Analysis - Infotact Team 23

## Project Overview
This project, developed by **Infotact Team 23**, focuses on analyzing hotel booking demand using data science techniques. The primary goal is to perform comprehensive data acquisition, cleaning, and feature engineering on a hotel booking dataset to prepare it for further analysis or predictive modeling.

## Project Structure
The project is organized as follows:
- `WEEK1/`: Contains the initial data analysis and preprocessing tasks.
  - `data_preprocessing_and_engineering.ipynb`: Main Jupyter Notebook covering the data pipeline.
  - `hotel_bookings_resort.csv`: The primary dataset (formerly H1.csv).
  - `cleaned_data.csv`: Output of the cleaning and preprocessing steps.

## Analysis Workflow
The analysis is divided into several key stages:

### 1. Data Acquisition
- The dataset (`hotel_bookings_resort.csv`) is loaded using Python's `pandas` library.
- Initial exploration is performed to understand its structure, including column names and data types.

### 2. Data Cleaning
- **Handling NULL Values**: Identified and replaced string-based 'NULL' values with standard `NaN` markers.
- **Deduplication**: Removed duplicate records to ensure data integrity, reducing the dataset size from approximately 40,060 to ~33,968 entries.
- **Standardization**:
  - Trimmed leading/trailing spaces from categorical values.
  - Standardized column names to lowercase and replaced spaces with underscores for easier programmatic access.
- **Type Casting**: Corrected data types for various columns, ensuring dates are properly formatted as `datetime64` and numerical fields are correctly typed.

### 3. Feature Engineering & Transformation
- **Log Transformation**: Applied logarithmic transformation to the `adr` (Average Daily Rate) column to stabilize variance and handle skewness (creating `adr_log`).
- **Date Features**: Extracted relevant components from reservation status dates to enhance temporal analysis capabilities.

### 4. Data Storage
- The final refined and cleaned dataset is exported as `cleaned_data.csv` for use in subsequent analysis or model training steps.

## Technologies Used
- **Python**: Core programming language.
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Seaborn & Matplotlib**: For data visualization (e.g., boxplots for outlier detection).
- **Jupyter Notebook**: For interactive development and documentation.

## How to Run
1. Ensure you have Python installed.
2. Install dependencies: `pip install pandas numpy seaborn matplotlib`.
3. Open the Jupyter Notebook in `WEEK1/` and run the cells sequentially.
