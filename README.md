# Eshop-sales-analysis
A self-generated data analysis on sales growth for a short period.

## Table of contents
- [Project overview](#project-overview)
- [Data sources](#data-sources)
- [Data tools](#data-tools)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data analysis](#data-analysis)
- [Findings](#findings)
- [Recommendation](#recommendation)
  
### Project Overview
This project shows the sales growth in an e-shop in a short period from 2023 to January 2024.

![Eshop data visualization](https://github.com/VictoryOfejiro-O/eshop-sales-analysis/assets/152421383/c6b19b5d-90b6-425a-ba1f-4808dd9fcc7c)

### Data sources
The data used in this project is generated from Google Chrome and populated by me.

### Data tools
- The draw.io website (ER diagram) [Download here](https://drive.google.com/file/d/1_A1TkGtFWzyUJVVAotHUlMkkG5OyDxtS/view?usp=sharing)
- Mysql server (database creation and analysis)
- Tableau (visualization) [View Dashboard here](https://public.tableau.com/views/AnEshopsalesanalysis-SmallData/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)
  
### Exploratory Data Analysis
1.	What is the sales trend?
2.	What country are most of the customers with higher sales?
3.	And what is their product preference based on their orders?
4.	What is the lowest-selling product?
5.	What can be done to boost the sales of those products?
   
### Data analysis
```sql
SELECT * FROM customers WHERE city = 'ikeja';
```
```sql
SELECT DISTINCT product_title 
FROM products WHERE genre = 'fiction' 
AND product_type = 'book';
```
OR
```sql
SELECT * FROM products 
WHERE genre = 'fiction' 
AND product_type = 'book'; 
```
```sql
SELECT COUNT(city) FROM customers 
WHERE city = 'logan';
```
```sql
SELECT AVG(unit_price) FROM products;
```
```sql
SELECT * FROM orders 
WHERE order_date >= '2024-01-01';
```
```sql
SELECT * FROM orders
WHERE product_type = 'music record'
AND payment_method REGEXP 'credit card';
```
```sql
SELECT COUNT(order_id) FROM orders;
```
```sql
SELECT COUNT(product_type) FROM employees
WHERE product_type = 'music record';
```
### Findings
- There are 10 orders, 80% of which are movies and music record products, from customers mostly in the United States and Nigeria, respectively, as shown in the data visualization. 
- Sweden has the lowest order record; this could be due to limited products that suit customers from that country.
- Most of the product languages available online are English, hence the highest sales/orders recorded are from customers in English-speaking countries. 

### Recommendation
Even with the limited data and products available on Eshop, the sales are a bit high within the short period provided. I would suggest more products be made available, both in English and other languages to boost sales in other non-English speaking countries too.





