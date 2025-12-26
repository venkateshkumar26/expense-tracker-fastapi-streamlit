# Expense Tracker – FastAPI & Streamlit

A simple and efficient **Expense Tracking Application** built using **FastAPI**, **SQLAlchemy**, **SQLite**, and **Streamlit**.  
This project allows users to add, delete, and view expenses by date or date range through a clean web interface.

---

## 🚀 Features

- Add daily expenses with category and amount
- Automatically manages expense categories
- Delete expenses by date and category
- View expenses for:
  - A single date
  - A selected date range
- RESTful API built using FastAPI
- Interactive UI built using Streamlit
- Persistent storage using SQLite

---

## 🛠️ Tech Stack

**Backend**
- FastAPI
- SQLAlchemy ORM
- SQLite database
- Pydantic (data validation)

**Frontend**
- Streamlit
- Pandas
- Requests

---

## 📂 Project Structure

expense-tracker-fastapi-streamlit/
│
├── backend.py # FastAPI application & API routes
├── add_data.py # Business logic (CRUD operations)
├── connect_data.py # Database models & DB connection
├── ui.py # Streamlit frontend
├── expenses.db # SQLite database (auto-created)
├── requirements.txt
└── README.md

yaml
Copy code

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/expense-tracker-fastapi-streamlit.git
cd expense-tracker-fastapi-streamlit
2️⃣ Install Dependencies
pip install -r requirements.txt

▶️ Running the Application
Step 1: Start the FastAPI Backend
uvicorn backend:app --reload
Backend will run at:
http://127.0.0.1:8000
Swagger API Docs:
http://127.0.0.1:8000/docs

Step 2: Start the Streamlit UI
Open a new terminal and run:
streamlit run ui.py
Streamlit UI will open in your browser:
http://localhost:8501

🔌 API Endpoints
Method	Endpoint	Description
POST	/expense/enter_expense	Add a new expense
DELETE	/expense/delete	Delete expense by date & category
POST	/expense/show_expenses	Show expenses for a single date
POST	/expense/from_to_expense	Show expenses in a date range

🧠 Database Design
ExpenseCategory Table
exp_id (Primary Key)

exp_name (Unique category name)

Expense Table
id (Primary Key)

date

exp_id (Foreign Key)

amount

Relationship:
One category → Many expenses

📈 Future Enhancements
Monthly and yearly expense summaries

Category-wise analytics and charts

Authentication (login system)

Export expenses to CSV / Excel

Dockerization

Deployment on cloud (AWS / Render)
