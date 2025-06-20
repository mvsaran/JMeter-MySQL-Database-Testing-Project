Meter MySQL Database Testing Project
This project demonstrates how to perform database testing using Apache JMeter by connecting to a MySQL database and running SQL queries.

📁 Folder Structure
graphql
Copy
Edit
JMeter-MySQL-DBTesting/
├── DatabaseTesting.jmx          # JMeter test plan file
├── README.md                    # Project documentation
├── test-data.sql                # Optional SQL script for setup
└── .gitignore

🔧 Setup Instructions
📌 Prerequisites
Apache JMeter (5.6.3 or later)

MySQL Server

JDBC Driver (mysql-connector-java-x.x.xx.jar)

Git

⚙️ JMeter Configuration Steps
Install MySQL JDBC Driver:

Download from MySQL Connector/J

Copy the .jar to JMeter/lib/ directory

Create MySQL DB and Table:

sql
Copy
Edit
CREATE DATABASE mydb;
USE mydb;

CREATE TABLE student (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(50),
  grade VARCHAR(5)
);

INSERT INTO student (name, grade) VALUES ('Alice', 'A'), ('Bob', 'B');
Open DatabaseTesting.jmx in JMeter

Update JDBC Connection Configuration:

URL: jdbc:mysql://localhost:3306/mydb

Driver: com.mysql.cj.jdbc.Driver

Username/Password: Your DB credentials

Run the Test & View Results

🧪 Test Coverage
✅ JDBC SELECT queries

📊 Results Viewers: Tree, Table

🔄 Update/Insert queries can be extended similarly

