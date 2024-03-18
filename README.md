# README for Retail Sales Data Pipeline


This repository contains a Python script that implements a data pipeline to extract data from a CSV file, transform the data by grouping it by product category and calculating the total sales for each category, and then load the transformed data into a MySQL database.


## Prerequisites

1. Python 3.11
2. pandas
3. sqlalchemy
4. mysql-connector-python
5. configparser


## Installation

1. Install the required dependencies:
    pip install pandas sqlalchemy mysql-connector-python configparser

2. Create a 'config.ini' file in the same directory as the Python script with the following content:
    [mysql]
user = your_mysql_username
password = your_mysql_password

Replace 'your_mysql_username' and 'your_mysql_password' with your actual MySQL username and password.


## Usage

1. Save the CSV file containing the sales data in the desired location.
2. Update the 'file_path' variable in the Python script with the correct path to the CSV file.
3. Run the Python script:
    python 'data_pipeline.ipynb' [your_python_file]
4. The extracted dataset will be displayed in the console or Jupyter Notebook.
5. The transformed dataset, with total sales calculated for each product category, will also be displayed.
6. The transformed data will be loaded into a new table named 'product_sales' in the 'Sales_prices' database (or an existing database with the same name).


## File Structure

1. 'data_pipeline.ipynb'[your_python_file]: Python script containing the data pipeline implementation.
2. 'README.md': This file.


## Dependencies

1. pandas
2. sqlalchemy
3. mysql-connector-python
4. configparser


## Documentation

The 'data_pipeline.ipynb'[your_python_file] script contains detailed step-by-step explanations for each part of the data pipeline implementation, including assumptions and design decisions.
