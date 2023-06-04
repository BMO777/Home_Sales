# Home_Sales
Using knowledge of SparkSQL to determine key metrics about home sales data

In this repo you will find a jupyter notebook file with sparkSQL queries that explores home sales data contained in the csv file within the resources folder.

1st the PySpark SQL functions are imported then a spark session is created, next the aforementioned csv is read to display into a sparksql dataframe.

Then after creating a temporary sales table with home sales data, the following queries are answered though sparkSQl queries:
* What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

* What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

* What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

* What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

Then the last query is rerun once with a cached temporary sales table then again with a temporary table created from a paraquet partition of the 'data built' column or field on the home sales data

The queries run on the cached temporry sales table and on the temporary table created from a paraquet partition of the 'data built' field, have a faster runtime than the uncached and un-paraquated runtime.

Also the query runtimes seem to get quicker as they are run on the the cached ones where at least one field is paraquet partitioned. So one can see the advantage when running multiple queries on the same table.Sometimes more than twice as quick.

Requirements to run; python with the pyspark library, Spark from https://spark.apache.org/downloads.html, and jdk...  
