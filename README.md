# SQL-Script-for-Managing-Sales-Orders-Database

This repository contains an SQL script that demonstrates various operations for managing a database and table structure. The script is designed to work with a database named `Sales` and a table called `Orders` (later renamed to `sales_orders`). It covers a range of Data Definition Language (DDL) and Data Manipulation Language (DML) operations.

## SCRIPT
-- ASSIGNMENT 2-DDL CONSTRAINTS

-- 1.Create a database called 'SALES'
CREATE DATABASE SALES;
-- 2.Switch to Sales
USE SALES;
-- 3.Create Table
CREATE TABLE Orders (
    Order_Id INT PRIMARY KEY, -- Primary Key
    Customer_name VARCHAR(100) NOT NULL, -- Not Null
    Product_Category VARCHAR(50),
    Ordered_item VARCHAR(100) NOT NULL,
    Contact_No VARCHAR(15) UNIQUE -- Unique Constraint
);
-- 4. Add a new column named "order_quantity" to the Orders table
ALTER TABLE Orders
ADD order_quantity INT;
-- 5. Rename the Orders table to sales_orders
RENAME TABLE ORDERS TO SALES_ORDERS;
-- 6. Insert 10 rows into the sales_orders table
INSERT INTO sales_orders (Order_Id, Customer_name, Product_Category, Ordered_item, Contact_No, order_quantity)
VALUES 
(1, 'John Doe', 'Electronics', 'Laptop', '1234567890', 1),
(2, 'Jane Smith', 'Apparel', 'T-Shirt', '2345678901', 2),
(3, 'Emily Johnson', 'Electronics', 'Smartphone', '3456789012', 1),
(4, 'Michael Brown', 'Groceries', 'Apples', '4567890123', 5),
(5, 'Chris Davis', 'Furniture', 'Chair', '5678901234', 1),
(6, 'Sarah Wilson', 'Electronics', 'Headphones', '6789012345', 2),
(7, 'David Martinez', 'Books', 'Novel', '7890123456', 3),
(8, 'Emma Garcia', 'Groceries', 'Bananas', '8901234567', 6),
(9, 'Sophia Lopez', 'Apparel', 'Jacket', '9012345678', 1),
(10, 'Daniel Hall', 'Furniture', 'Table', '0123456789', 1);
SELECT*FROM SALES_ORDERS;

-- 7. Retrieve customer_name and Ordered_item from the sales_orders table
SELECT Customer_name, Ordered_item FROM sales_orders;


-- 8. Update the name of the product for any row
UPDATE sales_orders SET Ordered_item = 'Gaming Laptop' WHERE Order_Id = 1;
SELECT * FROM SALES_ORDERS;

-- 9. Delete the sales_orders table from the database
DROP TABLE sales_orders;


## Features
The script performs the following tasks:
1. **Database Creation**: Creates a new database named `Sales`.
![image](https://github.com/user-attachments/assets/94cb3fc1-b9a2-4729-8419-eac306b4438f)

2.**Use Sales Table**:  Switches to database `Sales`.
![image](https://github.com/user-attachments/assets/9026d814-fff3-403e-a029-b127cd36aacf)

3. **Table Creation**: Creates a table `Orders` with the following columns:
   - `Order_Id` (Primary Key)
   - `Customer_name` (Not Null)
   - `Product_Category`
   - `Ordered_item` (Not Null)
   - `Contact_No` (Unique)
![image](https://github.com/user-attachments/assets/e7c55511-6400-470d-bf46-c6d56199ace6)

4. **Adding a Column**: Adds a new column `order_quantity` to the `Orders` table.
   ![image](https://github.com/user-attachments/assets/1dcc7994-3b10-4118-86a7-ae92edcc1f11)

5. **Renaming the Table**: Renames the `Orders` table to `sales_orders`.
![image](https://github.com/user-attachments/assets/93cfe540-9e27-4ce0-81e5-61ceb6fe1f73)
  
6. **Inserting Data**: Inserts 10 sample rows into the `sales_orders` table.
   ![image](https://github.com/user-attachments/assets/a0901937-5880-4220-aec6-42783b9c9729)
   ![image](https://github.com/user-attachments/assets/cab7a423-a2ef-4ed1-92fa-aa979cd5c78e)

7. **Retrieving Data**: Retrieves `Customer_name` and `Ordered_item` columns from the `sales_orders` table.
   ![image](https://github.com/user-attachments/assets/3d6e27ab-d85b-4436-aaa7-ea99d8377758)

8. **Updating Data**: Updates the `Ordered_item` column for a specific row.
   ![image](https://github.com/user-attachments/assets/e09c104c-ec03-4b9f-aca8-947ab8e3e780)

9. **Deleting the Table**: Deletes the `sales_orders` table from the database.
![image](https://github.com/user-attachments/assets/71e7f40e-921d-4492-9d6b-00af77a62ed6)

## Prerequisites
- A database management system (DBMS) such as MySQL or SQL Server.
- A SQL client tool to run the script (e.g., MySQL Workbench, SSMS).

## How to Use
1. Clone this repository to your local machine:
  https://github.com/LianaSimon/SQL-Script-for-Managing-Sales-Orders-Database/edit/main/README.md
OR Copy the above script and run it in your MYSQL workbench:

## Notes
Make sure the database does not already exist before running the script to avoid conflicts.
Review the script carefully and customize it as needed for your requirements.

## Contributing
Feel free to submit issues or pull requests to improve this script. Contributions are always welcome!

## Contact
For any questions or support, please contact lianasimon77@gmail.com
