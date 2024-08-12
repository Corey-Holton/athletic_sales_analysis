# Athletic Sales Data Analysis

## Description

This project processes athletic sales data from 2020 and 2021 to determine various sales metrics. It reads sales data from CSV files, combines and cleans the data, and then performs several analyses to find the top-performing regions, retailers, and products.

## Table of Contents

1. [Setup](#setup)
2. [Combine and Clean the Data](#combine-and-clean-the-data)
    - [Import CSVs](#import-csvs)
    - [Check Data Types](#check-data-types)
    - [Combine Sales Data](#combine-sales-data)
    - [Clean Data](#clean-data)
3. [Analysis](#analysis)
    - [Region with Most Products Sold](#region-with-most-products-sold)
    - [Region with Most Sales](#region-with-most-sales)
    - [Retailer with Most Sales](#retailer-with-most-sales)
    - [Retailer with Most Women's Athletic Footwear Sales](#retailer-with-most-womens-athletic-footwear-sales)
    - [Day with Most Women's Athletic Footwear Sales](#day-with-most-womens-athletic-footwear-sales)
    - [Week with Most Women's Athletic Footwear Sales](#week-with-most-womens-athletic-footwear-sales)
4. [Usage](#usage)

## Setup

- Import the necessary libraries: `pandas` and `pathlib.Path`.

## Combine and Clean the Data

### Import CSVs

- Read the CSV files `athletic_sales_2020.csv` and `athletic_sales_2021.csv` into DataFrames.

### Check Data Types

- Display and inspect the data types of each DataFrame.
- Check for any null values.

### Combine Sales Data

- Combine the 2020 and 2021 sales DataFrames by rows and reset the index.

### Clean Data

- Check for and handle any null values.
- Convert the "invoice_date" column to a datetime datatype.
- Confirm that the "invoice_date" data type has been changed.

## Analysis

### Region with Most Products Sold

#### Using `groupby`

- Group the data by region, state, and city to find the total number of products sold.
- Sort and display the top 5 results.

#### Using `pivot_table`

- Create a pivot table to find the total number of products sold by region, state, and city.
- Sort and display the top 5 results.

### Region with Most Sales

#### Using `groupby`

- Group the data by region, state, and city to find the total sales.
- Sort and display the top 5 results.

#### Using `pivot_table`

- Create a pivot table to find the total sales by region, state, and city.
- Sort and display the top 5 results.

### Retailer with Most Sales

#### Using `groupby`

- Group the data by retailer, region, state, and city to find the total sales.
- Sort and display the top 5 results.

#### Using `pivot_table`

- Create a pivot table to find the total sales by retailer, region, state, and city.
- Sort and display the top 5 results.

### Retailer with Most Women's Athletic Footwear Sales

- Filter the sales data to get the women's athletic footwear sales data.

#### Using `groupby`

- Group the filtered data by retailer, region, state, and city to find the total units sold.
- Sort and display the top 5 results.

#### Using `pivot_table`

- Create a pivot table to find the total units sold by retailer, region, state, and city.
- Sort and display the top 5 results.

### Day with Most Women's Athletic Footwear Sales

- Create a pivot table with the 'invoice_date' column as the index and the "total_sales" as the values.
- Resample the pivot table into daily bins and sort to find the day with the most sales.
- Display the top 10 results.

### Week with Most Women's Athletic Footwear Sales

- Resample the pivot table into weekly bins and sort to find the week with the most sales.
- Display the top 10 results.

## Usage

1. Ensure you have the necessary CSV files (`athletic_sales_2020.csv` and `athletic_sales_2021.csv`) in the `Resources` directory.
2. Run the script to perform the data analysis.
3. Review the results for insights into sales performance by region, retailer, and product.

## References
Thiscode was assemebled with the help of classmates, AskBCS, Learning Assistant and the readme file was published with the help of ChatGBT.

## Results
- The New York, New York of the NorthEast region had the most overall sales
- West Gear in San Franscisco had the most sales from a single retailer
- West Gear sold the most womans athletic footware at a single location, but Footlocker as a retailer sold the most womans footware
-Both the most sales in a single day and month were calculated to be July 16th 2021 and December 19th 2021 respectively. 



