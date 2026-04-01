# 🚀 Project Camp Backend

A powerful and scalable **Project Management Backend API** built with the MERN stack ecosystem.
Designed to support **team collaboration, task management, and role-based access control** with production-ready architecture.

---

## 🧠 Overview

Project Camp Backend is a RESTful API that enables teams to:

* Manage projects efficiently
* Assign and track tasks & subtasks
* Collaborate with team members
* Maintain structured project notes
* Ensure secure authentication & authorization

---

## ✨ Features

### 🔐 Authentication & Authorization

* JWT-based authentication (Access + Refresh Tokens)
* Email verification system
* Forgot / Reset password flow
* Role-based access control (Admin, Project Admin, Member)

### 📁 Project Management

* Create, update, delete projects
* View project details with members
* Role-based project access

### 👥 Team Management

* Add/remove members via email
* Assign roles within projects
* Manage permissions dynamically

### ✅ Task Management

* Create tasks with descriptions & assignees
* Status tracking: `Todo`, `In Progress`, `Done`
* File attachments support
* Task updates & deletion

### 🔹 Subtasks

* Nested task structure
* Mark completion individually
* Controlled access based on roles

### 📝 Project Notes

* Create and manage notes
* Admin-controlled editing
* Organized project documentation

### 🩺 System Health

* Dedicated health check endpoint

---

## 🛠️ Tech Stack

* **Node.js**
* **Express.js**
* **MongoDB + Mongoose**
* **JWT Authentication**
* **Multer (File Uploads)**
* **Nodemailer (Emails)**

---

## 📂 API Structure

### 🔑 Auth Routes

```
POST   /api/v1/auth/register
POST   /api/v1/auth/login
POST   /api/v1/auth/logout
GET    /api/v1/auth/current-user
POST   /api/v1/auth/change-password
POST   /api/v1/auth/refresh-token
GET    /api/v1/auth/verify-email/:token
POST   /api/v1/auth/forgot-password
POST   /api/v1/auth/reset-password/:token
```

---

### 📁 Project Routes

```
GET    /api/v1/projects/
POST   /api/v1/projects/
GET    /api/v1/projects/:projectId
PUT    /api/v1/projects/:projectId
DELETE /api/v1/projects/:projectId
```

---

### ✅ Task Routes

```
GET    /api/v1/tasks/:projectId
POST   /api/v1/tasks/:projectId
PUT    /api/v1/tasks/:projectId/t/:taskId
DELETE /api/v1/tasks/:projectId/t/:taskId
```

---

### 📝 Notes Routes

```
GET    /api/v1/notes/:projectId
POST   /api/v1/notes/:projectId
PUT    /api/v1/notes/:projectId/n/:noteId
DELETE /api/v1/notes/:projectId/n/:noteId
```

---

### 🩺 Health Check

```
GET /api/v1/healthcheck/
```

---

## 🔐 Role-Based Access

| Feature        | Admin | Project Admin | Member |
| -------------- | ----- | ------------- | ------ |
| Create Project | ✅     | ❌             | ❌      |
| Manage Members | ✅     | ❌             | ❌      |
| Manage Tasks   | ✅     | ✅             | ❌      |
| View Tasks     | ✅     | ✅             | ✅      |
| Manage Notes   | ✅     | ❌             | ❌      |

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Yashhh25/PingMe.git
cd PingMe/backend
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Setup environment variables

Create `.env` file:

```
PORT=5000
MONGO_URI=your_mongodb_uri
ACCESS_TOKEN_SECRET=your_secret
REFRESH_TOKEN_SECRET=your_secret
EMAIL_USER=your_email
EMAIL_PASS=your_password
```

### 4️⃣ Run server

```bash
npm run dev
```

---

## 📦 File Uploads

* Supports multiple file attachments
* Stored in `public/images`
* Metadata tracked (URL, type, size)

---

## 🔒 Security Features

* JWT authentication with refresh tokens
* Role-based authorization middleware
* Input validation on all routes
* Secure file uploads
* CORS protection

---

## 🎯 Future Improvements

* WebSocket integration for real-time updates
* Notifications system
* Activity logs
* Deployment with Docker

---

## 👨‍💻 Author

**Yash**
Full Stack Developer 🚀

---

## ⭐ Show your support

If you like this project, give it a ⭐ on GitHub!
