### PUNTO 1
SELECT customer.cust_name, customer.city, salesman.name, commission<br />
&ensp;&ensp;&ensp;FROM customer<br />
&ensp;&ensp;&ensp;INNER JOIN salesman ON customer.salesman_id = salesman.salesman_id<br />
&ensp;&ensp;&ensp;WHERE salesman.commission > 0.12;

### PUNTO 2
SELECT customer.cust_name, customer.city, customer.grade, salesman.name, salesman.city<br />
&ensp;&ensp;&ensp;FROM customer<br />
&ensp;&ensp;&ensp;INNER JOIN salesman ON customer.salesman_id = salesman.salesman_id<br />
&ensp;&ensp;&ensp;ORDER BY customer_id;

### PUNTO 3
SELECT customer.cust_name, customer.city, customer.grade, salesman.name, salesman.city<br />
&ensp;&ensp;&ensp;FROM customer<br />
&ensp;&ensp;&ensp;INNER JOIN salesman ON customer.salesman_id = salesman.salesman_id<br />
&ensp;&ensp;&ensp;WHERE customer.grade < 300<br />
&ensp;&ensp;&ensp;ORDER BY customer.customer_id DESC;

### PUNTO 4
SELECT city FROM customer
UNION
SELECT city FROM salesman;
