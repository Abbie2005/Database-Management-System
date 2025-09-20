LibraryDB Project
Overview

This project creates a simple Library Management System database using MySQL. It includes tables for managing Books, Authors, Members, and Loans, with support for many-to-many relationships between books and authors.

The database allows you to:
Store information about authors and books.
Track library members and their loaned books.
Maintain which authors wrote which books (many-to-many relationship).

Database Structure

Authors Table
Stores information about authors.
Columns: AuthorID, FirstName, LastName.
Books Table
Stores information about books.
Columns: BookID, Title, ISBN, PublishedYear, CopiesAvailable.
BookAuthors Table

Handles the many-to-many relationship between books and authors.

Columns: BookID, AuthorID.

Members Table

Stores library member information.

Columns: MemberID, FirstName, LastName, Email, JoinDate.

Loans Table

Tracks books loaned to members.

Columns: LoanID, BookID, MemberID, LoanDate, ReturnDate.

How to Use
Open MySQL Workbench or command line.
Create the database and tables by running the LibraryDB.sql file:

source path_to_your_file/LibraryDB.sql;


Check tables and data:

SHOW TABLES;
SELECT * FROM Books;
SELECT * FROM Authors;


Test adding, updating, or querying data using standard SQL commands.

Sample Data

3 Authors: J.K. Rowling, George Orwell, F. Scott Fitzgerald

3 Books: Harry Potter, 1984, The Great Gatsby

2 Members: John Doe, Jane Smith

2 Loan Records for testing purposes

Notes

The BookAuthors table ensures that one book can have multiple authors and one author can write multiple books.

Foreign key constraints are included to maintain data integrity.