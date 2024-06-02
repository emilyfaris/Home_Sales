# Home_Sales

## Project Overview

In this assignment, various operations were performed using SparkSQL to extract key insights from home sales data. In addition to reading data into a Spark DataFrame, creating temporary views, and performing SQL queries, the project also explored caching and partitioning to optimize query performance.

### SQL Queries

The `home_sales_colab` notebook answers the following questions:

1. **Average price for a four-bedroom house sold for each year**
   
2. **Average price of a home for each year the home was built** that has three bedrooms and three bathrooms

3. **Average price of a home for each year the home was built** that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet

4. **Average price of a home per "view" rating** having an average home price greater than or equal to $350,000

### Caching and Optimization

- Cached the `home_sales` table and verified the cache status.
- Ran query 4 again using cached data to determine runtime and compared it to uncached runtime.

### Partitioning and Performance

- Partitioned the data by `date_built` field and created a temporary table.
- Ran query 4 again on the parquet data and compared the runtime to uncached runtime.

## Conclusion

Caching the table reduced the query run time because cached data is stored in memory, allowing for faster access and reduced I/O operations. Partitioning with parquet further reduced the query run time because it allows for efficient data storage and retrieval. 

The run time differences in this project were slight due to using a relatively small dataset, but would significantly improve efficiency and optimization for big datasets. By reducing the time and resources required for data processing, these techniques enable faster insights and more responsive data analysis.
