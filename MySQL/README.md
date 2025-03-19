**MYSQL**

MySQL is an open-source relational database management system(RDBMS) developed by Oracle Corporation. It is used to store, manage, and retrieve structured data. MySQL uses Structured Query Language(SQL) to interact with databases, making it a popular choice for web applications, data analysis, and backend systems. The Relationl database is used to organise the data into tables with rows and columns.

***Explaining the step by step process on how to create a SQL database:***

Imagine you have been hired by a small retail business that wants to streamline its operations by creating a new database system. This database will be used to manage inventory, sales, and customer information. The business is a small corner shop that sells a range of groceries and domestic products. It might help to picture your local convenience store and think of what they sell. They also have a loyalty program, which you will need to consider when deciding what tables to create.

***1.	Understanding the Business Requirements:
a.	What kind of data will the database need to store?
b.	Who will be the users of the database, and what will they need to accomplish?***
In this retail scenario, the database must manage Inventory, Sales, Customer information, and Loyalty Points. The Inventory data includes Product Names, Prices, and quantities. The Sales data includes the sales data records, items sold and totals. The Customers data include Customers information, contact details, and Loyalty Points. The Users of the system include Store Managers, Cashiers, Office staff who will need to add new products, record sales, update inventory, and manage customer information and customer activities.

***2.	Designing the Database Schema:
a.	How would you structure the database tables to efficiently store inventory, sales, and customer information?
b.	What relationships between tables are necessary (e.g., how sales relate to inventory and customers)?***
The next step is to design a Schema for the database by creating tables. To create the tables, first we need to create a database and then create separate tables for Inventory (Product), Sales and Customers. In this the Inventory (Product) table would contain columns for ProductID which is the primary key, ProductName, Price, and Quantity. The Customers table contain CustomerID(PK), FirstName, LastName, Phone, Loyalty Points. The Sales Table Would contain SaleID, Sale Date, Amount, and a foreign key linking to Customers table, while the Sales Details table would record the details of each sale. The relationships between these tables are essential. Example: The Sales table has a one-to-many relationship with the Sale Details table because each sale can involve multiple products. Similarly, the Customers table is linked to the Sales table through a Foreign key, establishing which customer made a particular purchase.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/Retail%20sales%20schema.png)

