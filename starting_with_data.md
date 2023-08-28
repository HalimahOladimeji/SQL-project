Question 1: find the total number of unique visitors 

SQL Queries: 
SELECT COUNT(DISTINCT visitor_id) AS total_unique_visitors
FROM your_table_name;

Answer: 14147



Question 2: average time spent by visitors on the website

SQL Queries: 
SELECT AVG(time_on_site) AS average_time_on_site
FROM (
    SELECT full_visitor_id, time_on_site                          
    FROM all_sessions    
) AS subquery;

Answer:
175.7130302629840095


Question 3: date and month that has highest orders

SQL Queries:
SELECT date AS highest_order_date, COUNT(*) AS orders
FROM all_sessions   
GROUP BY date            
ORDER BY orders DESC
LIMIT 10;

Answer:
Highest sales was in August 2016.
"20160815"	106
"20160831"	105
"20160818"	102
"20160809"	99
"20160902"	93
"20160804"	91
"20160816"	87
"20160808"	87
"20160901"	86
"20170426"	85

Question 4: Average orders from each visitor at each visit

SQL Queries:
SELECT AVG(item_count) AS average_items_per_order
FROM (
    SELECT visit_id, COUNT(*) AS item_count
    FROM all_sessions   
    GROUP BY visit_id
) AS subquery;
Answer:
1.03970871118439131630


Question 5: 
count number of returning visitors
SQL Queries:
SELECT COUNT(*) AS returning_visitors_count
FROM (
    SELECT visit_id
    FROM all_sessions   
    GROUP BY visit_id
    HAVING COUNT(*) > 1
) AS subquery;

Answer:
553
