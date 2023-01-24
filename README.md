# mysql-crash-course
To install MySQL on Ubuntu using the terminal, you can follow these steps: 

Update the package list: 

sudo apt-get update 
 

Install the MySQL server package: 

Copy code 

sudo apt-get install mysql-server 
 

Run the MySQL secure installation script to set the root password and configure other security settings: 

sudo mysql_secure_installation 
 

Start the MySQL service: 

sudo service mysql start 
 

Log in to the MySQL command line as the root user: 

mysql -u root -p 
 

Once you are logged in, you can create a new database with the following command: 

CREATE DATABASE db_name; 
 

You can then create a table within that database with the following command: 

USE db_name; 
CREATE TABLE table_name (column1 datatype(size), column2 datatype(size), column3 datatype(size)); 
 

To link tables, you can use the FOREIGN KEY constraint. For example, to link a table called "orders" to a table called "customers" you would use the following command: 

USE db_name; 
ALTER TABLE orders ADD FOREIGN KEY (customer_id) REFERENCES customers(customer_id); 
 

This command would add a foreign key constraint on the "orders" table, linking the "customer_id" column to the "customer_id" column on the "customers" table. 

 
