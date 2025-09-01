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

## 🔍⭐ What is a JOIN? What is the difference between INNER JOIN and LEFT JOIN?
JOIN in SQL is used to combine data from multiple tables through a common column. This column is usually an id or a foreign key. The purpose is to display related data in a single result set.

📌 Example: Suppose there is a Customers table and an Orders table. To get the order information of a customer, we combine these two tables with a JOIN.

INNER JOIN 🔍

Brings only the records that match in both tables.

If there is no match, that row will not appear in the result.

Logic: Intersection set

Example: The list of customers who have placed an order.

LEFT JOIN ↔️

Brings all records from the left table. If there is no match in the right table, those columns will be NULL.

Logic: Entire left table + if right table exists, add extra data

Example: The list of all customers, with empty order information for those who have not placed any orders.

✅ Difference:

INNER JOIN → Only the matching ones ✅

LEFT JOIN → Entire left, add right if exists, otherwise empty 🗒️

💡 Tip: Unnecessary LEFT JOIN decreases performance. To find unmatched records, the technique

LEFT JOIN ... WHERE right_table.column IS NULL


is commonly used. On large datasets, using indexes speeds up the query.

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

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐ Key Points to Consider in Database Design

1️⃣ Choosing the Right Data Structure 🏗️

Tables, fields (columns), and data types should be defined correctly.

Avoid extra columns or redundant/repetitive data.

2️⃣ Normalization 📚

Data should be organized to prevent duplication.

Each piece of information must be stored in only one place, and relationships should be established using foreign keys.

3️⃣ Establishing Proper Relationships 🔗

One-to-One, One-to-Many, and Many-to-Many relationships must be clearly defined.

Primary Keys and Foreign Keys should be used appropriately.

4️⃣ Data Consistency and Integrity ✅

Constraints (NOT NULL, UNIQUE, CHECK) should be applied to prevent invalid data entry.

Referential integrity should be maintained with foreign keys.

5️⃣ Performance and Indexing ⚡

Indexes should be added to frequently queried columns.

Avoid unnecessary indexes (too many indexes → slower write operations).

6️⃣ Security 🔒

Sensitive data (passwords, credit card details) should be encrypted.

Authorization and access control must be implemented.

7️⃣ Scalability and Flexibility 📈

Database design should anticipate future growth of data.

New tables or fields should be easily addable when needed.

8️⃣ Backup and Recovery Plan 🗄️

A regular backup strategy should be in place to prevent data loss.

💡 Core Principle:
Good database design = non-redundant data + proper relationships + consistency + performance + security.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐🔐 What is SQL Injection?

SQL Injection is one of the most dangerous and most common security vulnerabilities in web applications.

Simply put: SQL Injection happens when user input (e.g., login forms, search boxes, URL parameters) is directly added into an SQL query without proper validation, allowing the attacker to inject and execute their own SQL commands.

💡 Think of it like this: Your app tells the database “fetch only specific data,” but the attacker slips in their own sentence saying, “do your query AND also run this extra command.”

⚠️ Why is it Dangerous?

🔓 Data can be leaked: The attacker may access all table data (usernames, passwords, emails).

✏️ Data can be modified: Fake records can be inserted, existing ones updated, or deleted entirely.

🚪 Unauthorized access can be gained: The attacker can access restricted data or even escalate privileges to admin level.

💥 The system can crash completely: If critical tables are dropped, the application may become unusable.

🔍 Most Sensitive Points

🚫 User input is never trustworthy.
→ Even a simple OR '1'='1' statement can expose all users.

❌ String concatenation is the biggest mistake.
Example:

"SELECT * FROM users WHERE username = '" + input + "';"


If user input is directly appended to the query → you’re fully exposed.

🌐 Not only login forms: URL parameters, cookies, and even HTTP headers can be exploited.

🕵️ Leaky error messages give clues.
→ Showing database error details helps attackers learn about your system structure.

🛡️ How to Prevent It?

✅ Use prepared statements (parameterized queries):
Values are separated from SQL commands → attackers cannot alter the query structure.

🏗️ Prefer ORM or secure query methods in frameworks:
E.g., Hibernate, Django ORM, Entity Framework.

🔍 Validate input:
Only accept expected formats. For example, if an ID is required → accept only numbers.

🔑 Apply the principle of least privilege:
The database user your app connects with should not have unnecessary permissions (e.g., DROP, ALTER).

🚫 Hide error messages:
Do not expose raw SQL errors → return a generic error message instead.

🧪 Perform security testing:
Use tools (e.g., SQLMap) or manual penetration tests to ensure safety.

🧩 Summary Logic

👉 The essence of SQL Injection is this:
“User input must never become part of the query itself — it should only be a parameter of the query.”

If you follow this rule, you eliminate one of the most critical security risks. ✅

## 🔍⭐ What is an Index and Why is it Important in Databases?

An index is a special data structure used in databases to speed up search and query operations.
The simplest analogy is the alphabetical index at the end of a book. Instead of reading every single page to find a topic, you check the index → and directly go to the relevant page.
A database index works in the same way.

🔍 Why is it Important?

⚡ Increases query speed:
In large tables with millions of rows, retrieving data can take a long time. With indexes, the desired row can be accessed much faster.

📉 Optimizes performance:
Especially in queries like SELECT, WHERE, and JOIN, indexes reduce system resource usage when working with large datasets.

🛠️ Facilitates sorting and searching:
Operations like ORDER BY and GROUP BY run more efficiently with indexes.

⚠️ Things to Watch Out For

❌ Not every column should have an index.
Since an index is also a data structure, it consumes additional storage space.

✏️ INSERT, UPDATE, and DELETE operations may slow down.
Because whenever data changes, the index also needs to be updated.

🎯 Use them in the right place.
Indexes are most useful on columns that are frequently searched or filtered (commonly used in WHERE clauses).

🧩 Summary

👉 Index = “A guide built to find data faster.”
If you’re facing performance issues in large tables, well-designed indexes can boost your queries dramatically. 

  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=footer&text=Thanks%20for%20visiting!%20🚀&fontSize=30&fontColor=ffffff" />
</p>
