# Exam Software

Exam Software is a Python-based application that allows teachers to create and manage exams while students can participate in and view their scores. The software uses MySQL as its database to store questions, student details, and scores. The application provides separate functionalities for students and teachers, allowing a smooth and organized testing environment.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Database Setup](#database-setup)

## Features

### For Students
- Login with a unique roll number
- View a personalized menu with options to:
  - Start a test
  - View their score
  - Exit the application

### For Teachers
- Create a teacher account with a secure Employee ID and password
- Login with Employee ID and password
- Access a menu with options to:
  - Add, update, or delete questions from the exam
  - View the full exam question list
  - Add, edit, or remove student information
  - View the class list
  - Exit the application

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/revachoudha/Exam-Software.git
    ```
2. **Navigate to the project directory**:
    ```bash
    cd Exam-Software
    ```
3. **Install required libraries**:
    This project uses the `mysql-connector-python` library to connect to the MySQL database. Install it with:
      ```bash
      pip install mysql-connector-python
      ```
      
## Usage

1. Run the application:
   ```bash
   python Python_Project.py_20210616.py

2. Follow the prompts to log in as a student or teacher.

3. **Student Menu Options**:
   - Start a test and answer the displayed questions.
   - View your score for completed exams.

4. **Teacher Menu Options**:
   - Add, edit, or delete questions in the test.
   - Manage student information, including adding, editing, or removing student profiles.
   - Display the class list.

## Database Setup

The application uses a MySQL database. Follow these steps to set up the database:

1. **Create a database** in MySQL:
    ```sql
    CREATE DATABASE python_project;
    ```

2. **Create the necessary tables**:
    ```sql
    USE python_project;

    CREATE TABLE Teacher (
        EmployeeID VARCHAR(50) PRIMARY KEY,
        Password VARCHAR(50),
        Name VARCHAR(50)
    );

    CREATE TABLE Student (
        RollNumber INT PRIMARY KEY,
        Name VARCHAR(50),
        GradeLevel INT,
        Score INT DEFAULT 0
    );

    CREATE TABLE Question (
        QuestionNumber INT PRIMARY KEY,
        Question VARCHAR(255),
        Option1 VARCHAR(50),
        Option2 VARCHAR(50),
        Option3 VARCHAR(50),
        Option4 VARCHAR(50),
        Answer CHAR(1)
    );
    ```
