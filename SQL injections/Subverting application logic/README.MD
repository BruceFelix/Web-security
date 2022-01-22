# SQL injection vulnerability allowing login bypass
## Description 
This lab contains an SQL injection vulnerability in the login function.

To solve the lab, perform an SQL injection attack that logs in to the application as the administrator user. 

## 1 Determine if the page is vulnerable
put a ' in the username and anything on the password part
response = error
### analysis
the page is vulnerable


## 2 inject the payload
username = administrator'--
password = anything
### analysis 
It works. The username is correct and password is commented out in the backend sql query