### PUNTO 1
SELECT customer.cust_name, customer.city, salesman.name, commission<br />
   ...> FROM customer<br />
   ...> INNER JOIN salesman ON customer.salesman_id = salesman.salesman_id<br />
   ...> WHERE salesman.commission > 0.12;

