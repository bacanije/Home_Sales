# Home_Sales
## Challenge Outline
### Instructions
1.	Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.
2.	Import the necessary PySpark SQL functions for this assignment.
3.	Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.
4.	Create a temporary table called home_sales.
5.	Answer the following questions using SparkSQL:
- What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
- What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
- What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
- What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your        answer to two decimal places.
7.  Cache your temporary table home_sales.
8.	Check if your temporary table is cached.
9.	Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine
    the runtime and compare it to uncached runtime.
11.	Partition by the "date_built" field on the formatted parquet home sales data.
12.	Create a temporary table for the parquet data.
13.	Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
14.	Uncache the home_sales temporary table.
15.	Verify that the home_sales temporary table is uncached using PySpark.
16.	Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.

# Summary
- What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
- What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
- What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
- What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
