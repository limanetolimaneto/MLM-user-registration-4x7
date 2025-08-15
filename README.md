# MLM User Registration 4X7

_Simulated User Registration MLM System_

![PHP](https://img.shields.io/badge/PHP-8.2-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

---

# 📝 Description

A PHP, MySQL, and JavaScript implementation for user registration in a 4x7 MLM matrix structure. Users are organized in a tree where each node can have up to 4 children and the structure can grow up to 7 levels deep.

---

# 🚀 Features

✅ User registration in a 4x7 MLM matrix

✅ Automatic parent assignment (max 4 children per parent)

✅ Level tracking for each user

✅ Multiple matrices support

✅ Basic frontend with JavaScript for interaction

---

# 💾 Database Structure

users table with fields:

id (PRIMARY KEY)

name

email (unique)

parent_id

level

matrix_id

created_at



## 💾 Database Setup

Create the `users` table:
```sql

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    parent_id INT DEFAULT NULL,
    level INT NOT NULL,
    matrix_id INT NOT NULL,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (parent_id) REFERENCES users(id)
);
```
---

# ⚡ Installation

Clone the repository

Create MySQL database and import tables

Open terminal in project folder

Run php -S localhost:8000 router.php

Open browser at http://localhost:8000

---

# 🎯 Usage

Fill the registration form

New users will be automatically placed in the matrix

The tree structure grows up to 7 levels

---

# 📈 Future Improvements

Visualization of the full 4x7 matrix

Commission calculation based on levels
User search and reporting

