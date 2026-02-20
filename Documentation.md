# 🚀 ChatterBox – Full Project Documentation

**Author:** Satyajeet Kumar
**Project Type:** Full Stack Web Application  
**Technologies:** FastAPI, WebSockets, SQLite, JWT, HTML, CSS, JavaScript  

---

## 1. 🌟 Introduction

### What is ChatterBox?
ChatterBox is a full-stack, real-time chat application built using FastAPI and WebSockets. It is designed to handle secure user registration, instant messaging, automated chat moderation, and an admin monitoring dashboard. This project showcases modern backend architecture, secure JWT authentication, and real-time communication handling.

### Main Objectives
* Implement real-time communication via WebSockets.
* Set up secure, JWT-based authentication.
* Enforce role-based access control (Admin vs. User).
* Build an admin dashboard for system monitoring.
* Automate chat moderation to keep the environment safe.
* Manage data efficiently using SQLite.

---

## 2. 🏗️ System Architecture



The app runs on a client-server architecture. The frontend (HTML, CSS, JS) communicates with the FastAPI backend using:
* **REST APIs:** For authentication and administrative tasks.
* **WebSockets:** For persistent, real-time messaging.

Everything is backed by an SQLite database to store user credentials and chat history securely.

---

## 3. 🛠️ Technology Stack

**Backend:**
* FastAPI
* SQLAlchemy & SQLite
* Python-Jose
* Passlib
* WebSockets

**Frontend:**
* HTML5 & CSS3
* JavaScript & Fetch API

---

## 4. 🧩 Functional Modules

### Authentication
Handles user registration and secure login.
* **Security Measures:** Passwords are hashed with bcrypt, JWT tokens expire automatically, and API routes are protected based on specific user roles.

### Real-Time Chat
Powered by WebSockets for instant message broadcasting.
* **Workflow:** Log in -> Establish WebSocket connection -> Send message -> Server validates & stores -> Broadcast to connected users.

### Moderation System
Keeps the chat safe from inappropriate content automatically.
* **Rules:** 1st & 2nd violation = Warning. 3rd violation = Auto-block.
* Blocked users are completely restricted from logging in, sending messages, or accessing the chat system.

### Admin Dashboard
Admins have special privileges to view all users, monitor active chat messages, check blocked accounts, and download activity reports as CSV files.

---

## 5. 🗄️ Database Design



* **Users Table:** `id` (PK), `username`, `email`, `password_hash`, `is_admin`, `is_blocked`, `warning_count`, `created_at`
* **Messages Table:** `id` (PK), `sender_id`, `content`, `timestamp`

---

## 6. 🔌 API Endpoints

* **Auth:** `POST /register`, `POST /login`
* **Chat:** `WebSocket /ws`
* **Admin:** `GET /admin/users`, `GET /admin/messages`, `GET /admin/download/users`, `GET /admin/download/messages`

---

## 7. 🛡️ Security Implementation
* Bcrypt password hashing
* Strict JWT-based authentication
* Role-based API route protection
* Automated user-blocking system

---

## 8. 🧪 Testing
The platform underwent manual testing for core user flows (registration, login), role access, real-time messaging stability, warning/blocking logic, and admin CSV exports. All modules behave as expected.

---

## 9. 🚧 Limitations & Future Enhancements

**Current Limitations:**
* SQLite is not suited for high-scale production.
* Currently runs locally.
* Lacks group chats and extensive UI polish.

**What's Next?**
* Add dedicated group chat rooms and private messaging.
* Migrate to PostgreSQL for scalability.
* Dockerize the application and deploy to the cloud.
* Implement AI-based content moderation and file sharing.

---

## 10. 🎉 Conclusion
ChatterBox successfully demonstrates how to wire up real-time WebSocket communication, secure it with JWTs, and manage users with role-based access and automated moderation. It is a solid showcase of modern backend architecture and real-time system design.
