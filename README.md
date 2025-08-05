# Data-Insertion-and-Handling-Nulls
 Objective:    Practice inserting, updating, and deleting data.
 
 Deliverables: SQL file with INSERT, UPDATE, DELETE statement.
 
 Hints/Mini Guide:
 
 1.Use INSERT INTO for adding rows
 
 2.Handle missing values using NULL or default
 
 3.Use UPDATE and DELETE with WHERE condition

--Created database with students name.

use Students;

--Creating a students table. 

--This table contain information of students like Studentid,name,age,email

Create table Students(
Studentid int primary key,
Name varchar(100),
Age int,
Email Varchar(100)
);

--Checking the table.
Select * from Students;

--INSERT with Full Data
Insert into Students values (1,'Jasmine',16,'jas20@gmail.com')

--  INSERT with Some Optional Values
Insert into Students(Studentid,name,age) values(2,'Tom handry',15)

--  INSERT with Some missing Values
Insert into students values(3,15)

-- Inser two students data at the same time
Insert into students values
(4,'Ava Green',17,'ava.greem@gmail.com'),
(5,'Noh White',15,'Noha,white@gmail.com');

--Inserting data with with one value
Insert into students values 
(6),
(7);

--Checking the table
Select * from Students;

--Update: Fix name in StudentID = 3
Update students set name = 'Zafar' where Studentid=3

--Update:Fix email typo in StudentID = 4
Update Students set email='ava.green@gmail.com' where studentid=4

--Update:Fix email format in StudentID = 5 (comma to dot)
Update Students set email='Noha.white@gmail.com' where studentid=5

--Update NULL fields in StudentID = 6
Update students set name='John',age=17,email='John@gmail.com'  where studentid=6

--Delete record with NULL name and age (e.g., StudentID = 7)
Delete from students where Studentid=7;

--Delete all students with missing email addresses
Delete from students where email is null;



		


