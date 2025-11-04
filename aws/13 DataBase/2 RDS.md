## AWS RDS (Relational Database Service):
```sh
AWS RDS is a managed relational database service that makes it easy to set up, operate, and scale relational databases in
the cloud.
It supports multiple database engines, including MySQL, PostgreSQL, Oracle, SQL Server, and Amazon Aurora.
```
## RDS Components:
```sh
DB Instance: A running database environment managed by RDS.
DB Engine: The database software running on the DB instance.
Parameter Group: A set of parameters and settings that control the behavior of the DB engine.
Option Group: A collection of features and settings that can be applied to a DB instance.
DB Parameter Group: A collection of database engine parameter values that can be applied to one or more DB instances.
DB Security Group: A virtual firewall that controls inbound and outbound traffic for your DB instance.
DB Subnet Group: A collection of subnets in your VPC.
Backup: A copy of your data that you can use to restore your database to a specific point in time.
```
## Advantages of using RDS include:
```sh
Automated backups and point-in-time recovery.
Scaling capabilities to handle increased workloads.
Security features such as encryption at rest and in transit.
Automated software patching and maintenance.
Multi-AZ deployment for high availability and fault tolerance.
```
## Use Cases
```sh
Use cases for RDS in the real world include:
	Hosting web applications with MySQL, PostgreSQL, or SQL Server databases.
	Running enterprise applications that require a reliable and scalable database backend.
	Storing and analyzing business data for reporting and decision-making.
	Building e-commerce platforms with a robust and scalable database infrastructure.
```
## Demo
### Create a mysql database
```sh
1. Create a Database instance in Mumbai Region as per the below requirement.

	Database Instance Identifier	   - testdb                             
	Database MAster  Name	    -   admin
	Master PAssword    -  Passowrd
	instance type		-         db.t3.micro
	Storage		      - 25 GB of gp3
	Deployment Method	-      Single-AZ Deployment
	Database ENgine		- MySQL (latest Version/Recommended)
	Automated Snapshots	- Enable at 06:30AM IST everyday
	Retention Period	- 7 Days
```
### Connect from ec2/local laptop
```sh
Download Microsoft’s Visual C++ 2019 Redistributable: 	https://aka.ms/vs/17/release/vc_redist.x64.exe
Download MySQL WorkBench: https://dev.mysql.com/downloads/workbench/
Login to the MySQL Database instance and create a table "StudentDetails" and load some sample data. (10 entries)
yum list all | grep -i client | grep -i mariadb
		mysql -h mydatabaseinstance.crwuc8ai6oma.us-east-1.rds.amazonaws.com -u admin -padmin12345
```
### Create the structure
```sh
CREATE DATABASE school;
USE school;

 CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(255),
    age INT,
    gender VARCHAR(10),
    grade VARCHAR(2)
);
```
### Insert the data
```sh
INSERT INTO students (id, name, age, gender, grade) VALUES
(1, 'Alice', 18, 'Female', 'A'),
(2, 'Bob', 17, 'Male', 'B'),
(3, 'Charlie', 16, 'Male', 'C'),
(4, 'Diana', 17, 'Female', 'A'),
(5, 'Eve', 18, 'Female', 'B'),
(6, 'Frank', 16, 'Male', 'C'),
(7, 'Grace', 17, 'Female', 'A'),
(8, 'Harry', 18, 'Male', 'B'),
(9, 'Ivy', 16, 'Female', 'C'),
(10, 'Jack', 17, 'Male', 'A');

Select * from students
```




