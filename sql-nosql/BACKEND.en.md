<p align="center">
  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/000000/external-coding-web-development-flaticons-lineal-color-flat-icons.png" alt="Coding Icon" />
</p>

## 🔍⭐Key Differences Between SQL and NoSQL 💡
SQL and NoSQL are two different systems used to store data. Both store data, but they do it in different ways.

Data Structure 🗂️

SQL: Data is organized in tables (rows and columns). There are clear relationships between tables. The schema is predefined and fixed.

NoSQL: Data is more flexible; it can be stored as documents (JSON), key-value pairs, graphs, or other formats. Schema is either absent or flexible.

Query Language 📝

SQL: Uses a standardized, powerful language called SQL. Complex queries and relationships are easy to handle.

NoSQL: Each NoSQL database has its own query method. Complex joins like in SQL are generally not supported.

Scalability 📈

SQL: To improve performance, you typically upgrade to a more powerful server (vertical scaling). Horizontal scaling is difficult for large data.

NoSQL: Data is distributed by increasing the number of servers (horizontal scaling). It’s suitable for large and fast-growing datasets.

Data Consistency 🔒

SQL: Data is always consistent and guarantees accuracy (ACID). Preferred in systems like banking.

NoSQL: Sometimes relaxes consistency for better performance (Eventual consistency). Data may not update immediately but becomes consistent over time.

Use Cases 🛠️

SQL: Systems with structured data and complex relationships where data integrity is critical.

NoSQL: Applications requiring flexible data structures and rapid growth; social media, big data, real-time analytics.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐What is a JOIN operation? What’s the difference between INNER JOIN and LEFT JOIN?
JOIN in SQL is used to combine data from multiple tables based on a common column. This column is usually an id or a foreign key. The goal is to display related data in a single result set.

📌 Example: Suppose we have a Customers table and an Orders table. To get a customer’s order information, we use JOIN to combine these two tables.

INNER JOIN 🔍

Returns only the rows that have matching values in both tables.

If there’s no match, the row is not included in the result.

Logic: Intersection set

Example: A list of only the customers who have placed orders.

LEFT JOIN ↔️

Returns all rows from the left table. If there’s no match in the right table, those columns will contain NULL.

Logic: All rows from the left table + data from the right table if it exists

Example: A list of all customers, with empty order information for those who haven’t placed an order.

✅ Difference:

INNER JOIN → Only matching rows ✅

LEFT JOIN → All rows from the left table, add from the right if available, otherwise NULL 🗒️

💡 Pro Tip: Avoid unnecessary LEFT JOINs as they can hurt performance. To find non-matching records, use:

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐What is a Primary Key and a Foreign Key in a Database?
A Primary Key is a column (or set of columns) in a table that uniquely identifies each row. No two rows can have the same value, and it cannot contain NULL.

📌 Example: In a Customers table, customer_id can be the primary key because each customer has a unique ID.

A Foreign Key is a column (or set of columns) in a table that references the primary key in another table. It establishes a relationship between tables and ensures referential integrity.

📌 Example: In an Orders table, customer_id can be a foreign key referencing the customer_id in the Customers table. This links each order to the correct customer.

✅ Difference:

Primary Key → Uniquely identifies rows in its own table ✅

Foreign Key → Establishes a relationship with a primary key in another table 🗒️

💡 Pro Tip:

Every table should have a primary key.

Foreign keys ensure data consistency and prevent orphaned records.

Using indexes on foreign keys speeds up JOIN queries.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐What is Data Normalization?

Data normalization is a method of storing information in a database in an organized, non-redundant, and consistent way. The logic is simple: instead of storing the same information in multiple places, keep the data in one place and link it to other tables. This ensures data consistency and avoids unnecessary storage.

📌 Example: Suppose in an Orders table, the customer name, address, and phone number are repeated for every order. This table is not normalized. By applying normalization, we move customer information to a separate Customers table. Now, each customer’s data is stored only once, and the Orders table links to it using the customer ID.

✅ This way:

Data consistency improves: updates are done in a single place ✅

Storage space is saved ✅

Queries become faster and management easier ✅

💡 The essence of the logic:

“Each piece of data should be stored only once; repeating data should be linked through separate tables.”

📌 Extra tip: Normalization is usually done in steps like 1NF, 2NF, 3NF. However, in some cases, controlled denormalization is preferred for performance reasons.


<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐What are CRUD operations? (Create, Read, Update, Delete)

CRUD refers to the four basic operations that can be performed on a database or an application: Create, Read, Update, Delete. These operations form the foundation of almost all software and data management systems.

Create (Oluştur) ✨
Used to add new data.
📌 Example: When a user fills out and submits a registration form, this operation adds a new user to the database.

Read (Oku) 📖
Used to read or retrieve existing data.
📌 Example: Running a query to view the list of users is a Read operation.

Update (Güncelle) 🔄
Used to modify existing data.
📌 Example: Changing a user's email address is an Update operation.

Delete (Sil) 🗑️
Used to remove existing data from the system.
📌 Example: Permanently deleting a user account is a Delete operation.

✅ In short:

Create → Add new data

Read → Retrieve/view data

Update → Modify existing data

Delete → Remove data

💡 Pro Tip: CRUD operations are often mapped to HTTP methods:

Create → POST

Read → GET

Update → PUT/PATCH

Delete → DELETE

This way, both database and REST API logic are built upon the same core principles.
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=footer&text=Thanks%20for%20visiting!%20🚀&fontSize=30&fontColor=ffffff" />
</p>
