CHARTTERBOX – REAL-TIME WEBSOCKET CHAT APPLICATION  
FULL PROJECT DOCUMENTATION  

Author: Siddhi Kumari  
Project Type: Full Stack Web Application  
Technologies Used: FastAPI, WebSockets, SQLite, JWT, HTML, CSS, JavaScript  

------------------------------------------------------------

1. INTRODUCTION  

1.1 Project Overview  

ChatterBox is a full-stack real-time chat application developed using FastAPI and WebSockets.  
The system enables secure user registration and login, real-time messaging, automated moderation, and an admin monitoring dashboard.  

The platform demonstrates modern backend architecture, secure authentication using JWT, and real-time communication handling.

1.2 Objectives  

The main objectives of this project are:  

• To implement real-time communication using WebSockets  
• To design secure JWT-based authentication  
• To implement role-based access control  
• To create an admin monitoring system  
• To build automated moderation for chat messages  
• To manage data efficiently using SQLite  

------------------------------------------------------------

2. SYSTEM ARCHITECTURE  

The application follows a client-server architecture.

Frontend (HTML, CSS, JavaScript) communicates with the FastAPI backend using:

• REST APIs (for authentication and admin operations)  
• WebSockets (for real-time messaging)  

The backend interacts with an SQLite database to store users and messages.

------------------------------------------------------------

3. TECHNOLOGY STACK  

3.1 Backend  

• FastAPI  
• SQLAlchemy  
• SQLite  
• Python-Jose (JWT handling)  
• Passlib (Password hashing using bcrypt)  
• WebSockets  

3.2 Frontend  

• HTML5  
• CSS3  
• JavaScript  
• Fetch API  

------------------------------------------------------------

4. FUNCTIONAL MODULES  

4.1 Authentication Module  

Features:  

• User Registration  
• User Login  
• JWT Token Generation  
• Role-based Authorization  
• Blocked User Detection  

Security Measures:  

• Passwords hashed using bcrypt  
• JWT tokens with expiration time  
• Protected API routes  
• Admin-only endpoints  

------------------------------------------------------------

4.2 Real-Time Chat Module  

Features:  

• WebSocket-based messaging  
• Instant message broadcasting  
• Persistent message storage  
• Timestamp tracking  

Workflow:  

1. User logs in  
2. WebSocket connection is established  
3. Message is sent to the server  
4. Message is validated and stored  
5. Message is broadcast to connected users  

------------------------------------------------------------

4.3 Moderation System  

Purpose:  

To maintain safe and controlled communication.

Implementation:  

• Messages are checked for inappropriate words  
• Warning system is implemented  

Violation Handling:  

• 1st violation → Warning  
• 2nd violation → Warning  
• 3rd violation → User automatically blocked  

Blocked users cannot:  

• Log in  
• Send messages  
• Access the chat system  

------------------------------------------------------------

4.4 Admin Module  

Admin Capabilities:  

• View all registered users  
• View blocked users  
• Monitor chat messages  
• Download reports in CSV format  

Admin routes are protected using role-based JWT verification.

------------------------------------------------------------

5. DATABASE DESIGN  

5.1 Users Table  

Fields:  

• id (Primary Key)  
• username  
• email  
• password_hash  
• is_admin  
• is_blocked  
• warning_count  
• created_at  

5.2 Messages Table  

Fields:  

• id (Primary Key)  
• sender_id  
• content  
• timestamp  

------------------------------------------------------------

6. API ENDPOINTS  

6.1 Authentication  

• POST /register  
• POST /login  

6.2 Chat  

• WebSocket /ws  

6.3 Admin  

• GET /admin/users  
• GET /admin/messages  
• GET /admin/download/users  
• GET /admin/download/messages  

------------------------------------------------------------

7. SECURITY IMPLEMENTATION  

• Password hashing using bcrypt  
• JWT-based authentication  
• Role-based route protection  
• Auto-block moderation system  

------------------------------------------------------------

8. TESTING  

The system was manually tested for:

• User registration  
• Login validation  
• Role-based access control  
• Real-time chat functionality  
• Warning logic  
• Auto-block functionality  
• Admin report download  

All modules were verified for expected behavior.

------------------------------------------------------------

9. LIMITATIONS  

• SQLite is not suitable for high-scale production  
• No cloud deployment implemented  
• No group chat feature  
• Limited UI enhancements  

------------------------------------------------------------

10. FUTURE ENHANCEMENTS  

• Group chat rooms  
• Private messaging  
• PostgreSQL integration  
• Docker containerization  
• Cloud deployment  
• AI-based content moderation  
• File and image sharing  

------------------------------------------------------------

11. CONCLUSION  

ChatterBox successfully demonstrates:

• Real-time WebSocket communication  
• Secure JWT authentication  
• Role-based access control  
• Automated moderation system  
• Admin monitoring dashboard  

The project reflects a strong understanding of backend architecture, authentication mechanisms, and real-time system development.
