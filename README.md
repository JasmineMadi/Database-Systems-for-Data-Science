# Database-Systems-for-Data-Science (Fall 2023)
**MS Applied Data Science**

**Instructor:** Dimitri Yatsenko, Ph.D.

## Syllabus

Organization concepts and terminology of data models and the underlying data architectures needed to support them. 
Presentation of the relational database management systems including an introduction to SQL programming: relational database design and data queries with integration into application programming languages, with Python used for examples. 

I will assume basic Python proficiency: we want to use databases directly from Python. 

The course will include practical exercises and will be graded based on several indvidual and group projects using real-world datasets.

## Class and attendance

Class participation is required and much of the material will be presented in class only. The class will be held in room Malloy 024 and also broadcast in Zoom.
We will also use a Slack channel. If you have not received access to any of these resources, please notify your instructor.

## Textbook 

The University provided you with a [Safari Books](https://www.oreilly.com) subscription account. Readings, examples, and projects will be selected primarily from the following references:

1. Jan L. Harrington, *Relational Database Design and Implementation*: 4th edition (2016)

  * https://learning.oreilly.com/library/view/relational-database-design/9780128499023/

2. Alan Beaulieu, Learning SQL, 3rd Edition (2020)

  * https://learning.oreilly.com/library/view/learning-sql-3rd/9781492057604/

3. Michael Hernandez, *Database Design for Mere Mortals: A Hands-On Guide to Relational Database Design*; 4th edition (2020).  ISBN-13: 978-0136788041 ISBN-10: 0136788041

  * https://learning.oreilly.com/library/view/database-design-for/9780136788133/

4. Josephine Bush, *Learn SQL Database Programming* (2020)

  * https://learning.oreilly.com/library/view/learn-sql-database/9781838984762/

Additional slides and notes will be provided in class.


## Grading 
10-12 Assignments/Projects

|grade| percent |
|---|---|
|**A** |>=94%|
|**A-**|>=90%|
|**B+**|>=86%|
|**B**|>=82%|
|**B-**|>=78%|
|**C+**|>=74%|
|**C**|>=70%|
|**C-**|>=66%|
|**D+**|>=62%|
|**D**|>=58%|
|**F**|>=0%|


## Weeks 1-2: (Aug 22, Aug 29)

History of datatabases and database technologies.

Databases in data science. Data models: diverse ways to think about data: hiearchical, network, relational, object, graph, and document data models.

Database access. Creating SQL tables and inserting data. Simple queries. sqlite and mysql.

Issue SQL queries from Jupyter using SQL Magic.

Issuing SQL queries from Python code using a database client library, (`pymysql`). 

`CREATE SCHEMA`, `CREATE TABLE`, `INSERT`, `DELETE`, `DROP TABLE`, `DROP SCHEMA`. 

Create schemas and tables, insert rows, delete, and drop.

Using the `faker` module to populate tables.

Using `datajoint` as a high-level interface. 

Datatypes: numerical, character strings, and enum. 


### Homework 1 (due Sep 5)
1. On GitHub, fork the repository  https://github.com/MSDS-5315/datajoint-tutorials into your repository.
   Run the `db-course` tutorials in Dev Container in VSCode on your computer or on GitHub CodeSpaces, following the README instructions. 

2. On the MySQL server, create a database named `university` and define a table named `person`. Make sure it has a well chosen primary key. 
 * Connect to the database server 
 * Create a schema, a table within it, and insert at least one row. 

Report success to the instructor. Learn to start and stop your own  database server and to connect to it reliably.  This will be necessary for all your subsequent assignments. 


### Readings: 
  * Harrington, Chapter 1, "The Database Environment"
  * Hernandez, Chapter 1, "The Relational Database" 
  * Beauliue, Chapter 2: "Creating and Populating a Database"
  * Generating fake data: https://towardsdatascience.com/generating-fake-data-with-python-c7a32c631b2a
1. Create a `university` database 
2. Create a table named `person` with basic attributes: name, date of birth, address, phone, 
3. Insert at least one record into the person table.

### Key terms
Database, database system, database server, data model, data integrity, data consistency, ACID, relational data model, SQL, imperative queries, schema.

### Key skills
* Connect to the MySQL database provided for the class, create a simple table, and insert data into it.
* Issue queries in SQL (using the SQL magic in jupyter for quick SQL scripting) 
* Execute queries with a client library (`pymysql`). Generate fake data. See notebook `Fake-It.ipynb`
* Execute queries using DataJoint. See notebooks `DataJoint-config` and `DataJoint-Intro`.

### Homework 2 (due Sep 13)

1. Answer questions in [Block 1](Block1.md). You can check your answers with ChatGPT or a similar service.  Do not turn in your answers.
Come up with one original non-trivial question about the material and post it in the class chat room. Provide your own answer as well. 


## Weeks 3-5: (Sep 5, Sep 12, Sep 19)

Data models: diverse ways to think about data: hierarchical, network, relational, object, graph, and document data models. 

### Key concepts 

* Data models: structured (schema) and self-describing (schema-less). 
* How a database table works. 
* Schema design. Simple queries. Primary key. Foreign keys. Entity integrity. Referential integrity. 
* Normalization. First normal form.  Entity normalization.
* Diagramming. Entity-Relationship Diagrams. DataJoint diagrams. 
* See the `Language` notebook used in Lecture 3.
* Relational algebra: restriction and projection. The structure of the `SELECT` Statement.
* `SELECT ... FROM ... WHERE ... ORDER BY ... LIMIT ...`
* Fetch. Order by. Offset and Limit.
* Declarative queries vs. imperative queries
* Default values. Nullable attributes. Nullable foreign keys.
* UUID, surrogate keys, secondary unique constraints


### Readings:
  * Harrington, Chapters 3-7
  * Hernandez, Chapters 2-3
  * Beaulieu, Chapters 3-4
  * Beaulieu [Appendix A. ER Diagram](https://learning.oreilly.com/library/view/learning-sql-3rd/9781492057604/app01.html)
  * Example databases: https://dev.mysql.com/doc/index-other.html

[Assignment 3](Assign3.md) -- Due Sep 26

### Resources and exercises
* http://www.w3resource.com/mysql-exercises/ 
* http://www.w3resource.com/sql-exercises/


* [Assignment 4](Assign4.md) -- Due Oct 3



* [Assignment 5](https://github.com/msds-5315/datajoint-tutorials/blob/main/db-course/005-Queries-HW.ipynb) -- Due Oct 17 

## Weeks 6-8 (Sep 26, Oct 3, Oct 10 (Fall Break), Oct 17)

Surrogate keys / Natural keys. 
Indexes, secondary unique keys.
Data serialization - blobs.

Notebooks 
* [Joins](notebooks/Joins.ipynb)
* [GroupBy](notebooks/GroupBy.ipynb)
* [Indexes](notebooks/Indexes.ipynb)
* [Using BLOBS](notebooks/Using-BLOBs.ipynb)
* [Division](notebooks/Relational-Division.ipynb)

Advanced Queries: 

* Subqueries
* Inner Joins: cross join, theta join, equijoin, natural join
* Aggregations 

Reading: Harrington  Chapters 16-19


## Weeks 9, 10 (Oct 24, Oct 31, Nov 7)

* [Assignment 6](https://github.com/msds-5315/datajoint-tutorials/blob/main/db-course/006-Joins-HW.ipynb) -- Due Nov 9
* [Assignment 7](https://github.com/msds-5315/datajoint-tutorials/blob/main/db-course/007-Aggregation-HW.ipynb) -- Due Nov 16


Modeling relationships: 

* Sequences and workflows.
* Specialization / generalization.
* Hierarchies (ownership, composite keys, partial keys)
* Groupings 
* Directed Graphs (including trees)
* Unidrected Graphs.
* Master-part relationships

Transaction processing.

* [Assignment 8](https://github.com/msds-5315/datajoint-tutorials/blob/main/db-course/008-Transactions-HW.ipynb) -- Due Nov 28.


Reading: 

* Harrington: Chapters 13, 14, 15 (case studies), 22 (concurrency and transactions)


## Weeks 11-13 (Nov 14, Nov 21, Nov 28):
Putting it all together. Practical examples

Final: Design due on Nov 27.  Complete submission Dec 13.


