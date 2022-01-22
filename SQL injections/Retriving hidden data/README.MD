# Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data

## Description
 This lab contains an SQL injection vulnerability in the product category filter. When the user selects a category, the application carries out an SQL query like the following:

SELECT * FROM products WHERE category = 'Gifts' AND released = 1

To solve the lab, perform an SQL injection attack that causes the application to display details of all products in any category, both released and unreleased. 

### step 1 determine if the their is a vulnerability
GET /filter?category=Gifts' response 500 
#### analysis
The response shows that the page is vulnerable.

### step2 inject the payload
'+OR+1%3d1-- response = 200
#### analysis
Retrived all the products released and unreleased.
The payload 1=1 is always true
and the comments -- after the 1=1 is used to ignore the rest of the query


![image](https://user-images.githubusercontent.com/44478872/150627360-f4621ccd-16fd-4f3c-8207-5327516d5c76.png)
