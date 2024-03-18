# Documentation For Retail Sales Data Pipeline

## Design and Implementation:


## Overview:

The Retail Sales Data Pipeline is designed to automate the process of preprocessing retail sales data and storing it into a MySQL database. This pipeline streamlines the data handling process and facilitates further analysis of retail sales data.


## Assumptions:

1. The Input data is stored in a CSV format in a valid format and at the local computer.
2. The MySQL server is installed and running on the local machine.
3. The MySQL user has the necessary permissions to create a database and tables.
4. The config.ini file is present in the same directory as the code and contains the MySQL username and password in the correct format.


## Dependencies:

1. Python (version: 3.11)
2. pandas
3. sqlalchemy
4. mysql-connector-python


## Functionality:

1. Data Extraction:
    The code reads the CSV file specified by the file_path variable using the pd.read_csv() function from the pandas library.

2. Data Transformation:
    The code checks for missing values in the extracted data using the isnull().sum() method from pandas. It then groups the data by 'product_category_name' and sums the 'total_price' column for each group using the groupby() and sum() methods. The transformed data is stored in a new DataFrame transformed_data with columns 'product_category_name' and 'total_sales'.

3. Database Setup: 
    The code defines a create_database function that creates a new MySQL database if it doesn't already exist. This function uses the mysql.connector library to connect to the MySQL server and execute the SQL query to create the database.

4. Database Connection: 
    The code reads the MySQL username and password from a configuration file (config.ini) using the configparser module. It then creates a connection to the MySQL database using the create_engine function from the sqlalchemy library.

5. Data Loading & Storage: 
    Finally, the code creates a new table named 'product_sales' in the MySQL database and loads the transformed data into it using the to_sql method from pandas.

6. Completion Message:
    Upon successful execution, a completion message is printed.

