# 👋 Welcome to ChatterBox!

ChatterBox is a full-stack, real-time chat application I built using FastAPI and WebSockets. I wanted to create a platform that handles secure authentication, instant messaging, and automated moderation smoothly. 

This project was a great way to put modern backend architecture, JWT-based auth, and real-time communication into practice.

## ✨ What It Can Do

- 🔐 Secure user registration and login
- 🎫 JWT-based authentication to keep sessions safe
- 👤 Role-based access (so Admins have special powers)
- 💬 Instant real-time chatting via WebSockets
- 🛡️ Automated bad word detection
- ⚠️ An auto-warning and blocking system for rule-breakers
- 📊 A dedicated Admin Dashboard
- 📥 Downloadable CSV reports for monitoring
- 🗄️ Lightweight SQLite database integration

## 🛠️ Built With

**Backend:** FastAPI, SQLAlchemy, SQLite, Python-Jose (JWT), Passlib (bcrypt), WebSockets
**Frontend:** HTML5, CSS3, JavaScript, Fetch API

## 📂 Project Structure

```text
CHATTERBOX/
├── backend/
│   ├── app/
│   │   ├── admin/
│   │   ├── auth/
│   │   ├── chat/
│   │   ├── ml/
│   │   ├── utils/
│   │   ├── database.py
│   │   ├── main.py
│   │   ├── models.py
│   │   └── schemas.py
│   ├── requirements.txt
│   └── run.py
├── frontend/
│   ├── admin/
│   ├── assets/
│   ├── css/
│   ├── js/
│   ├── chat.html
│   ├── index.html
│   └── register.html
├── LICENSE
├── PROJECT_DOCUMENTATION.md
└── README.md
