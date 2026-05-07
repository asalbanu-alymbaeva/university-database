🎓 University Database Project
📌 Overview

This project represents a relational database system for a University Management System.
It is designed to manage students, professors, courses (lessons), grades, faculties, and language-based course structures.

The database is built using PostgreSQL and follows normalized relational design principles.

🗂️ Database Architecture

The system consists of the following main entities:

👨‍🎓 Students

Stores student information:

id
firstname
lastname
grade
faculty
🏫 Faculty

Stores faculty information:

id
faculty
code
👨‍🏫 Professors

Stores professor details:

id
firstname
lastname
email
📚 Lessons

Represents university courses:

id
name
hours
auditory
language
🌐 Languages

Stores available teaching languages:

id
language
🧾 Grades

Stores grading reference values:

id
grade
🔗 Relationship Tables
📖 student_lessons

Maps students to lessons (many-to-many relationship):

id
student_id
lesson_id
attended
👨‍🏫 professor_lessons

Maps professors to lessons:

id
professor_id
lesson_id
students_number
🧩 ER Diagram

The database structure is visualized below:

⚙️ Tech Stack
PostgreSQL
SQL (DDL & DML)
Relational Database Design
🚀 How to Use
1. Create Database
CREATE DATABASE university;
2. Restore Database

Using pg_dump file:

psql -U postgres -d university -f university.sql
📌 Key Features
Normalized relational structure
Many-to-many relationships (students ↔ lessons, professors ↔ lessons)
Scalable design for university systems
Clean separation of entities
👩‍💻 Author

Project developed as a practice database for learning PostgreSQL and relational design.
