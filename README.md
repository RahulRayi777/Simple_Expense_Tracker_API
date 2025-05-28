# 💸 Simple Expense Tracker API

A lightweight and scalable expense tracking REST API built using **FastAPI**, **Pydantic**, **SQLAlchemy**, and **MySQL**.  
Perfect for learning full-stack Python API development with clean architecture.

## 📄 Project Description

**Simple Expense Tracker API** is a lightweight, backend-only application designed to help users manage their personal expenses effectively. Built with **FastAPI**, **Pydantic**, and **MySQL**, it provides a robust RESTful API with built-in data validation, clean code structure, and full CRUD capabilities.

Users can:
- Create profiles
- Add and categorize expenses
- Retrieve expense data for tracking and analysis

By leveraging FastAPI’s automatic documentation, developers and consumers of the API can easily test and understand endpoints via Swagger UI or ReDoc.


## 🛠️ Setup Instructions

### 1. 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

2. 🛢️ Configure MySQL
Create a database in MySQL (e.g., expense_db) and update the DATABASE_URL in database.py:

```bash
DATABASE_URL = "mysql+pymysql://username:password@localhost/expense_db"
```

3. 🏁 Run the API
```bash
uvicorn main:app --reload
```

Open in browser:

Swagger UI → http://127.0.0.1:8000/docs

ReDoc → http://127.0.0.1:8000/redoc


| Method | Endpoint       | Description       |
| ------ | -------------- | ----------------- |
| POST   | `/users/`      | Create a new user |
| POST   | `/categories/` | Create a category |
| POST   | `/expenses/`   | Add a new expense |
| GET    | `/expenses/`   | List all expenses |

📌 Example JSON Payloads

➕ Create User
json
 
```bash
{
  "name": "Alice"
}
```

➕ Create Category
```bash
{
  "name": "Food"
}
```

➕ Create Expense
```bash
{
  "amount": 250.75,
  "description": "Dinner at a restaurant",
  "user_id": 1,
  "category_id": 1
}
```

# 🧪 Testing
You can test endpoints using:

🔹 Swagger UI (http://localhost:8000/docs)

🔹 Postman

🔹 cURL

# 🙌 Contributing
Pull requests are welcome!
For major changes, please open an issue first to discuss what you'd like to change.

 


## 🛠️ Setup Instructions

### 1. 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

2. 🛢️ Configure MySQL
Create a database in MySQL (e.g., expense_db) and update the DATABASE_URL in database.py:

```bash
DATABASE_URL = "mysql+pymysql://username:password@localhost/expense_db"
```

3. 🏁 Run the API
```bash
uvicorn main:app --reload
```

Open in browser:

Swagger UI → http://127.0.0.1:8000/docs

ReDoc → http://127.0.0.1:8000/redoc


| Method | Endpoint       | Description       |
| ------ | -------------- | ----------------- |
| POST   | `/users/`      | Create a new user |
| POST   | `/categories/` | Create a category |
| POST   | `/expenses/`   | Add a new expense |
| GET    | `/expenses/`   | List all expenses |

📌 Example JSON Payloads

➕ Create User
json
 
```bash
{
  "name": "Alice"
}
```

➕ Create Category
```bash
{
  "name": "Food"
}
```

➕ Create Expense
```bash
{
  "amount": 250.75,
  "description": "Dinner at a restaurant",
  "user_id": 1,
  "category_id": 1
}
```

# 🧪 Testing
You can test endpoints using:

🔹 Swagger UI (http://localhost:8000/docs)

🔹 Postman

🔹 cURL

# 🙌 Contributing
Pull requests are welcome!
For major changes, please open an issue first to discuss what you'd like to change.

 
