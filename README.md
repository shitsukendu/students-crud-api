Students Database CRUD API

A RESTful API built with Python, FastAPI, SQLAlchemy, and SQLite to manage student records. This project demonstrates backend development fundamentals, database integration, request validation, and CRUD operations.

Features

- Create new student records
- Retrieve all students
- Retrieve a student by ID
- Update student information
- Delete student records
- Validate request data using Pydantic
- Validate email addresses
- Prevent duplicate email addresses
- Handle errors such as student not found and duplicate email
- Automatically generate interactive API documentation

Technologies Used

- Python
- FastAPI
- SQLAlchemy
- SQLite
- Pydantic
- Uvicorn
- uv

Student Fields

Each student record contains:

- "id" — Unique student ID
- "name" — Student name
- "date_of_birth" — Date of birth
- "email" — Student email address
- "phone" — Phone number

API Endpoints

Method| Endpoint| Description
GET| "/"| Check API status
POST| "/students"| Create a student
GET| "/students"| Get all students
GET| "/students/{student_id}"| Get a student by ID
PATCH| "/students/{student_id}"| Update student details
DELETE| "/students/{student_id}"| Delete a student

Installation and Setup

1. Clone the repository

git clone https://github.com/shitsukendu/students-crud-api.git
cd students-crud-api

2. Install dependencies

Install Python dependencies using uv:

uv sync

3. Run the application

uv run uvicorn main:app --reload

4. Open the API documentation

Visit:

- Swagger UI: http://127.0.0.1:8000/docs
- ReDoc: http://127.0.0.1:8000/redoc

Validation and Error Handling

The API validates student input and returns appropriate HTTP status codes.

- "201 Created" — Student created successfully
- "200 OK" — Request completed successfully
- "404 Not Found" — Student record does not exist
- "409 Conflict" — Email address already exists
- "422 Unprocessable Content" — Invalid request data

Database

The application uses SQLite and SQLAlchemy ORM. The database file is created automatically when the application starts.

Learning Outcomes

This project helped me practice REST API development, database operations, ORM integration, input validation, error handling, and API testing with Swagger UI.

Author

SUKENDU SHIT

GitHub: https://github.com/shitsukendu