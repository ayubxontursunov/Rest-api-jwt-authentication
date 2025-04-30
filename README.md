# 🛡️ REST API with JWT Authentication

A secure Django REST Framework project providing full-featured user authentication and note management using JSON Web Tokens (JWT).

## 🚀 Features

- ✅ User Registration with Image Upload
- 🔐 JWT Authentication (Login / Token Refresh)
- 📝 Create, Update, Delete, and List Notes
- 👤 User Profile with Custom Fields
- 📸 Image Validation and Upload
- 🔒 Public/Private Notes Handling
- 🧪 API tested via Postman

## 📦 Tech Stack

- **Backend:** Django, Django REST Framework
- **Authentication:** JWT via `SimpleJWT`
- **Database:** SQLite (default, can be switched)
- **Media Handling:** File/Image uploads
- **Validation:** Django Validators

## 📁 API Endpoints

| Method | Endpoint                     | Description                      |
|--------|------------------------------|----------------------------------|
| POST   | `/api/register/`             | Register a new user              |
| POST   | `/api/token/`                | Obtain JWT tokens (login)        |
| POST   | `/api/token/refresh/`        | Refresh access token             |
| GET    | `/api/notes/`                | List user's & public notes       |
| GET    | `/api/note/<int:pk>/`        | Get specific note details        |
| POST   | `/api/notes/create/`         | Create a new note                |
| PATCH  | `/api/note/<int:pk>/update/` | Update a note                    |
| DELETE | `/api/note/<int:pk>/delete/` | Delete a note                    |
| GET    | `/api/profile/`              | Get authenticated user's profile |
| PATCH  | `/api/profile/update/`       | Update user profile              |
| GET    | `/api/users/<int:pk>/notes`  | Get notes of a specific user     |

## 🧪 Sample Registration (Postman Raw JSON)

```json
{
  "username": "testuser",
  "email": "test@example.com",
  "password": "YourStrongPassword123",
  "password2": "YourStrongPassword123",
  "bio": "I love notes!",
  "cover_photo": null
}
```

## 🛠️ Setup Instructions

```commandline
git clone https://github.com/yourusername/Rest-api-jwt-authentication
cd Rest-api-jwt-authentication
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

## 📂 Project Structure

```commandline
api/
├── models.py
├── views.py
├── serializer.py
├── urls.py
```
## 🧾 License
MIT License — feel free to use and contribute!

Made with ❤️ using Django & DRF