Normalization
Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included.
 The database table is where all the data in a database is stored,
•	Tables 
o	Tables are used to store data within the database. 
•	Indexes 
o	Indexes are used to make data retrieval faster.  
•	Views 
o	the view hides some of the database complexity.  This makes it easier to read queries; 
•	Stored Procedures 
o	programs can be stored in the SQL database as stored procedures. 
	A stored procedure is a group of one or more database statements stored in the database’s data dictionary and called from either a remote program, another stored procedure, or the command line.
	Stored procedure are commonly called SPROCS, or SP’s.  Stored procedure features and command syntax are specific to the database engine.  Traditionally Oracle uses PL/SQL as its language; whereas, SQL Server uses T/SQL.
•	Triggers 
o	Triggers are special instructions that are executed when important events, such as inserting or updating records in a table happen.  The most common triggers are Insert, Update, and Delete triggers
It is these various pieces that are used to house, retrieve, and process data with the SQL database.
Rows
•	A table can contain zero or more rows.  When there are zero, it said to be empty.
Columns
•	Columns are defined to hold a specific type of data, such as dates, numeric, or textual data.  In the simplest of definitions a column is defined by its name and data type.  
Reasons for Database Normalization
There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 
1.	 Search and Sort Issues making it easier to search and sort your data. 
2.	Data Duplication and Modification Anomalies
•	 Duplicated information presents two problems:
1.	
1.	It increases storage and decrease performance.
2.	It becomes more difficult to maintain data changes
3.  Simplify Queries
There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively. 
•	First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
•	Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
•	Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key

