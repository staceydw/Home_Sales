# Home_Sales
Module 22 Challenge

In this challenge, SparkSQL is used to determine key metrics about home sales data. Then Spark is used to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

The following questions are answered using SparkSQL:
1. What is the average price for a four-bedroom house sold for each year? 
2. What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms?
3. What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to    2,000 square feet?
4. What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000?

The last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000 will be run using the cached data. The runtime was determined and compared to the uncached runtime, then the data was partitioned by the "date_built" field on the formatted parquet home sales data. Afterwards, a temporary table for the parquet data was created and the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000 was run. Again, the runtime was determined and compared to the uncached runtime.

Assessment of the findings:
Home prices are similar during the first several queries, ranging (on average) from $250,000-$300,000. One interesting piece of the data is that the average home price stayed relatively steady from 2010-2017, fluctuating by $10,000 at most. Of course, it's important to keep in mind that this data is not reflective of every state and town -- there are some that varied greatly (mostly increasing) during that timeframe -- but for this set, the prices are consistent. Lastly, the findings show a large increase in price when the query jumped to greater or equal to $350,000. Instead of having a lot that are in the $500,000-$800,000 range, average home prices jumpt to $1,000,000 or greater. 
