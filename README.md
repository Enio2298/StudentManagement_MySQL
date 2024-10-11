# StudentManagement MySQL

This is a desktop-based application built with PyQt6 for managing student records. It connects to a MySQL database to store, update, delete, and search for student records. The application provides a graphical user interface (GUI) for ease of use.
Features

    Add Students: Add new student records, including their name, course, and mobile number.
    Edit Students: Edit existing student records.
    Delete Students: Remove a student record from the database.
    Search Students: Search for a student by name.
    Table Display: Display all students in a tabular format.

Prerequisites

Before you run the application, make sure you have the following installed:

    Python 3.x: Make sure Python is installed on your system.
    PyQt6: GUI toolkit for Python.
    MySQL Server: A MySQL server to store the student records.
    MySQL Connector: Python library to connect to the MySQL database.

Python Package Installation

You can install the required Python packages using pip:

bash

pip install PyQt6 mysql-connector-python

MySQL Setup

Create a MySQL database and a table to store the student records:

sql

CREATE DATABASE school;

USE school;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    course VARCHAR(100),
    mobile VARCHAR(15)
);

You will also need MySQL login credentials, such as host, user, password, and database. The default values used in the code are:

    Host: localhost
    User: root
    Password: You7hanas1
    Database: school

You can change these credentials in the DatabaseConnection class in the code if needed.
How to Run

    Clone the repository (or save the script to a local directory).
    Install the required packages using the pip command above.
    Set up the MySQL database as described in the MySQL Setup section.
    Run the Python script:

bash

python app.py

The PyQt6 application will open, displaying the student management system interface.
Application Overview

The application is built with several key components:
1. MainWindow (Main Application Window)

The MainWindow class sets up the main interface, including a table to display the student data and menus to add, edit, search, or delete students. It also contains a toolbar for easy access to the "Add Student" and "Search Student" functions.
2. Dialogs

The app uses various dialog boxes for inserting, editing, searching, and deleting student records:

    InsertDialog: Used to add a new student to the database.
    EditDialog: Allows updating an existing student’s details.
    DeleteDialog: Confirms the deletion of a student record.
    SearchDialog: Provides a search interface for looking up students by name.
    AboutDialog: Provides basic information about the application.

3. DatabaseConnection

This class manages the connection to the MySQL database, using the MySQL Connector library to interact with the database and perform CRUD operations (Create, Read, Update, Delete).
File Structure

bash

project-folder/
│
├── app.py               # Main application code
├── icons/               # Folder containing icons (add.png, search.png)
└── README.md            # This readme file

Notes

    Icons: Make sure to place any required icons in the icons/ folder, such as add.png and search.png. You can use your own icons if necessary.
    Database Connection: If you’re using different MySQL credentials or database setup, remember to adjust the DatabaseConnection class in the code accordingly.
