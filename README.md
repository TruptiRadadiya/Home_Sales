# Home_Sales

## Home Sales Analysis using SparkSQL

This project focuses on analyzing home sales data using SparkSQL. The steps include reading the data, creating temporary views, partitioning, caching, and uncaching tables, and performing various SQL queries to determine key metrics such as average home prices based on different criteria.

### File Structure

```
Home_Sales/
├── Home_Sales.ipynb                   # Jupyter Notebook with the analysis and queries
└── README.md                          # This README file
```

### What do you need?

- Python 3.7+
- PySpark
- Jupyter Notebook

### How to use the code?

1. Clone this repository to your local machine.
2. Install the required libraries using pip install pyspark.
3. Open the Jupyter Notebook `Home_Sales.ipynb` to view and run the analysis.

### Steps and Features

#### Prepare the Data

- Load the home_sales_revised.csv data into a Spark DataFrame.
- Create a temporary table named home_sales from the DataFrame.

#### Perform Queries Using SparkSQL

- Average Price for Four-Bedroom Houses Sold Each Year:
    - Calculate the average price for a four-bedroom house sold for each year.
    - Round off the answer to two decimal places.

- Average Price for Three-Bedroom, Three-Bathroom Houses by Year Built:
    - Calculate the average price of homes built each year with three bedrooms and three bathrooms.
    - Round off the answer to two decimal places.

- Average Price for Specific Criteria:
    - Calculate the average price of homes built each year with three bedrooms, three bathrooms, two floors, and at least 2,000 square feet.
    - Round off the answer to two decimal places.

- Average Price by "View" Rating:
    - Calculate the average price of homes per "view" rating where the average home price is greater than or equal to $350,000.
    - Determine and record the runtime of this query.
    - Round off the answer to two decimal places.

####Optimization Techniques

- Cache the Temporary Table:
    - Cache the home_sales temporary table to improve query performance.

- Verify Caching:
    - Verify that the home_sales temporary table is cached.

- Run Query on Cached Data:
    - Re-run the query for average price by "view" rating using the cached data.
    - Determine the runtime and compare it to the uncached runtime.

- Partition the Data:
    - Partition the home sales data by the date_built field and store it in parquet format.

- Create a Temporary Table from Partitioned Data:
    - Create a new temporary table for the parquet data.

- Run Query on Partitioned Data:
    - Re-run the average price by "view" rating query on the partitioned data.
    - Determine the runtime and compare it to both cached and uncached runtimes.

### Conclusion

This project provides a detailed approach to analyzing home sales data using SparkSQL. It demonstrates how to optimize query performance through caching and partitioning and offers insights into average home prices based on various criteria.








