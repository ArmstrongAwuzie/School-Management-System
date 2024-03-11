
#School Management System Database
This repository contains SQL code for creating a simple school management system database. The database schema includes tables for managing students, courses, and their enrollments.


Overview
This database schema is designed to manage information about students, courses, and their enrollments. It allows you to perform operations such as adding students and courses, enrolling students in courses, updating student information, removing course enrollments, and querying information about students and courses.

Database Schema
The database consists of the following tables:

Students: Stores information about students including their ID, first name, last name, and grade level.

CREATE TABLE Students (
    StudentID INT IDENTITY(001, 1) PRIMARY KEY,
    FirstName NVARCHAR(50),
    LastName NVARCHAR(50),
    GradeLevel INT
);
Courses: Contains information about different courses offered by the school.

CREATE TABLE Courses (
    CourseID INT IDENTITY(101, 1) PRIMARY KEY,
    CourseName NVARCHAR(100)
);
Enrolments: Manages the many-to-many relationship between students and courses. It stores enrollment records with references to both the student and the course they are enrolled in.

CREATE TABLE Enrolments (
    EnrollmentID INT IDENTITY(1, 1) PRIMARY KEY,
    StudentID INT,
    CourseID INT,
    FOREIGN KEY (StudentID) REFERENCES Students(StudentID),
    FOREIGN KEY (CourseID) REFERENCES Courses(CourseID)
);
Usage
Clone the repository or copy the SQL code into your database management tool.
Execute the SQL code to create the database schema and populate it with sample data.
Use the provided SQL statements to perform operations on the database, such as adding, updating, or querying student and course information.
Feel free to modify the SQL code or database schema to suit your specific requirements. If you encounter any issues or have questions, please don't hesitate to reach out for assistance.

