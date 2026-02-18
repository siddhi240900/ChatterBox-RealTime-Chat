🚀 ChatterBox – Real-Time WebSocket Chat Application

📌 Overview

ChatterBox is a full-stack real-time chat application built using FastAPI and WebSockets.
It supports secure authentication, instant messaging, automated moderation, and an admin monitoring dashboard.

This project demonstrates modern backend architecture, JWT-based authentication, and real-time communication handling.

✨ Features

🔐 User Registration & Login
🎫 JWT-based Authentication
👤 Role-based Access (Admin & User)
💬 Real-Time Chat using WebSockets
🛡️ Automated Bad Word Detection
⚠️ Warning & Auto-Block System
📊 Admin Dashboard
📥 CSV Report Download
🗄️ SQLite Database Integration
🛠️ Tech Stack

🔹 Backend

FastAPI
SQLAlchemy
SQLite
Python-Jose (JWT)
Passlib (bcrypt)
WebSockets

🔹 Frontend

HTML5
CSS3
JavaScript
Fetch API

📂 Project Structure
ChatterBox/
│
├── backend/
├── frontend/
├── README.md
├── PROJECT_DOCUMENTATION.md
└── LICENSE

⚙️ Installation Guide
🔹 1. Clone the Repository
git clone https://github.com/siddhi240900/ChatterBox-RealTime-Chat.git
cd ChatterBox-RealTime-Chat

🔹 2. Backend Setup
cd backend
python -m venv venv
pip install -r requirements.txt
python run.py


Backend will run at:

http://127.0.0.1:8000

🔹 3. Frontend Setup
cd frontend
npm install
npm run dev

🔐 Admin Features

Admin users can:

View all registered users
Monitor chat messages
View blocked users
Download reports in CSV format

🛡️ Security Implementation

Password hashing using bcrypt
JWT token authentication
Role-based route protection
Auto-block moderation system

📈 Future Improvements

Group chat functionality
Private messaging
PostgreSQL integration
Docker containerization
Cloud deployment
AI-powered moderation

📜 License

This project is licensed under the MIT License.