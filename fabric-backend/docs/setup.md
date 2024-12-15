# Setup Guide for Fabric Management Backend

Welcome to the **Fabric Management Backend**! This guide will walk you through the steps to set up and run the backend application locally. Whether you're new to the project or revisiting it, this document will serve as your reference for getting started.
[Return To Index 🗂️](welcome.md#-index)
---

## 🛠️ Prerequisites

Before starting, ensure you have the following installed on your machine:

1. **Python 3.10+**
2. **PostgreSQL** (configured and running)
3. **Virtual Environment** (optional but recommended)

---

## 📥 Step 1: Clone the Repository

Clone the repository to your local machine using Git:

```
bash
git clone https://github.com/yourusername/fabric-management.git
cd fabric-backend
```

---

## 🏗️ Step 2: Set Up a Virtual Environment

Set up a virtual environment to isolate dependencies for this project:

```
bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows Users:**

```
bash
.venv\Scripts\activate
```

---

## 📦 Step 3: Install Dependencies

Install the required Python packages listed in `requirements.txt`:

```
bash
pip install -r requirements.txt
```

---

## 🗄️ Step 4: Configure the Environment Variables

Create a `.env` file in the project's root directory and add the following environment variables:

```
plaintext
DATABASE_URL=postgresql://<username>:<password>@localhost:5432/fabric_db
SECRET_KEY=your-secret-key
DEBUG=True
```

- Replace `<username>` and `<password>` with your PostgreSQL credentials.
- Use a secure value for `SECRET_KEY`.
- You can use `.env.example` as a reference if available.

---

## 🛢️ Step 5: Set Up the Database

### 1. Create the Database:

Log in to your PostgreSQL instance and create a new database:

```
sql
CREATE DATABASE fabric_db;
```

### 2. Apply Migrations:

Run Alembic to apply database migrations:

```
bash
alembic upgrade head
```

---

## 🚀 Step 6: Run the Application

Start the backend server using Uvicorn:

```
bash
uvicorn app.main:app --reload
```

The server will start running at:

- **Base URL:** `http://127.0.0.1:8000`
- **Swagger Docs:** `http://127.0.0.1:8000/docs`
- **ReDoc:** `http://127.0.0.1:8000/redoc`

---

## 🧪 Step 7: Run Tests (Optional)

To ensure everything is working correctly, run the tests:

```
bash
pytest
```

---

## 🌟 What's Next?

Once the backend is running, you can:

- Explore the [API documentation](api_docs.md) to understand available endpoints.
- Dive into the [architecture details](architecture.md) for a deeper understanding of the backend structure.

For any issues, feel free to create a GitHub issue or contact the maintainer.

---

Happy coding! 🎉

[Return To Index 🗂️](welcome.md#-index)