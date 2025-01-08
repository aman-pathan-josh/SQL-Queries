1)  Find the number of orders sent by each shipper.

```sql
SELECT shippers.company_name AS ShipperName, COUNT(orders.order_id) AS TotalOrders
FROM shippers
JOIN orders
ON shippers.shipper_id = orders.ship_via
GROUP BY shippers.company_name
ORDER BY TotalOrders ASC;
```

2)  Find the number of orders sent by each shipper, sent by each employee

pending
```sql
SELECT shippers.company_name AS ShipperName, employees.first_name AS EmployeeName, COUNT(orders.order_id) AS TotalOrders
FROM orders
JOIN shippers
ON orders.ship_via = shippers.shipper_id
JOIN employees
ON employees.employee_id = orders.order_id
GROUP BY employees.first_name, shippers.company_name
ORDER BY TotalOrders DESC;
```

3)  Find  name  of  employees who has registered more than 100 orders.

```sql
SELECT employees.first_name,employees.last_name, COUNT(orders.employee_id) AS TotalOrders
FROM orders 
JOIN employees 
ON orders.employee_id = employees.employee_id
GROUP BY orders.employee_id, employees.first_name,employees.last_name
HAVING COUNT(orders.employee_id) >= 100
ORDER BY TotalOrders DESC;
```

4) Find if the employees "Davolio" or "Fuller" have registered more than 25 orders.

```sql
SELECT employees.first_name,employees.last_name, COUNT(orders.employee_id) AS TotalOrders
FROM orders 
JOIN employees 
ON orders.employee_id = employees.employee_id
GROUP BY orders.employee_id, employees.first_name, employees.last_name
HAVING COUNT(orders.employee_id) >= 25 AND employees.last_name in ('Davolio','Fuller')
ORDER BY TotalOrders DESC;
```

5  Find the customer_id and name of customers who had placed orders more than one time and how many times they have placed the order

6 Select all the orders where the employee’s city and orders ship city are same.

7 Create a report that shows the order ids and the associated employee names for orders that shipped 

 8 Create a report that shows the total quantity of products ordered fewer than 200.

 9 Create a report that shows the total number of orders by Customer since December 31, 1996 and the NumOfOrders is greater than 15.

 10 Create a report that shows the company name, order id, and total price of all products of which Northwind has sold more than $10,000 worth.
          
 11 Create a report showing the Order ID, the name of the company that placed the order,
   and the first and last name of the associated employee. Only show orders placed after January 1, 1998  hat shipped after they were required. Sort by Company Name.

 12  Get the phone numbers of all shippers, customers, and suppliers.

 13 Create a report showing the contact name and phone numbers for all employees,customers, and suppliers.

 14 Fetch all the orders for a given customers phone number 030 0074321.

 15 Fetch all the products which are available under Category Seafood.

 16 Fetch all the products which are supplied by a company called Pavlova, Ltd.

 17 All orders placed by the customers belong to London city.

 



18 All orders placed by the customers not belong to London city.

 20 Find the name of the company that placed order 10290.

 21 Find the Companies that placed orders in 1997

 22 Get the product name , count of orders processed

 23 Get the top 3 products which has more orders

 24 Get the list of employees who processed the order chai

 25 Get the shipper company who processed the order categories Seafood.

 26 Get category name , count of orders processed by the USA employees

 27 Select CategoryName and Description from the Categories table sorted by CategoryName.

 28 Select ContactName, CompanyName, ContactTitle, and Phone from the Customers table sorted byPhone.

 29 Create a report showing employees' first and last names and hire dates sorted from newest to oldest employee.

30 Create a report showing Northwind's orders sorted by Freight from most expensive to cheapest. Show OrderID, OrderDate, ShippedDate, CustomerID, and Freight.

31 Select CompanyName, Fax, Phone, HomePage and Country from the Suppliers table sorted by Country in descending order and then by CompanyName in ascending order

 32 Create a report showing all the company names and contact names of Northwind's customers in Buenos Aires.

33 Create a report showing the product name, unit price and quantity per unit of all products that are out of stock.

 34 Create a report showing the order date, shipped date, customer id, and freight of all orders placed on May 19, 1997.

 35 Create a report showing the first name, last name, and country of all employees not in the United States.

 36 Create a report that shows the city, company name, and contact name of all customers who are in cities that begin with "A" or "B."

 37 Create a report that shows all orders that have a freight cost of more than $500.00.

 38 Create a report that shows the product name, units in stock, units on order, and reorder level of all
products that are up for reorder.

 39 Create a report that shows the company name, contact name and fax number of all customers that have a fax number.

 40 Create a report that shows the first and last name of all employees who do not report to anybody.
 41 Create a report that shows the company name, contact name and fax number of all customers that have a fax number, Sort by company name.

 42 Create a report that shows the city, company name, and contact name of all customers who are in cities that begin with "A" or "B." Sort by contact name in descending order.

 43 Create a report that shows the first and last names and birth date of all employees born in the 1950s

 44 Create a report that shows the shipping postal code, order id, and order date for all orders with a ship postal code beginning with "02389".

 45 Create a report that shows the contact name and title and the company name for all customers whose contact title does not contain the word "Sales".

 46 Create a report that shows the first and last names and cities of employees from cities other than Seattle in the state of Washington.
