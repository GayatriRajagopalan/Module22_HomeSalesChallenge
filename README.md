# Home Sales Challenge

This project demonstrates how to use Spark SQL for reading and querying a dataset, specifically focusing on partitioning and caching for performance optimization. 

The dataset includes home sales data with various attributes such as price, bedrooms, bathrooms, square footage, and date of sale.

## The project covers:

Loading a CSV file into a PySpark DataFrame.

Creating temporary views for SQL queries.

Running Spark SQL queries to calculate average home prices based on different filters.

Optimizing queries using partitioning and caching.

Comparing performance between partitioned and cached data.

## Key Concepts:

### Queries

Query 1: Calculates the average price of 4-bedroom houses sold per year.

Query 2: Calculates the average price of 3-bedroom, 3-bathroom homes grouped by the year the home was built.

Query 3: Filters homes that have 3 bedrooms, 3 bathrooms, 2 floors, and are over 2000 square feet, then calculates the average price grouped by the year the home was built.

Query 4: Calculates the average price for each "view" rating, filtering for homes with an average price greater than or equal to $350,000.

Query 5: Calculates the average price for each "view" rating, filtering for homes with an average price greater than or equal to $350,000 with a year filter.

## Caching

Caching stores data in memory for faster subsequent queries. When data is cached, it doesn't need to be re-read from disk, making repeated queries faster.

## Partitioning

Partitioning organizes data into separate directories based on the values of a specified column (e.g., date_built). 

This helps optimize query performance, particularly when filtering or grouping by the partitioned column.

However, partitioning is only useful if your query filters or groups by the partitioned column. If not, partitioning might not significantly improve performance.

## Conclusion

Partitioning is useful when filtering or grouping by the partitioned column. It improves query performance by reading only relevant data.

Caching is beneficial when repeatedly querying the same dataset, as it stores the data in memory for faster access.
