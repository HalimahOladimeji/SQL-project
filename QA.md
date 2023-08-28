What are your risk areas? Identify and describe them. 
missing data in some columns
loss of data
quality of data

QA Process:
Describe your QA process and include the SQL queries used to execute it.

1. Check for missing values and empty columns
E.g
SELECT item_quantity             
FROM all_sessions    
WHERE item_quantity IS NOT NULL

SELECT time_on_site             
FROM all_sessions    
WHERE time_on_site IS NOT NULL

2. Validate data types
E.g
SELECT DISTINCT product_price
FROM all_sessions
WHERE ISNUMERIC(product_price) = 0;

3. Very data consistency
SELECT COUNT (DISTINCT full_visitor_id) 
FROM all_sessions

4. Sum and Product validation
SELECT SUM (product_price * product_quantity)
FROM all_sessions

In summary,
Counting Newly Added Rows (Using COUNT & GROUP BY)
Validated the data by checking for accuracy (Using SELECT, COUNT & DISTINCT)
Validated the Country names and priotize data with country names
Validate the dates to be in correct format and within 2016 and 2017
Validate calculations like total revenue, average and sentiment_ratio
Ensure numeric values are in the correct data type
