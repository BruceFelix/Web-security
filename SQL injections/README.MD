# SQL injection
SQL injection is an old-but-gold vulnerability responsible fro many high profile data breaches. Although relatively simple to learn, it can potentially be used for some high-severity exploits.

### An image

## What is an SQL Injection(SQLi)?


SQL injection is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. It generally allows an attacker to view data that they are not normally able to retrieve. This might include data belonging to other users, or any other data that the application itself is able to access. In many cases, an attacker can modify or delete this data, causing persistent changes to the application's content or behavior.

In some situations, an attacker can escalate an SQL injection attack to compromise the underlying server or other back-end infrastructure, or perform a denial-of-service attack.

## What is the impact of a successful SQL injection attack?
A successful SQL injection attack can result in unauthorized access to sensitive data, such as passwords, credit card details, or personal user information. Many high-profile data breaches in recent years have been the result of SQL injection attacks, leading to reputational damage and regulatory fines. In some cases, an attacker can obtain a persistent backdoor into an organization's systems, leading to a long-term compromise that can go unnoticed for an extended period. 

## SQL injection examples
 There are a wide variety of SQL injection vulnerabilities, attacks, and techniques, which arise in different situations. Some common SQL injection examples include:

   * Retrieving hidden data, where you can modify an SQL query to return additional results.
   * Subverting application logic, where you can change a query to interfere with the application's logic.
   * UNION attacks, where you can retrieve data from different database tables.
   * Examining the database, where you can extract information about the version and structure of the database.
   * Blind SQL injection, where the results of a query you control are not returned in the application's responses.


The majority of SQL injection vulnerabilities can be found quickly and reliably using Burp Suite's web vulnerability scanner.
SQL injection can be detected manually by using a systematic set of tests against every entry point in the application. This typically involves:

    Submitting the single quote character ' and looking for errors or other anomalies.
    Submitting some SQL-specific syntax that evaluates to the base (original) value of the entry point, and to a different value, and looking for systematic differences in the resulting application responses.
    Submitting Boolean conditions such as OR 1=1 and OR 1=2, and looking for differences in the application's responses.
    Submitting payloads designed to trigger time delays when executed within an SQL query, and looking for differences in the time taken to respond.
    Submitting OAST payloads designed to trigger an out-of-band network interaction when executed within an SQL query, and monitoring for any resulting interactions.
