# 🛒 E-Commerce Data Warehouse – SQL + Python + PostgreSQL Project

This project demonstrates the creation of a mini **data warehouse** for an e-commerce company. It includes **schema design**, **relational table creation in PostgreSQL**, and **automated loading of cleaned datasets** using Python (`psycopg2` and `SQLAlchemy`).

---

## 🧰 Tools & Technologies

- Python 3.x
- PostgreSQL
- SQLAlchemy
- psycopg2
- Pandas
- Jupyter Notebook

---

## 📁 Project Files

| File                     | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| `E-commerce.ipynb`       | Jupyter Notebook with full Python + SQL workflow                   |
| `ERD DIAGRAM.png`        | Entity Relationship Diagram (ERD) of the schema                    |
| `data/*.csv`             | Raw datasets (`orders`, `products`, `departments`, etc.)           |

---

## 🧠 Project Workflow

1. **Read & Sample CSV Files:**
   - Load datasets such as `orders.csv`, `order_products.csv`, `products.csv`, `aisles.csv`, and `departments.csv` using `pandas`.

2. **Connect to PostgreSQL:**
   - Establish a connection to a local PostgreSQL database (`ecom_analysis`) using `psycopg2`.

3. **Create Tables with Relationships:**
   - Define normalized schema with foreign key constraints between `orders`, `products`, `departments`, etc.

4. **Load Data into PostgreSQL:**
   - Use `pandas.to_sql()` with SQLAlchemy to insert data into the database.

5. **Query-ready Warehouse:**
   - Once loaded, the data can be analyzed using SQL for reporting, dashboarding, or analytics.

---

## 🗺️ ERD (Entity Relationship Diagram)

![ERD Diagram](https://raw.githubusercontent.com/dinesh-puppala/Ecommerce-data-analysis-sql-python/main/ERD%20DIAGRAM.png)

---

## 🏗️ PostgreSQL Schema Overview

- **aisles**: `aisle_id`, `aisle`
- **departments**: `department_id`, `department`
- **products**: `product_id`, `product_name`, `aisle_id`, `department_id`
- **orders**: `order_id`, `user_id`, `order_number`, `order_dow`, `order_hour_of_day`, `days_since_prior_order`
- **order_products**: `order_id`, `product_id`, `add_to_cart_order`, `reordered`

> Includes `PRIMARY KEY` and `FOREIGN KEY` constraints for referential integrity

---
