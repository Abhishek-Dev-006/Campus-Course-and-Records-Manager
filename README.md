### Campus Course Records Manager (CCRM)

## Project Overview

Campus Course Records Manager (CCRM) is a console-based Java SE application designed to help educational institutes manage their academic records effectively. The system allows managing Students, Courses, Enrollments, Grades, and Transcripts using a menu-driven Command Line Interface (CLI).

The project demonstrates key Object-Oriented Programming (OOP) concepts, employs modern Java APIs, incorporates robust exception handling, and applies design patterns to build a maintainable and extensible academic management system.

## Features

# Student Management

- Add new students with registration number, name, email, status, and enrollment date.

- Update existing student data.

- List all students and print detailed profiles.

- Manage active/inactive status for students.

# Course Management

- Add, update, and list courses with attributes including course code, title, credits, department, semester, and assigned instructor.

- Search and filter courses by instructor, department, and semester.

# Enrollment and Grading

- Enroll and unenroll students in/from courses with automatic checks for duplicate enrollment and max credit constraints.

- Record students’ marks, compute and assign letter grades.

- Compute GPA based on course credits and grades.

# Transcript Generation

- Print student transcripts showing course details, marks, grades, and cumulative GPA.

# File Import/Export and Backup

- Import and export student and course data in CSV-like text files.

- Backup application data recursively with timestamped directories using Java NIO.2 API.

# User Interface

- Fully menu-driven CLI enabling easy navigation and interaction.

- Robust input validation and error handling with clear feedback.

## Technologies Used

- Java SE 17

- Java NIO.2 API for file operations

- Java Streams API for data processing

- Java DateTime API for handling dates and time

- OOP principles: encapsulation, inheritance, polymorphism, and abstraction

- Design Patterns: Singleton (for AppConfig), Builder (for Student entity creation)

- Custom exceptions for domain-specific error handling

- Use of enums, nested classes, lambdas, recursion for enhanced functionality

## Project Structure

- edu.ccrm.domain — Domain model classes, enums, and abstract types.

- edu.ccrm.service — Business logic and CRUD operation implementations.

- edu.ccrm.io — File import/export and backup utilities.

- edu.ccrm.util — Configuration and helper utility classes.

- edu.ccrm.cli — CLI classes handling user interaction and menu management.

- edu.ccrm.exceptions — Custom exception classes specific to project requirements.

## Installation and Setup

# Prerequisites:

- Java JDK 17 or later installed on your system.

- Preferred IDE (Eclipse, IntelliJ IDEA) or command line setup.

# Setup:

- Clone or download the source code repository.

- Open the project in your favorite IDE or navigate using terminal.

- Compile the source files maintaining package structure.

# Build:

- In IDE: Build or compile the project normally.

- Command Line Example:

```bash
text
javac -d bin src/edu/ccrm/**/*.java
```

# Run:

- Run the CLI Menu main class:

```bash
text
java -cp bin edu.ccrm.cli.CCRMMenu
```

## Usage Guide

- Navigate the menu using number choices.

- Add and update Students and Courses.

- Enroll Students in Courses with checks for credit limits.

- Record grades after course completion.

- Print transcripts to summarize academic performance.

- Import/export CSV files for data portability.

- Backup data for restoration and archival.

## Sample Commands and Expected Output

# 1. Adding a New Student

```bash
text
-- Student Management --
1. Add New Student
2. List All Students
Enter your choice: 1
Enter ID: 001
Enter Full Name: Abhishek Singh
Enter Email: xyz@gmail.com
Enter Registration Number: abcd1
Student added successfully.
```
# 2. Listing All Students

```bash
text
-- Student Management --
1. Add New Student
2. List All Students
Enter your choice: 2
Student Profile | Name: Alice Johnson | Reg No: S001 | Email: alice@example.com
Student Profile | Name: Bob Williams | Reg No: S002 | Email: bob@example.com
Student Profile | Name: Abhishek Singh | Reg No: abcd1 | Email: xyz@gmail.com
Student Profile | Name: Aditya Singh | Reg No: abcd2 | Email: abc@gmail.com
Student Profile | Name: Saubhagya Srivastava | Reg No: abcd3 | Email: pqr@gmail.com
Student Profile | Name: Adarsh Patel | Reg No: abcd4 | Email: lmn@gmail.com
```

# 3. Listing All Courses

```bash
text
-- Campus Course & Records Manager --
1. Manage Students
2. Manage Courses
3. File Operations
0. Exit
Enter your choice: 2

-- Course Management --
1. List All Courses
Course [CS101: Intro to CS, Credits: 4, Instructor: TBD, Semester: FALL]
Course [MA202: Calculus II, Credits: 3, Instructor: TBD, Semester: SPRING]
```

# 4. Exporting Students to CSV

```bash
text
-- Campus Course & Records Manager --
1. Manage Students
2. Manage Courses
3. File Operations
0. Exit
Enter your choice: 3

-- File Operations --
1. Export All Students to CSV
2. Create a Backup
Enter your choice: 1
Successfully exported 6 students to data\students_export.csv
```

# 5. Creating a Data Backup

```bash
text
-- File Operations --
1. Export All Students to CSV
2. Create a Backup
Enter your choice: 2
Backup created at: backups\backup_20250925_182846
Total size of backup: 0 bytes.
```

# 6. Application Startup and Exit

```bash
text
Application configurations loaded successfully.
-- Campus Course & Records Manager --
1. Manage Students
2. Manage Courses
3. File Operations
0. Exit
Enter your choice: 0
Thank you for using CCRM. Goodbye!

```

## Known Limitations

- CLI interface only (no GUI).

- No persistent database; data is file-based.

- Basic validation; advanced user role management not implemented.

## Future Enhancements

- Develop GUI frontend.

- Integrate with relational database.

- Add report generation and export formats.

- Enhance user role and access controls.

## Author

- Name: Abhishek Singh 

- Date: September 25, 2025
