---
outline: deep
---

# Database Management System (DBMS)

A Database Management System (DBMS) is software that enables users to define, create, maintain, and control access to databases. It serves as an intermediary between users/applications and the database, ensuring that data is consistently organized and remains easily accessible. The DBMS handles the interaction between the end user and the database, facilitating data management tasks such as data retrieval, insertion, updating, and deletion while ensuring data security, integrity, and consistency.

## Key Functions of a DBMS
1. **Data Definition**: Enables the definition of the database structure, schema, and data types.
2. **Data Manipulation**: Facilitates data retrieval, insertion, modification, and deletion using query languages like SQL.
3. **Data Security and Integrity**: Ensures that only authorized users have access to the database and maintains data integrity.
4. **Data Recovery and Backup**: Provides mechanisms for recovering data in case of failures and supports regular backups.
5. **Concurrency Control**: Manages simultaneous data access by multiple users, ensuring data consistency and integrity.

## Example of a DBMS

Consider a university's student information system. The database schema might include tables like `Students`, `Courses`, and `Enrollments`. Here's a simplified example:

### 1. Data Definition

Creating the tables using SQL:
```sql
CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    birthdate DATE
);

CREATE TABLE Courses (
    course_id INT PRIMARY KEY,
    course_name VARCHAR(100),
    credits INT
);

CREATE TABLE Enrollments (
    enrollment_id INT PRIMARY KEY,
    student_id INT,
    course_id INT,
    enrollment_date DATE,
    FOREIGN KEY (student_id) REFERENCES Students(student_id),
    FOREIGN KEY (course_id) REFERENCES Courses(course_id)
);
