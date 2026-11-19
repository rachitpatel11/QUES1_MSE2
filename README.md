# Q1 – Order Management System using Java JDBC & MySQL

A menu-driven Order Management System developed using **Core Java, JDBC, Maven and MySQL** as part of the KIET CS336B MSE-II assignment.

## Project Overview

This application manages e-commerce orders through a simple console-based interface. It connects to a MySQL database using JDBC and performs essential database operations such as insertion, searching, updating, calculating order values and conditional deletion.

## Features

- **Insert Orders:** Insert three predefined sample orders into the database.
- **Search Orders:** Search orders by status with quantity greater than 2, sorted by unit price in descending order.
- **Increase Quantity:** Increase the quantity of an existing order.
- **Update Order Status:** Update order status with validation.
- **Calculate Total Value:** Calculate the total order value using SQL aggregate functions.
- **Conditional Deletion:** Delete orders only when their status is Cancelled.
- **Duplicate Handling:** Handle duplicate order IDs without crashing.

## Technologies Used

- Java 17
- JDBC (Java Database Connectivity)
- MySQL
- Maven
- IntelliJ IDEA

## Project Structure

```text
OrderManagement-JDBC/
│
├── pom.xml
├── README.md
│
├── database/
│   └── schema.sql
│
└── src/
    └── main/
        └── java/
            └── com/kiet/orders/
                ├── Main.java
                ├── DBConnection.java
                ├── Order.java
                └── OrderDAO.java
```

## Database Configuration

Database Name: `ecommerce_db`

Table Name: `Orders`

| Column | Data Type |
|---|---|
| order_id | INT (Primary Key) |
| customer_name | VARCHAR(100) |
| product_name | VARCHAR(100) |
| quantity | INT |
| unit_price | DOUBLE |
| status | VARCHAR(30) |

Execute `database/schema.sql` in MySQL Workbench to create the database and table.

## Setup and Execution

1. Install JDK 17 and MySQL.
2. Clone or download this repository.
3. Open the project in IntelliJ IDEA.
4. Load the Maven dependencies.
5. Execute `database/schema.sql` in MySQL Workbench.
6. Configure the following environment variables in IntelliJ Run Configuration:

```text
DB_URL=jdbc:mysql://localhost:3306/ecommerce_db?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC
DB_USER=root
DB_PASSWORD=your_mysql_password
```

7. Run `Main.java`.

## Application Menu

```text
===== ORDER MANAGEMENT SYSTEM =====

1. Insert three sample orders
2. Search orders by status
3. Increase order quantity
4. Update order status
5. Display total order value
6. Delete order (only if Cancelled)
7. Exit
```

## Concepts Demonstrated

- JDBC database connectivity
- PreparedStatement
- SQL CRUD operations
- Exception handling
- Try-with-resources
- Object-Oriented Programming
- SQL WHERE and ORDER BY clauses
- Aggregate functions (SUM)
- Input validation

## Author

Developed as part of the KIET CS336B MSE-II assignment.
