# Database Setup Guide (MySQL)

This project uses **MySQL** as the database.  
Follow this guide to create the database and required tables locally.

---

## 1. Prerequisites

- MySQL Server (5.7+ or 8.x)
- MySQL CLI / Workbench / phpMyAdmin
- MySQL user credentials

---

## 2. Create Database

```sql
CREATE DATABASE billing_app;
USE billing_app;
```

---

## 3. Create Tables

### 3.1 users

```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100),
    phone_no VARCHAR(20),
    email VARCHAR(100),
    password VARCHAR(100),
    role ENUM('staff', 'admin')
);
```

---

### 3.2 shop

```sql
CREATE TABLE shop (
    id INT AUTO_INCREMENT PRIMARY KEY,
    pro_name VARCHAR(200),
    price DECIMAL(10,2),
    quantity INT,
    category VARCHAR(100),
    img_url TEXT
);
```

---

### 3.3 customer

```sql
CREATE TABLE customer (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    phone_no VARCHAR(20),
    email VARCHAR(100),
    payment_method ENUM('cash', 'upi_online'),
    total_amount DECIMAL(10,2)
);
```

---

### 3.4 orders

```sql
CREATE TABLE orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    product_id INT,
    quantity INT,
    price DECIMAL(10,2),
    FOREIGN KEY (customer_id) REFERENCES customer(id),
    FOREIGN KEY (product_id) REFERENCES shop(id)
);
```

---

## 4. Verify

```sql
SHOW TABLES;

DESCRIBE users;
DESCRIBE shop;
DESCRIBE customer;
DESCRIBE orders;

```
