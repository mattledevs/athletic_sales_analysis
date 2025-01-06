# Background
In this practice, we'll analyze sales data to gain insights into which cities in the U.S. have sold the most athletic wear over two years. Next, we'll determine which retailers had the greatest total sales for athletic wear, and which retailers sold the most women's athletic footwear. Finally, we'll determine which day and week had the highest sales for women's athletic footwear.

# Location of GIT repository
[https://github.com/mattledevs/athletic_sales_analysis](https://github.com/mattledevs/athletic_sales_analysis)


# Combine and Clean the Data
The two CSV files, athletic_sales_2020.csv and athletic_sales_2021.csv, were imported and read into DataFrames.

Columns were checked in the two DataFrames to see similar names and data types.

The two DataFrames were combined by the rows using an inner join, and the index was reset. 

Both data frames were checked for any null values, along with each column’s data type.

The "invoice_date" column was converted to a datetime data type and confirmed.

# Region that Sold the Most Products
The groupby and pivot_table functions were used to create a multi-index DataFrame with the "region", "state", and "city" columns.

The results were sorted in descending order to show the top five regions, including the state and city that have the greatest number of products sold. 

# Region that had the Most Sales
The groupby and pivot_table functions were used to create a multi-index DataFrame with the "region", "state", and "city" columns.

The results were sorted in descending order to show the top five regions, including the state and city that generated the most sales. 

# Retailer that had the Most Sales
The groupby and pivot_table functions were used to create a multi-index DataFrame with the "retailer", "region", "state", and "city" columns.

The results were sorted in descending order to show the top five retailers along with their region, state, and city that generated the most sales. 

# Retailer that Sold the Most Women's Athletic Footwear
The combined DataFrame was filtered to create a DataFrame with only women's athletic footwear sales data.

The results were sorted in descending order to show the top five retailers along with their region, state, and city that sold the most women's athletic footwear. 

# Day with the Most Women's Athletic Footwear Sales
A pivot table was created with the "invoice_date" column as the index and the "total_sales" column as the values parameter.

The resample function was applied to the pivot table, placing the data into daily bins, to get the total sales for each day.

Then the resampled DataFrame was sorted in descending order to show the top 10 days that generated the most women's athletic footwear sales. 

# Week with the Most Women's Athletic Footwear Sales
The resample function was applied to the pivot table and placed into weekly bins, and get the total sales for each week.

The resampled DataFrame was resorted in descending order to show the top 10 weeks that generated the most women's athletic footwear sales. 

# Future Work
Future work could include created other pivot tables indexing by products like Men's Street Footware and other types of products. 