# 💸 Simple Expense Tracker API

A lightweight and scalable expense tracking REST API built using **FastAPI**, **Pydantic**, **SQLAlchemy**, and **MySQL**.  
Perfect for learning full-stack Python API development with clean architecture.

## 📄 Project Description

**Simple Expense Tracker API** is a lightweight, backend-only application designed to help users manage their personal expenses effectively. Built with **FastAPI**, **Pydantic**, and **MySQL**, it provides a robust RESTful API with built-in data validation, clean code structure, and full CRUD capabilities.

Users can:
- Create profiles
- Add and categorize expenses
- Retrieve expense data for tracking and analysis

 ## WorkFlow 
   
  ![Image](https://github.com/user-attachments/assets/c90bf414-a0e2-4a89-8728-c5440aa94b04)

 
### 📌 Key Learnings:

- ✅ Input validation with Pydantic
- ✅ Used **Pydantic models (`BaseModel`)** to define request and response schemas.
- ✅ Implemented **strict input validation** (e.g., types like `str`, `int`, `float`).
- ✅ Applied **model inheritance** (e.g., `UserBase`, `UserCreate`, `User`) for clean and DRY schema design.
- ✅ SQLAlchemy ORM integration with MySQL
- ✅ Automatic API docs (Swagger + ReDoc)
- ✅ User registration


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

📌 Role of Pydantic
Pydantic plays a crucial role in the API by enforcing type hints and validating data before it reaches your SQLAlchemy models.

🔍 Example: Category Model:

 ![Image](https://github.com/user-attachments/assets/7703f766-fd78-45c9-a3c4-587e2169fe16)

📤 API Input Example
This is an example of the payload expected for a category creation:

![Image](https://github.com/user-attachments/assets/5d7266c6-31b7-4a59-99f5-ca3213308920)

🚫 Here incorrect input is passed  like this example (e.g., "id": "rr")  becuase ID is int & NAME is string. finally the input passed is wrong then , it will throw a error like:

![Image](https://github.com/user-attachments/assets/c38c3024-fb6d-43a7-9526-e48477329921)



# 🙌 Contributing
Pull requests are welcome!
For major changes, please open an issue first to discuss what you'd like to change.
 
