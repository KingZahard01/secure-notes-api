# Secure Notes API

Secure REST API for user-based note management with token authentication and per-user data isolation.

---

## 🚀 Features
- User registration and authentication
- Token-based authentication
- Full CRUD operations for notes
- Per-user data isolation (users can only access their own notes)
- JSON-based REST API

---

## 🛠 Tech Stack
- Backend: Django
- API Framework: Django REST Framework
- Authentication: Token-based auth
- Database: SQLite (PostgreSQL-ready)
- Deployment: Render

---

## 🧠 Architecture Overview
The API is built using Django REST Framework and follows a clear separation of concerns between models, serializers, views, and permissions.

Authentication is handled via token-based authentication, ensuring that all note operations are securely scoped to the authenticated user.

---

## 🌍 Live API
Base URL: https://notes-backend-knfs.onrender.com

---

## 📌 Core Endpoints

| Method | Endpoint            | Description              |
|------|---------------------|--------------------------|
| POST | `/api/register/`     | Register new user        |
| POST | `/api/login/`        | Obtain auth token        |
| GET  | `/api/notes/`        | List user notes          |
| POST | `/api/notes/`        | Create new note          |
| GET  | `/api/notes/{id}/`   | Retrieve note            |
| PUT  | `/api/notes/{id}/`   | Update note              |
| DELETE | `/api/notes/{id}/` | Delete note              |

> All note endpoints require authentication.

---

## 🧪 Local Development

```bash
# Clone repository
git clone https://github.com/your-username/secure-notes-api.git
cd secure-notes-api

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Apply migrations
python manage.py migrate

# Run server
python manage.py runserver
