What issues will you address by cleaning the data?

Make the data readable
Calculate revenue
Using correct data types e.g changing varchar values to Numeric in order to use values for calculations by using CAST
Removing duplicates e.g Some values under product_sku (which should be unique)  were repeated. Use DISTINCT
Joining tables that had similar columns e.g products and sales_report using UNION or JOIN
Filling in empty columns with correct values e.g transaction_revenue
Creating new columns that helped with cleaning data
Change unit price to correct USD value 
Some columns had NULL values which were either changed to 0, default values or removed.
Combine duplicate visitorid to know the total products bought 

Queries:
Below, provide the SQL queries you used to clean your data.
ALTER TABLE all_sessions 
ALTER COLUMN converted_time TYPE time USING '00:00'::time + (converted_time	|| ' seconds')::interval;

ALTER TABLE all_sessions
ALTER COLUMN visit_id TYPE numeric USING visit_id::numeric;

UPDATE all_sessions
SET converted_time = '00:00'::time + (converted_time	|| ' seconds')::interval;

UPDATE all_sessions
SET country = ('Not given')
WHERE country = ('(not set)');

UPDATE all_sessions
SET city = ('Not given')
WHERE city = ('not available in demo dataset');

UPDATE all_sessions
SET time_on_site = ('0')
WHERE time_on_site IS NULL

UPDATE all_sessions
SET session_quality_dim = ('N/A')
WHERE session_quality_dim IS NULL

UPDATE all_sessions
SET visit_id= CAST(visit_id AS integer)

UPDATE all_sessions
SET full_visitor_id= CAST(full_visitor_id AS bigint)

ALTER TABLE all_sessions    
ALTER COLUMN full_visitor_id TYPE numeric USING full_visitor_id::numeric

ALTER TABLE all_sessions    
ALTER COLUMN product_price TYPE numeric USING product_price::numeric

ALTER TABLE analytics
ALTER COLUMN unit_price TYPE numeric USING unit_price::numeric

UPDATE all_sessions
SET product_price = CAST(product_price AS integer)

UPDATE all_sessions
SET product_price = CAST (product_price / 1000000 AS DECIMAL(8,2))
SELECT CAST (product_price / 1000000 AS DECIMAL(8,2))

UPDATE all_sessions
SET full_visitor_id = CAST(full_visitor_id AS bigint)

UPDATE all_sessions
SET product_variant= ('N/A')
WHERE product_variant = ('(not set)')

CREATE TABLE combined_sales AS
SELECT DISTINCT product_sku, total_ordered
FROM sales_report
UNION ALL
SELECT product_sku, total_ordered
FROM sales_by_sku;

UPDATE all_sessions
SET product_quantity = products.ordered_quantity
FROM products
WHERE all_sessions.product_sku = products.product_sku;

ALTER TABLE all_sessions    
ALTER COLUMN product_quantity TYPE numeric USING product_quantity::numeric

ALTER TABLE all_sessions    
ALTER COLUMN time_on_site TYPE numeric USING time_on_site::numeric

ALTER TABLE all_sessions    
ALTER COLUMN pageviews TYPE numeric USING pageviews::numeric

ALTER TABLE all_sessions    
ALTER COLUMN product_refund_amount TYPE numeric USING product_refund_amount::numeric

ALTER TABLE all_sessions    
ALTER COLUMN product_revenue TYPE numeric USING product_revenue::numeric

UPDATE all_sessions
SET product_refund_amount = all_sessions.product_quantity * all_sessions.product_price
WHERE product_sku = product_sku;

UPDATE analytics   
SET unit_price = CAST (unit_price / 1000000 AS DECIMAL(8,2)) 

ALTER TABLE all_sessions
RENAME COLUMN revenue
TO product_refund_amount;

UPDATE all_sessions
SET product_revenue = ('0')
WHERE product_revenue IS NULL

UPDATE all_sessions  
SET transactions = ('1')  
WHERE transactions IS NULL

UPDATE all_sessions 
SET total_transaction_revenue = ('N/A')
WHERE total_transaction_revenue IS NULL

ALTER TABLE all_sessions
DROP COLUMN search_keyword, transaction_id, transaction_revenue, item_revenue, item quantity;

UPDATE all_sessions
SET "eCommerce_action_option" = ('N/A')
WHERE "eCommerce_action_option" IS NULL
