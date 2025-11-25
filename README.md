User Management Application (CRUD

with JDBC)

This project is a simple Java application that demonstrates C.R.U.D. (Create, Read, Update,

Delete) operations on a MySQL database using JDBC. The application features a graphical

user interface (GUI) built with Swing for easy user interaction.

Prerequisites

To run this application, you need the following:

● Java Development Kit (JDK): Version 8 or higher.

● MySQL Database: A running MySQL server.

● MySQL Connector/J: The JDBC driver for MySQL. The mysql-connector-j-9.4.0.jar file is

already included in the project directory.

● Database Schema: A database named userdb with a table named users.

Database Setup

Before running the application, you need to set up the database and table.

1. Create a database named userdb in your MySQL server.

2. Create the users table with the following schema:

CREATE TABLE users (

id INT PRIMARY KEY,

name VARCHAR(255),

email VARCHAR(255),

country VARCHAR(255)

);

3. Update the DBConnection.java file with your MySQL username and password.

private static String jdbcURL =

"jdbc:mysql://localhost:3306/userdb?useSSL=false&serverTimezone=UTC";

private static String jdbcUsername = "your_mysql_username"; // Update this

private static String jdbcPassword = "your_mysql_password"; // Update this

Project Structure

● DBConnection.java: Handles the connection to the MySQL database.

● UserDAO.java: Contains the Data Access Object (DAO) class with methods for C.R.U.D.

operations on the users table.

● UserForm.java: The main class that creates the Swing GUI and handles user input and

actions.

● mysql-connector-j-9.4.0.jar: The MySQL JDBC driver.

How to Run

1. Compile the Java files:

javac -cp .:mysql-connector-j-9.4.0.jar DBConnection.java UserDAO.java UserForm.java

(Note: The -cp flag is used to include the JDBC driver in the classpath.)

2. Run the application:

java -cp .:mysql-connector-j-9.4.0.jar UserForm

The application window will appear, allowing you to insert, view, update, and delete user

records.
