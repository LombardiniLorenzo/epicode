### PUNTO 1
SELECT customer.cust_name, customer.city, salesman.name, commission<br />
&ensp;&ensp;&ensp;FROM customer<br />
&ensp;&ensp;&ensp;INNER JOIN salesman ON customer.salesman_id = salesman.salesman_id<br />
&ensp;&ensp;&ensp;WHERE salesman.commission > 0.12;

### PUNTO 2
