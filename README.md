# Sales Vision

## About
**Sales Vision** aims to offer a clear and detailed understanding of sales patterns, customer behavior, and product performance based on past data.

## Description
- **Loading Data**: Load past data from CSV files into the project environment.
- **Processing and Cleaning Data**:
  - Check for null values and handle them appropriately.
  - Remove outliers using standardization methods.
  - Ensure data is compatible with MySQL by typecasting as needed.
- **Storing Data**: Store the cleaned and processed data in a structured format within a MySQL repository.
- **Identifying Patterns and Trends**: Analyze the data to uncover patterns and generate insights.

## Installation

### Required Software
- **IDE**: Jupyter Notebook
- **Database**: MySQL (Download from [here](https://www.mysql.com/))

### Python Packages
- **Pandas**: Install with `!pip install pandas`
- **Numpy**: Install with `!pip install numpy`
- **MySQL Connector**: Install with `!pip install mysql-connector-python`

## Importing and Cleaning Data

### Importing Data
- Use `pandas` to create data frames from CSV files.
- Use `numpy` for data typecasting if necessary.
- Use `mysql.connector` to establish a connection with MySQL.

### Cleaning Data
1. Check for null values and fill them with front values if necessary.
2. Drop rows if they do not affect the overall data characteristics.
3. Remove outliers in numeric columns (e.g., price, number of orders, quantity) using standardization methods.

### Processing Data
1. Typecast data using `numpy` (e.g., convert `int32`/`int64` to `int` for MySQL compatibility).
2. Convert float types to ensure compatibility with MySQL.
3. Adjust datetime formats to ensure MySQL compatibility.
4. Remove special characters if present.

## Saving Data

### MySQL Database Setup
- Establish a connection with MySQL using `mysql.connector`.
- Create the database `mde92` with the following tables:
  - **customers**: `customer_id`, `customer_key`, `gender`, `name`, `city`, `state_code`, `state`, `zip_code`, `country`, `continent`, `birthday`.
  - **exchange_rates**: `Erid`, `ExchangeDate`, `currency`, `ExchangeRate`.
  - **products**: `ProductKey`, `ProductName`, `Brand`, `Color`, `UnitCostUSD`, `UnitPriceUSD`, `Subcategorykey`, `Subcategory`, `CategoryKey`, `Category`.
  - **sales**: `id`, `order_number`, `line_item`, `order_date`, `delivery_date`, `customer_id`, `store_id`, `product_id`, `quantity`, `currency_code`.
  - **stores**: `store_key`, `country`, `state`, `square_meters`, `open_date`.

- Store the cleaned and processed data in the respective tables.

## Identifying Patterns and Trends

### Tools Used
- **Application**: Power BI

### Steps
1. Connect to the MySQL database using server name, database name, username, and password.
2. Import the necessary tables: `customers`, `products`, `stores`, `sales`, `exchange_rates`.
3. Create visualizations:
   - **Ribbon Chart**: Show the pattern of sales by product and category.
   - **Line Chart**: Illustrate the trend of sales volume by country over time.
   - **Map**: Display the geographical distribution of stores globally.
4. Add legends, slicers, and textboxes to enhance visualization clarity and interactivity.

## Identifying Metrics Using SQL Queries
- Write 10 SQL queries to uncover trends and provide actionable insights based on historical data.
- Import data corresponding to each query into Power BI and showcase the results across 10 different pages.
- Use DAX queries in Power BI’s Advanced Editor to load data for each SQL query.
- Enhance table visualizations with effects, slicers, and appropriate titles.

## Conclusion
The **Sales Vision** project integrates multiple data sources and analytical tools to provide a comprehensive view of sales performance and trends. By using Power BI for data visualization and SQL for trend identification, this project enables deep insights into customer behavior, product performance, and geographical sales distribution.

