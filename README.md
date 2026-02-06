🔐 Auth Backend API
Node.js · Express · MongoDB · JWT

A secure and scalable authentication backend built with Node.js, Express, MongoDB, and JWT.
This project handles user registration, login, password encryption, and JWT-based authorization — ready to plug into any frontend (React, Next.js, mobile apps, etc.).

✨ Features

✅ User Registration
✅ User Login
🔐 Password Hashing (bcrypt)
🪪 JWT Authentication
🛡 Protected Routes Middleware
⚙️ Environment Variable Support
📁 Clean & Scalable Folder Structure

🧰 Tech Stack
Technology	Purpose
Node.js	Runtime
Express.js	Backend framework
MongoDB	Database
Mongoose	ODM
JWT	Authentication
bcryptjs	Password hashing
dotenv	Environment variables
📂 Project Structure
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
 ├─ package.json
 └─ README.md

⚙️ Environment Setup

Create a .env file in the root directory:

PORT=5000
MONGO_URL=mongodb://127.0.0.1:27017/authdb
JWT_SECRET=your_super_secret_key

📦 Installation & Running
1️⃣ Clone the repository
git clone https://github.com/your-username/auth-backend.git
cd auth-backend

2️⃣ Install dependencies
npm install

3️⃣ Start MongoDB

Make sure MongoDB is running locally or use MongoDB Atlas.

4️⃣ Run the server
npm run dev


or

npm start

🔑 API Endpoints
📝 Register User

POST /api/auth/register

{
  "name": "John Doe",
  "email": "john@gmail.com",
  "password": "123456"
}

🔐 Login User

POST /api/auth/login

{
  "email": "john@gmail.com",
  "password": "123456"
}


Response

{
  "message": "Login successful",
  "token": "JWT_TOKEN_HERE"
}

🛡 Protected Routes

Include the JWT token in request headers:

Authorization: Bearer <your_token>


Example:

router.get("/profile", authMiddleware, controller);

🔒 Security Highlights

🔑 Passwords are hashed before storage

⏱ JWT expires in 24 hours

🙈 Passwords excluded from responses

🚫 Unauthorized access blocked by middleware

🧪 Testing

Use tools like:

Postman

Thunder Client

Insomnia

Flow:

Register → Login → Copy Token → Access Protected Routes

🚀 Future Enhancements

🔄 Refresh Tokens

🧑‍🤝‍🧑 Role-based Authorization

📧 Email Verification

🔁 Forgot / Reset Password

⚡ Rate Limiting & Security Headers

📸 Screenshots

<img width="1476" height="490" alt="Screenshot 2026-02-06 123832" src="https://github.com/user-attachments/assets/cae6df56-1d55-44b9-a917-6d333b4f5b20" />


<img width="1473" height="495" alt="Screenshot 2026-02-06 123941" src="https://github.com/user-attachments/assets/02a28739-744a-4d1d-924e-59bb8e3e1dc5" />
