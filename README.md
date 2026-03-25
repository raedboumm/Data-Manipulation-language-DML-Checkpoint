# SQL DML - Data Insertion Script

This repository contains SQL `INSERT` statements for populating three tables: **Customer**, **Product**, and **Orders**, based on the provided relational model.

## Table Structures

### Customer
| Column          | Type         |
|-----------------|--------------|
| Customer_id     | VARCHAR2(10) |
| customer_Name   | VARCHAR2(50) |
| customer_Tel    | VARCHAR2(20) |

### Product
| Column        | Type          |
|---------------|---------------|
| Product_id    | VARCHAR2(10)  |
| product_name  | VARCHAR2(50)  |
| category      | VARCHAR2(20)  |
| Price         | NUMBER(8,2)   |

### Orders
| Column        | Type          |
|---------------|---------------|
| Customer_id   | VARCHAR2(10)  |
| Product_id    | VARCHAR2(10)  |
| OrderDate     | DATE          |
| quantity      | NUMBER        |
| total_amount  | NUMBER(10,2)  |

## Inserted Data

### Customer
| Customer_id | customer_Name | customer_Tel |
|-------------|---------------|--------------|
| C01         | ALI           | 71321009     |
| C02         | ASMA          | 77345823     |

### Product
| Product_id | product_name         | category    | Price |
|------------|----------------------|-------------|-------|
| P01        | Samsung Galaxy S20   | Smartphone  | 3299  |
| P02        | ASUS Notebook        | PC          | 4599  |

### Orders
| Customer_id | Product_id | OrderDate   | Quantity | total_amount |
|-------------|------------|-------------|----------|--------------|
| C01         | P02        | NULL        | 2        | 9198         |
| C02         | P01        | 28/05/2020  | 1        | 3299         |

## SQL Commands

```sql
-- Insert into Customer
INSERT INTO Customer (Customer_id, customer_Name, customer_Tel) VALUES ('C01', 'ALI', '71321009');
INSERT INTO Customer (Customer_id, customer_Name, customer_Tel) VALUES ('C02', 'ASMA', '77345823');

-- Insert into Product
INSERT INTO Product (Product_id, product_name, category, Price) VALUES ('P01', 'Samsung Galaxy S20', 'Smartphone', 3299);
INSERT INTO Product (Product_id, product_name, category, Price) VALUES ('P02', 'ASUS Notebook', 'PC', 4599);

-- Insert into Orders
INSERT INTO Orders (Customer_id, Product_id, OrderDate, quantity, total_amount) VALUES ('C01', 'P02', NULL, 2, 9198);
INSERT INTO Orders (Customer_id, Product_id, OrderDate, quantity, total_amount) VALUES ('C02', 'P01', TO_DATE('28/05/2020', 'DD/MM/YYYY'), 1, 3299);
