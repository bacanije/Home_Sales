# Home_Sales
## Challenge Outline
### Instructions
1.	Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.
2.	Import the necessary PySpark SQL functions for this assignment.
3.	Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.
4.	Create a temporary table called home_sales.
5.	Answer the following questions using SparkSQL (See summary for answers):
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
    For the years 2019-2022, the average four-bedroom house was sold over $200,000. In 2019 the average sat at $300,263.70, in 2020 it sold for $298,353.78, in 2021 avearge price     was $$301,819.44 and decreased in 2022 at $296,363.88
  
+--------------------+----------+
|round(avg(PRICE), 2)|year(date)|
+--------------------+----------+
|           296363.88|      2022|
|           301819.44|      2021|
|           298353.78|      2020|
|            300263.7|      2019|
+--------------------+----------+

- What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
+--------------------+----------+
|round(avg(price), 2)|date_built|
+--------------------+----------+
|           292676.79|      2017|
|           290555.07|      2016|
|            288770.3|      2015|
|           290852.27|      2014|
|           295962.27|      2013|
|           293683.19|      2012|
|           291117.47|      2011|
|           292859.62|      2010|
+--------------------+----------+
- What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
+--------------------+----------+
|round(avg(price), 2)|date_built|
+--------------------+----------+
|           280317.58|      2017|
|            293965.1|      2016|
|           297609.97|      2015|
|           298264.72|      2014|
|           303676.79|      2013|
|           307539.97|      2012|
|           276553.81|      2011|
|           285010.22|      2010|
+--------------------+----------+
- What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
+----+--------------------+
|view|round(avg(price), 2)|
+----+--------------------+
|  51|           788128.21|
|  54|           798684.82|
|  69|           750537.94|
|  87|           1072285.2|
|  73|           752861.18|
|  64|           767036.67|
|  59|            791453.0|
|  85|          1056336.74|
|  52|           733780.26|
|  71|            775651.1|
|  98|          1053739.33|
|  99|          1061201.42|
|  96|          1017815.92|
| 100|           1026669.5|
|  70|           695865.58|
|  61|           746877.59|
|  75|          1114042.94|
|  78|          1080649.37|
|  89|          1107839.15|
|  77|          1076205.56|
+----+--------------------+
only showing top 20 rows

--- 0.16201996803283691 seconds ---
