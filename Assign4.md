## Assignment 4

Design schemas for the following database designs.
* Make sure that the tables have a proper primary key that correctly enforces *entity integrity*.
* Make sure that the table has all the required columns with appropriate data types  and null constraints 
* Introduce appropriate foreign key to enforce the constraints. 
* Include an insert statement to populate a few entries into each table but you do not need to completely fill the tables. 
* Follow best conventions and practices we discussed in class.
* Ensure that your schema is in 3rd normal form.
* Execute the entire assignment in one notebook, print it and submit the PDF to the instructor by Slack. 

You can use DataJoint, SQL Jupypter Magic, or `pymysql` to interact with the database. 


### Problem 1.  Students and Assignments 
Design a database that 

1. Students in this class.
2. Assignments in this class, including a link to its specification. 
3. If assignment has been graded, store the grade for each student and each assignment. 


### Problem 2. Library 
Design a database to represents books in the library. You may try to learn how real libraries identify copies of the same book.

1. Books have an ISBN but multiple copies of the same title may exist.
2. The library has members. They have a name and an address. 
3. A library member can check out any book, include the checkout date.
4. The book may not be checked out by two people at the same time. 
5. Some books are not checked out. 

### Problem 3. Bank
Design a database to represent bank customers and their accounts.

1. A bank has branches that have a phone and a street address.
1. The Bank has customers.
2. Each customer has one "home branch."
2. The bank manages bank accounts, which can be either "savings" or "checking."
3. Each account has exactly one customer as its owner.

### Problem 4. Online App
You are designing a smart phone app 

1. Users can subscribe for free, identified by their phone number
2. Users can add one or more credits cards to their account.
3. The app has paid add-ons called "Track & Field", "Marathon", and "Sprint", each with a fixed price.
4. A user can purchase each add-on, in which case she must provide a credit card for the purchase.




