# Exploratory Data Analysis of New York Airbnb Listing

# INTRODUCTION

Exploratory Data Analysis (EDA) is a crucial step in understanding and extracting insights from a dataset. In this analysis, we will explore the New York Airbnb listings dataset obtained from Kaggle. The dataset provides information about various aspects of Airbnb listings in New York, such as price, location, availability, and amenities.
Our approach involves loading the dataset into Excel for initial examination and data cleaning, utilizing SQL queries in MySQL for further data manipulation, and then performing in-depth analysis and visualization using Python and Tableau.

# Step 1: Data Extraction and Cleaning in Excel:

Download the New York Airbnb dataset from Kaggle and load it into Excel.
Identify and handle missing values, duplicates, and outliers.
Standardize data types and format columns for consistency.

# Step 2: Data Manipulation with SQL Queries in MySQL:

Create a MySQL database and table to store Airbnb data.
Use SQL queries to load data into MySQL and perform basic analysis, such as calculating average prices for each location.


#SQL QUERY
-- Connect to the MySQL database
USE your_database;

-- Create a table for Airbnb data
CREATE TABLE airbnb_data (
    id INT PRIMARY KEY,
    name VARCHAR(255),
    price INT,
    location VARCHAR(255),
    availability INT,
    amenities VARCHAR(255)
);

-- Load the data into the MySQL table (assuming CSV file)
LOAD DATA INFILE 'path/to/your/airbnb_data.csv'
INTO TABLE airbnb_data
FIELDS TERMINATED BY ','
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;

-- Example SQL query: Find the average price of listings in each location
SELECT location, AVG(price) AS avg_price
FROM airbnb_data
GROUP BY location;

# Step 3: Data Analysis in Python:

Use Python, particularly libraries like Pandas, for more advanced analysis.
Conduct exploratory data analysis, such as finding top listings, distribution of prices, and correlations between variables.

#PYTHON CODE
#Assuming you have a pandas dataframe loaded with your data
import pandas as pd

#Example: Find the top 5 most expensive listings
top_expensive = df.nlargest(5, 'price')

#Perform additional analysis as needed


# Step 4: Data Visualization in Tableau:

Connect Tableau to the MySQL database or load the cleaned dataset directly.
Create interactive and insightful visualizations to represent trends, patterns, and relationships within the data.


# Conclusion

Exploring the New York Airbnb dataset involved a multi-step process, starting with data extraction and cleaning in Excel, followed by data manipulation using SQL queries in MySQL. Python was employed for more sophisticated analysis, and finally, Tableau was used for visualization. This comprehensive approach allows for a thorough understanding of the dataset and the extraction of valuable insights. Each step plays a crucial role in ensuring the accuracy and reliability of the analysis, ultimately leading to informed decision-making in the context of Airbnb listings in New York.


