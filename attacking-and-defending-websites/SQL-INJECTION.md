# SQL  Injection

Structured Query Language is commonly a server-side language that can built a query, execute it on the server and database in order to return useful information.

In these examples we'll use MySQL conntected to a DVWA databse, which is the most common used on the internet today. MySQL shells allow you to navigate the database easily.

## Getting Started

SQL injection is all about syntax, We'll use this regular old statement as an example for now:

> SELECT first_name, last_name FROM users WHERE  user_id='1'

PHP will pass this SQL command as a string, so there is no context or intuitive understanding of the request. With that concept, the user can change a parameter for manipulative purposes.

> SELECT * FROM users WHERE user_id='1' OR '1'='1'

Utilizing this statement on the same database plays on the logic to return the first and last names of every user in the database.

In most cases you will never have direct access to a SQL shell, or the backend. That would be disasterous in context of privacy and most applications would not make such a grave mistake. What you will have access to is the web application.