***3.	Implementing the Database:
a.	What SQL commands would you use to create the database and its tables?
b.	Provide examples of SQL statements for creating tables and defining relationships between them.***
Implementing the Database:
CREATE DATABASE RetailDB;
USE RetailDB;
Then, create the tables:
CREATE TABLE Products( ProductID INT Primary Key, ProductName Varchar (100), Price Decimal (10, 2), Quantity INT);
CREATE TABLE Customers( CustomerID INT Primary key, FirstName Varchar (50), LastName Varchar (50), Phone Varchar (15), LoyaltyPoints INT Default 0);
CREATE TABLE Sales (SaleID INT primary key, SaleDate Date, Amount Decimal (10, 2), CustomerID INT, 
Foreign key (CustomerID) References Customers (CustomerID));
CREATE TABLE SalesDetails ( SaleID INT, ProductID INT, Quantity INT, Price Decimal (10, 2),
Primary key (SaleID, ProductID),
Foreign Key (SaleID) References Sales (SaleID),
Foreign Key (ProductID) References Products (ProductID)

***4.	Populating the Database:
a.	How would you input initial data into the database? Give examples of SQL INSERT statements.***
Populating the Database: It can be done using SQL insert Statements,
INSERT INTO Products (ProductID, ProductName, Price, Quantity)
VALUES (1, ‘Milk’, 1.99, 100);
INSERT INTO Customers (CustomerID, FirstName, LastName, Phone, LoyaltyPoints) VALUES (1, ‘John’, ‘Deo’, ‘1234567890’, 50);
INSERT INTO Sales (SaleID, SaleDate, Amount, CustomerID)
VALUES (1, ‘2025-01-12', 15.75, 1);
INSERT INTO SaleDetails (SaleID, ProductID, Quantity, Price)
VALUES (1, 1, 2, 1.99);

***5.	Maintaining the Database:
a.	What measures would you take to ensure the database remains accurate and up to date?
b.	How would you handle backups and data security?***
Maintaining the Database: Regular updates to product inventories and customer records are necessary, and implementing constraints, indexes, can help maintain data integrity and optimize performance. Scheduled backups and applying security measures such as role-based access control, encryption, and protecting sensitive information with data protection regulations.

**Setting up the database:**

-	Download world_db(1) here ![Data.sql](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/World_db%20Database.sql)
-	Follow each step to create your database here ![Data.sql](https://justit831-my.sharepoint.com/personal/danpe_justit_co_uk/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fdanpe%5Fjustit%5Fco%5Fuk%2FDocuments%2FLearner%20Share%2FData%20%2D%20Week%203%2FIntroduction%20to%20the%20MySQL%20Workbench%2Epdf&parent=%2Fpersonal%2Fdanpe%5Fjustit%5Fco%5Fuk%2FDocuments%2FLearner%20Share%2FData%20%2D%20Week%203&ga=1)

1. Count Cities in USA: Scenario: You've been tasked with conducting a demographic analysis of cities in the United States. Your first step is to determine the total number of cities within the country to provide a baseline for further analysis.
 
![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/World%20DB%20Dataset%20sql%20queries.png)

2.	Country with Highest Life Expectancy: Scenario: As part of a global health initiative, you've been assigned to identify the country with the highest life expectancy. This information will be crucial for prioritising healthcare resources and interventions.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/SQL%20Query4.png)

3.	"New Year Promotion: Featuring Cities with 'New : Scenario: In anticipation of the upcoming New Year, your travel agency is gearing up for a special promotion featuring cities with names including the word 'New'. You're tasked with swiftly compiling a list of all cities from around the world. This curated selection will be essential in creating promotional materials and enticing travellers with exciting destinations to kick off the New Year in style.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/SQL%20Query6.png)

4.	Display Columns with Limit (First 10 Rows): Scenario: You're tasked with providing a brief overview of the most populous cities in the world. To keep the report concise, you're instructed to list only the first 10 cities by population from the database.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/SQL%20Query5.png)

5.	Cities with Population Larger than 2,000,000: Scenario: A real estate developer is interested in cities with substantial population sizes for potential investment opportunities. You're tasked with identifying cities from the database with populations exceeding 2 million to focus their research efforts.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/Name%20and%20population%20from%20city.png)

6.	Cities Beginning with 'Be' Prefix: Scenario: A travel blogger is planning a series of articles featuring cities with unique names. You're tasked with compiling a list of cities from the database that start with the prefix 'Be' to assist in the blogger's content creation process.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/select%20'Be%25'%20like%20from%20city.png)

7.	Cities with Population Between 500,000-1,000,000: Scenario: An urban planning committee needs to identify mid-sized cities suitable for infrastructure development projects. You're tasked with identifying cities with populations ranging between 500,000 and 1 million to inform their decision-making process.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/population%20btw%2050k%20to%20100k.png)

8.	Display Cities Sorted by Name in Ascending Order: Scenario: A geography teacher is preparing a lesson on alphabetical order using city names. You're tasked with providing a sorted list of cities from the database in ascending order by name to support the lesson plan.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/order%20by%20city%20asc.png)

9.	Most Populated City: Scenario: A real estate investment firm is interested in cities with significant population densities for potential development projects. You're tasked with identifying the most populated city from the database to guide their investment decisions and strategic planning.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/population%20limit%20by%20desc.png)

10. City Name Frequency Analysis: Supporting Geography Education Scenario: In a geography class, students are learning about the distribution of city names around the world. The teacher, in preparation for a lesson on city name frequencies, wants to provide students with a list of unique city names sorted alphabetically, along with their respective counts of occurrences in the database. You're tasked with this sorted list to support the geography teacher.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/group%20by%20syntax.png)

11.	City with the Lowest Population: Scenario: A census bureau is conducting an analysis of urban population distribution. You're tasked with identifying the city with the lowest population from the database to provide a comprehensive overview of demographic trends.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/population%20limit%20by%20asc.png)

12.	Country with Largest Population: Scenario: A global economic research institute requires data on countries with the largest populations for a comprehensive analysis. You're tasked with identifying the country with the highest population from the database to provide valuable insights into demographic trends.
 
![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/population%20limit%20by%20desc.png)

13.	Capital of Spain: Scenario: A travel agency is organising tours across Europe and needs accurate information on capital cities. You're tasked with identifying the capital of Spain from the database to ensure itinerary accuracy and provide travellers with essential destination information.
 
![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/Syntax1.png)

14.	Cities in Europe: Scenario: A European cultural exchange program is seeking to connect students with cities across the continent. You're tasked with compiling a list of cities located in Europe from the database to facilitate program planning and student engagement.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/select%20the%20continent%20europe.png)

15.	Average Population by Country: Scenario: A demographic research team is conducting a comparative analysis of population distributions across countries. You're tasked with calculating the average population for each country from the database to provide valuable insights into global population trends.
 
![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/Sub%20Queries.png)

16.	Capital Cities Population Comparison: Scenario: A statistical analysis firm is examining population distributions between capital cities worldwide. You're tasked with comparing the populations of capital cities from different countries to identify trends and patterns in urban demographics.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/Joins.png)

17.	Countries with Low Population Density: Scenario: An agricultural research institute is studying countries with low population densities for potential agricultural development projects. You're tasked with identifying countries with sparse populations from the database to support the institute's research efforts.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/Order%20%20by%20population%20density.png)

18.	Cities with High GDP per Capita: Scenario: An economic consulting firm is analysing cities with high GDP per capita for investment opportunities. You're tasked with identifying cities with above-average GDP per capita from the database to assist the firm in identifying potential investment destinations.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/inner%20join%20syntax.png)

19.	Display Columns with Limit (Rows 31-40): Scenario: A market research firm requires detailed information on cities beyond the top rankings for a comprehensive analysis. You're tasked with providing data on cities ranked between 31st and 40th by population to ensure a thorough understanding of urban demographics.

![Dashboard](https://github.com/Manjukudupudi/Manjukudup/blob/Projects/MySQL/select%20last%2010%20rows.png)







