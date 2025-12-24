# PRODIGY_BD_02 – REST API with Database Integration

## 📌 Project Overview
This project extends a basic REST API by integrating a relational database for persistent storage.  
The API is built using **Node.js** and **Express**, with **MySQL** as the database and **Sequelize ORM** for database operations.

This task demonstrates database integration, ORM usage, migrations, environment variable management, and connection pooling.

---

## 🛠️ Tech Stack
- **Node.js**
- **Express.js**
- **MySQL**
- **Sequelize (ORM)**
- **dotenv**
- **Postman** (for API testing)

---

## 📂 Project Structure
PRODIGY_BD_02/
│
├── app.js
├── config/
│ └── config.js
├── models/
│ ├── index.js
│ └── user.js
├── migrations/
├── routes/
│ └── userRoutes.js
├── .gitignore
├── package.json
└── README.md

---

## ⚙️ Environment Configuration
Environment variables are managed using a `.env` file (not pushed to GitHub).

Example:
DB_HOST=localhost
DB_USER=api_user
DB_PASSWORD=your_password
DB_NAME=prodigy_api
DB_DIALECT=mysql
PORT=3000

---

## 🗄️ Database Setup
- MySQL database is used for persistent storage.
- Sequelize ORM is used to define models and interact with the database.
- Database migrations are used to create the `Users` table.
- Connection pooling is enabled through Sequelize configuration.

---

## 🚀 How to Run the Project

1. Install dependencies:
```bash
npm install
Run database migrations:

npx sequelize-cli db:migrate


Start the server:

node app.js


Server runs on:

http://localhost:3000

🔗 API Endpoints
➕ Create User

POST /users

Request Body:

{
  "name": "Amit",
  "email": "amit@gmail.com",
  "age": 21
}

📄 Get All Users

GET /users

🔍 Get User by ID

GET /users/:id