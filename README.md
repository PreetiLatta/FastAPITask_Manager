# FastAPITask_Manager
A FastAPI-based task manager with authentication and database integration

#Features
- User authentication (JWT-based)
- Task management (Create, Update, Delete, View)
- Secure API endpoints
- Database integration with SQLite

#structure
 fastapi-taskmanager
 database
 models.py
 database.py
 routes
 routes.py
 main.py
 auth.py
 schemas.py
 README.md
 requirements.txt

 ##  Installation Guide

1 Clone the Repository
```bash
git clone https://github.com/<your-username>/fastapi-taskmanager.git
cd fastapi-taskmanager
2 Create a Virtual Environment (Recommended)
bash
Copy
Edit
python -m venv venv
Activate the environment:

Windows:
bash
Copy
Edit
venv\Scripts\activate
Mac/Linux:
bash
Copy
Edit
source venv/bin/activate
3 Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4️ Set Up the Database
bash
Copy
Edit
alembic upgrade head
5️ Run the Application
bash
Copy
Edit
uvicorn main:app --reload
The API will be available at:
-- http://127.0.0.1:8000

6️ Access API Documentation
FastAPI provides an interactive API doc:

Swagger UI: http://127.0.0.1:8000/docs
Redoc UI: http://127.0.0.1:8000/redoc
---- API Endpoints
Method	Endpoint	Description
POST	/register	Register a new user
POST	/login	Authenticate user & get JWT token
GET	/tasks	Get all tasks (Authenticated users only)
POST	/tasks	Create a new task
PUT	/tasks/{id}	Update a task
DELETE	/tasks/{id}	Delete a task
