
# 🌐 VibeIT - FastAPI Social Media Backend

A backend clone of a social media application, built using **FastAPI**. This API handles user registration, authentication, post creation, voting (likes), and more — with secure JWT-based login and PostgreSQL as the database.

---

## 📦 Project Structure

```
VibeIT/
├── alembic/               # DB migration folder
├── app/                   # Core application (routers, models, etc.)
├── tests/                 # Unit tests
├── requirements.txt       # Dependencies
├── alembic.ini            # Alembic config
└── main.py                # Main FastAPI app entry point
```

---

## 🛣 API Routes Overview

### 1️⃣ **/posts**
- Create a new post
- Delete an existing post
- Update post content
- Retrieve posts

### 2️⃣ **/users**
- Register a new user
- Get user by ID

### 3️⃣ **/auth**
- Login with username/email and password
- Returns JWT token for secure access

### 4️⃣ **/vote**
- Like or unlike a post (Upvote/Remove vote)
- No downvote logic included

---

## 🧪 Running Locally

### ✅ Clone the Repository

```bash
git clone https://github.com/Zeroo-01/VibeIT.git
cd VibeIT
```

### ✅ Install FastAPI with all extras

```bash
pip install fastapi[all]
```

### ✅ Start the Server

```bash
uvicorn main:app --reload
```

Visit the docs at:  
🔗 [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## 🗃 Database Setup (PostgreSQL)

Create a PostgreSQL database, then in the root folder, create a `.env` file with the following:

```env
DATABASE_HOSTNAME=localhost
DATABASE_PORT=5432
DATABASE_PASSWORD=your_password
DATABASE_NAME=your_database_name
DATABASE_USERNAME=your_username
SECRET_KEY=your_custom_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=60
```

⚠️ **Note**: Replace values as needed. The `SECRET_KEY` should be a securely generated string (you can use FastAPI docs or any online secret generator).

---

## 🚀 Tech Stack

- FastAPI
- PostgreSQL
- SQLAlchemy
- Alembic
- JWT Authentication
- Pydantic

---

## ✅ Todo / Improvements

- Add support for downvotes
- Add pagination for posts
- Rate limiting (for API abuse protection)
- Profile picture support

---

## 👤 Author

**Zeroo-01**  
GitHub: [https://github.com/Zeroo-01](https://github.com/Zeroo-01)

---

