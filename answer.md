1. Definition of a Database Relationship

A database relationship defines how data in one table is connected to data in another table using keys (primary key and foreign key).

In simple terms, it explains how tables depend on each other to store related information efficiently.
Relationships help:

Avoid data duplication

Maintain data integrity

Organize data logically

In an e-commerce application, relationships connect customers, orders, products, payments, and categories.

2. Types of Database Relationships with E-commerce Examples
1. One-to-One Relationship (1:1)
Definition

One record in Table A is linked to only one record in Table B.

E-commerce Example

User ↔ User Profile

Each user has only one profile

Each profile belongs to one user

Example Tables

Users(user_id, email, password)

UserProfiles(profile_id, user_id, address, phone)

Explanation

User login details are stored in the Users table, while personal details are stored in UserProfiles.

 Why used?
To separate sensitive or optional information.

2. One-to-Many Relationship (1:N)
Definition

One record in Table A can be related to many records in Table B.

E-commerce Example

Customer → Orders

One customer can place many orders

Each order belongs to one customer

Example Tables

Customers(customer_id, name)

Orders(order_id, customer_id, order_date)

Explanation

A customer may place multiple orders over time, but an order cannot belong to multiple customers.

 Most common relationship in e-commerce

3. Many-to-One Relationship (N:1)
Definition

Many records in one table are linked to one record in another table.

E-commerce Example

Orders → Customer

Many orders belong to one customer

This is the reverse view of one-to-many.

 Used when querying from child to parent

4. Many-to-Many Relationship (M:N)
Definition

Many records in Table A relate to many records in Table B.
This relationship requires a junction table.

E-commerce Example

Orders ↔ Products

One order can contain many products

One product can be part of many orders

Example Tables

Orders(order_id)

Products(product_id, name, price)

OrderItems(order_id, product_id, quantity)

Explanation

The OrderItems table connects orders and products and stores quantity.

 Very important in shopping carts and order systems

5. Self-Referencing Relationship
Definition

A table has a relationship with itself.

E-commerce Example

Product Categories

A category can have a parent category

Example Table

Categories(category_id, category_name, parent_category_id)

Explanation

“Electronics” can have subcategories like “Mobiles” and “Laptops”.

 Used for category hierarchies

3. Importance of Database Relationships in E-commerce

Ensures data consistency

Prevents duplicate data

Makes querying efficient

Supports scalability

Helps maintain business rules

4. Summary Table
Relationship Type	E-commerce Example
One-to-One	User → Profile
One-to-Many	Customer → Orders
Many-to-One	Orders → Customer
Many-to-Many	Orders ↔ Products
Self-Referencing	Categories → Subcategories
