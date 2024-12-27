# 🛒 BlinkIt Online App Database

## ✨ Overview
This project implements an online application database inspired by BlinkIt, providing functionalities for users to browse, purchase, and manage products effectively. The database integrates advanced features such as schema diagrams, URL structures, constraints checking, transactions, and deadlock resolution.

## ⚖️ Features
- **🛒 User functionalities**:
  1. 🔎 Search and browse products by category or name.
  2. 🛍️ Add products to the cart and place orders.
  3. 📜 View order history and track orders.
  4. 🛡️ Manage user profiles and payment methods.
- **⚙️ Admin functionalities**:
  1. ➕ Add and update product details.
  2. ❌ Remove outdated or unavailable products.
  3. 🔍 View user activities and sales analytics.
  4. 🔧 Resolve database deadlocks and maintain transactions.
- **🔧 Database functionalities**:
  1. 📊 Schema definition with relationships and constraints.
  2. 🔒 ACID-compliant transaction management.
  3. ✅ Constraints checking for data integrity.
  4. 🚦 Deadlock detection and resolution mechanisms.

## 📐 Schema Diagram
The database schema includes the following tables and relationships:
1. **Users**: Stores user details such as user ID, name, email, and address.
2. **Products**: Stores product details including product ID, name, category, price, and stock.
3. **Orders**: Tracks orders with fields for order ID, user ID, product ID, quantity, and order status.
4. **Transactions**: Manages payment details with fields for transaction ID, order ID, and payment status.

Relationships:
- A **user** can place multiple **orders**.
- An **order** can include multiple **products**.
- Each **order** has an associated **transaction**.


## 🔧 Prerequisites
- 🛠️ MySQL or PostgreSQL installed.
- 🔧 Python 3.8+ installed.
- 🐍 Required Python libraries: Flask, SQLAlchemy, etc.

## ⚡ Setup and Execution
### Step 1: 🔧 Clone the Repository
1. Download or clone the repository containing the project files.

### Step 2: ⛱ Navigate to the Project Directory
Ensure that the project directory contains the `schema.sql` file.

### Step 3: 📊 Initialize the Database
Run the following commands to set up the database schema:
```sql
source schema.sql;
source constraints.sql;
```

### Step 4: ▶️ Run the Application
Start the application server:
```bash
python app/main.py
```

## 🔍 Functionalities in Detail
### 🌐 URL Structures
- `/products`: Displays all available products.
- `/cart`: Manages the user’s cart.
- `/checkout`: Processes orders and initiates transactions.
- `/admin`: Provides admin functionalities for managing the database.

### ✅ Constraints Checking
- Ensures no duplicate products.
- Validates stock availability during checkout.
- Enforces unique email addresses for user registration.

### 🔄 Transactions
- Implements ACID properties for order placement.
- Ensures atomicity with rollback support for failed transactions.
- Logs all transactions for audit purposes.

### 🚦 Deadlock Resolution
- Detects circular wait conditions.
- Automatically resolves deadlocks using the wait-die or wound-wait algorithms.

## 📢 Contact
For any issues or queries related to the project, please contact **Vipul** at [Vipul22576@iiitd.ac.in](mailto:Vipul22576@iiitd.ac.in).

🌟 Enjoy building robust databases!

