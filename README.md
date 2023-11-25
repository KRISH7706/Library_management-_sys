# Library_management-_sys
The Efficient library management system using SQL and C++. Manage library collection, facilitate user interactions, and generate data-driven insights.
ER diagram and schema, including a description of the relationships between the entities:

Entities:

Student:

Id: Unique identifier for the student.
Data type: VARCHAR(255)
Primary key: Yes
Library:

Name: Unique identifier for the library book.
Data type: VARCHAR(255)
Primary key: Yes
Quantity: Number of copies of the book available.
Data type: INT
Not null: Yes
Relationships:

Student borrows Library:
This is a many-to-many relationship, meaning that a student can borrow multiple books, and a book can be borrowed by multiple students.
This relationship is represented by the student_library join table.
Join Table:

student_library:
Student_Id: Foreign key referencing the Id attribute of the Student table.
Data type: VARCHAR(255)
Library_Name: Foreign key referencing the Name attribute of the Library table.
Data type: VARCHAR(255)
Primary key: The combination of Student_Id and Library_Name uniquely identifies each record in the table.

Example Scenario:
Consider a scenario where a student named Alice wants to borrow a book titled "The Lord of the Rings". The following steps would occur:
Alice would select the book from the available library books.
The librarian would record the transaction in the student_library table, linking Alice's student ID to the book's name.
The quantity of the book in the Library table would be decremented to reflect the borrowed copy.
This process ensures that the system maintains accurate records of which books are borrowed by which students.

SCHEMA :
SQL
CREATE TABLE Student (
  Id VARCHAR(255) PRIMARY KEY
);

CREATE TABLE Library (
  Name VARCHAR(255) PRIMARY KEY,
  Quantity INT NOT NULL
);

CREATE TABLE student_library (
  Student_Id VARCHAR(255) REFERENCES Student(Id),
  Library_Name VARCHAR(255) REFERENCES Library(Name),
  PRIMARY KEY (Student_Id, Library_Name)
);
