# Mentor-Mentee Management System

A web-based application designed to simplify mentor-mentee interactions, task management, performance tracking, feedback, and communication.

## Technologies Used
- Python
- FastAPI
- SQLite
- SQLAlchemy
- HTML, CSS, JavaScript

## Setup & Run

### Prerequisites
- Python 3.12 or compatible version

### Installation

```bash
pip install -r requirements.txt
```

### Start the application

```bash
uvicorn main:app --reload
```

Open your browser and visit: http://127.0.0.1:8000

## Features

### Admin
- Dashboard with statistics
- View mentors and mentees
- Assign mentor-mentee pairs
- Add tasks for mentees
- Manage feedback questions and release feedback forms
- Messenger to communicate with users

### Mentor
- Dashboard with mentee performance overview
- View assigned mentees
- Assign tasks with deadlines
- Messenger to chat with assigned mentees

### Mentee
- Dashboard with task progress and performance percentage
- View and complete assigned tasks
- Submit feedback when released
- Messenger to communicate with mentors

## Messenger API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/messages/send` | Send a message |
| GET | `/messages/conversation/{user1_id}/{user2_id}` | Retrieve chat history |
| GET | `/messages/contacts/{user_id}` | Retrieve contacts with unread count |
| GET | `/messages/unread/{user_id}` | Get total unread messages |

## User Roles
- **Admin:** Full system access and management.
- **Mentor:** Manage assigned mentees and their tasks.
- **Mentee:** View tasks, track progress, and submit feedback.
