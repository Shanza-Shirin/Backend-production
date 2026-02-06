Auth Backend API

A simple authentication backend built with Node.js, Express, MongoDB, and JWT.
It supports user registration, login, and JWT-based authentication.

-Features

User registration

User login

Password hashing (bcrypt)

JWT authentication

Protected routes middleware

-Tech Stack

Node.js

Express.js

MongoDB & Mongoose

JWT

bcryptjs

- Project Structure

backend/
 ├─ src/
 │   ├─ app.js
 │   ├─ config/
 │   │   └─ db.js
 │   ├─ controllers/
 │   │   └─ auth.controller.js
 │   ├─ middleware/
 │   │   └─ auth.middleware.js
 │   ├─ models/
 │   │   └─ user.model.js
 │   ├─ routes/
 │   │   └─ auth.routes.js
 ├─ .env
 ├─ server.js
 └─ README.md

-Environment Setup

Create a .env file in the root directory:

PORT=5000
MONGO_URL=mongodb://127.0.0.1:27017/authdb
JWT_SECRET=your_secret_key

- Installation & Run
npm install
npm run dev

- API Endpoints
Register User

POST /api/auth/register

{
  "name": "John Doe",
  "email": "john@gmail.com",
  "password": "123456"
}

Login User

POST /api/auth/login

{
  "email": "john@gmail.com",
  "password": "123456"
}


Response

{
  "message": "Login successful",
  "token": "JWT_TOKEN"
}




