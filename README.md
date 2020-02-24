# Task13_BootcampRefactory
SQL

###QUERY

Create query to show orders by customer

  SELECT customers.forename, orders.* FROM Customers INNER JOIN orders ON customers.id = orders.customer_id ORDER BY CUSTOMERS.FORENAME;                      

Create query to show sum of orders by order status (“paid”, “cancelled”,"pending")

  SELECT STATUS, COUNT(STATUS) FROM ORDERS GROUP BY STATUS; 

Create query to show products by categories

  SELECT CATEGORIES.NAME, PRODUCTS.NAME FROM CATEGORIES INNER JOIN PRODUCTS ON PRODUCTS.CAT_ID = CATEGORIES.ID ORDER BY CATEGORIES.NAME; 

Create query to show address of customers orders

  SELECT ORDERS.ID, DELIVERY_ADDRESSES.ADD1, DELIVERY_ADDRESSES.ADD2, DELIVERY_ADDRESSES.ADD3 FROM DELIVERY_ADDRESSES INNER JOIN orders ON DELIVERY_ADDRESSES.ID = ORDERS.DELIVERY_ADD_ID ORDER BY ORDERS.ID;

Create query to show all product on orders

  SELECT ORDERS.ID, PRODUCTS.NAME FROM PRODUCTS JOIN ORDER_ITEMS ON ORDER_ITEMS.PRODUCT_ID = PRODUCTS.ID JOIN ORDERS ON ORDER_ITEMS.ORDER_ID = ORDERS.ID ORDER BY ORDERS.ID; 
