<textarea>
# Data Processing and Merging for Retail Analytics Project

This project focuses on data cleaning, preprocessing, and merging multiple datasets related to customer sales, products, stores, and exchange rates. The final goal is to create a comprehensive dataset for analysis in the retail electronics domain.

## Project Structure

The project consists of several steps including data cleaning, data type conversion, merging, and normalization of column names.

## Files

- `normalized_customer.csv`: Contains cleaned and normalized customer data.
- `Exchange_Rates.csv`: Contains exchange rates with respective dates.
- `Products.csv`: Contains details about products including price and cost.
- `Sales.csv`: Contains sales transactions with various details like order date, product key, etc.
- `Updated_stores.csv`: Contains store details including the date they were opened.
- `merged_Data_final5.csv`: The final merged dataset before column name normalization.
- `companyrecord.csv`: The final processed dataset with normalized column names.

## Setup

### Prerequisites

Ensure you have Python installed along with the following packages:
- `pandas`

You can install the required package using pip:

```bash
pip install pandas
Data Preparation
Place all the CSV files (normalized_customer.csv, Exchange_Rates.csv, Products.csv, Sales.csv, Updated_stores.csv) in the D:/project 2/ directory.

Running the Script
Download and place the script in your working directory.
Run the script using Python:
bash
Copy code
python script_name.py
Replace script_name.py with the name of your script file.

Output Files
Updated_Customers1.csv: Cleaned customer data.
Exchange_Rates_final.csv: Cleaned exchange rates data.
Products_final.csv: Cleaned products data with updated column names.
sales_final1.csv: Cleaned sales data with removed Delivery Date column.
Stores_final.csv: Cleaned stores data.
merged_Data_final5.csv: Final merged dataset.
companyrecord.csv: Final dataset with normalized column names.
Code Explanation
The script performs the following steps:

Load and Clean Customer Data:

Handle missing values.
Convert 'Birthday' to datetime format.
Save the cleaned data.
Load and Clean Exchange Rates Data:

Convert 'Date' to datetime format.
Convert 'Exchange' to numeric format.
Save the cleaned data.
Load and Clean Products Data:

Rename 'Unit Price USD' to 'Unit_sale_USD'.
Clean and convert 'Unit Cost USD' and 'Unit_sale_USD' to float.
Save the cleaned data.
Load and Clean Sales Data:

Check for missing values.
Drop the 'Delivery Date' column.
Convert 'Order Date' to datetime format.
Save the cleaned data.
Load and Clean Stores Data:

Convert 'Open Date' to datetime format.
Save the cleaned data.
Merge Data:

Merge Sales and Customers data on CustomerKey.
Merge the resulting dataset with Products data on ProductKey.
Merge the resulting dataset with Stores data on StoreKey.
Filter out rows with missing 'Order Date'.
Merge the filtered dataset with Exchange Rates data on Currency Code and Order Date.
Drop the redundant 'Date' column.
Normalize Column Names:

Replace spaces in column names with underscores.
Save the final dataset.
Conclusion
This script automates the process of cleaning and merging datasets to prepare a comprehensive dataset for retail analytics. The final dataset is saved as companyrecord.csv and can be used for further analysis.
