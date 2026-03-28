# TodoApp-FastAPI

## Project Information

**TodoApp-FastAPI** is a simple yet powerful API built with FastAPI to manage daily tasks efficiently. This project allows users to create, read, update, and delete their tasks.

---

## Features
- User authentication
- Task management (CRUD operations)
- Fast and efficient performance
- Built using FastAPI and SQLAlchemy

---

## Setup Instructions

### Prerequisites
- Python 3.7 or later
- pip (Python package installer)
- A virtual environment (recommended)

### Installation Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/vidyajain20/TodoApp-FastAPI.git
   cd TodoApp-FastAPI
   ```

2. **Create and activate a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the requirements**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**:
   ```bash
   uvicorn main:app --reload
   ```

5. **Access the API documentation**:
   Navigate to `http://127.0.0.1:8000/docs` in your browser to view the interactive API documentation.

---

## API Endpoints

### Authentication
- **POST /auth/login**: Authenticate user and get access token.
  - Request Body: `{ "username": "<your_username>", "password": "<your_password>" }`
  - Response: Token string.

### Task Management
- **GET /tasks/**: Retrieve all tasks.
- **POST /tasks/**: Create a new task.
  - Request Body: `{ "title": "<task_title>", "description": "<task_description>", "completed": false }`
- **GET /tasks/{task_id}**: Retrieve a specific task by ID.
- **PUT /tasks/{task_id}**: Update a task by ID.
  - Request Body: `{ "title": "<task_title>", "description": "<task_description>", "completed": true }`
- **DELETE /tasks/{task_id}**: Delete a task by ID.

---

## Architecture Overview
The TodoApp is structured using the Model-View-Controller (MVC) architecture:
- **Models**: Define data structures and handle data manipulation (SQLAlchemy models).
- **Views**: Handle API responses and request routing (FastAPI routes).
- **Controllers**: Manage application logic and data flow between models and views.

The application uses SQLite as the database for simplicity and ease of setup.