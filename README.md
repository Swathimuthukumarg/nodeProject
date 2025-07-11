# Task Manager API (MySQL + TypeORM + Node.js)

A simple task management system built using **Node.js**, **Express**, **TypeORM**, and **MySQL**.  
This project supports user authentication via **mobile number**, and provides APIs to manage tasks.

---

## Features

- Single Mobile Login + Register API
- JWT-based authentication
- Create, List, Update Tasks
- MySQL database integration with TypeORM
- Modular project structure

---

## Technology Stack

| Component       | Tech                     |
|----------------|--------------------------|
| Runtime         | Node.js                  |
| Framework       | Express.js               |
| ORM             | TypeORM                  |
| Language        | TypeScript               |
| Database        | MySQL                    |
| Auth            | JWT                      |
| Dev Tools       | ts-node-dev, dotenv      |

---

## File Structure

src/
├── config/ # TypeORM and environment setup
├── controllers/ # Business logic for Auth & Tasks
├── entities/ # DB Models using decorators
├── middlewares/ # JWT Auth middleware
├── routes/ # API route definitions
├── utils/ # Token generation helpers
└── server.ts # Express app entry point


## Instructions - How to start the APP

## ⚙️ Environment Variables

Create a `.env` file in the root directory:

DATABASE_URL=mysql://root:<your_password>@localhost:3306/taskdb
JWT_SECRET=your_jwt_secret

yaml
Copy
Edit

---

## 🛠️ Setup & Run

1. **Install dependencies**

bash
npm install
Create the database

In MySQL Workbench or CLI:

sql
CREATE DATABASE taskdb;
Run the server 

bash
npm run dev
Server will start at http://localhost:5000.

API Endpoints
Method	Endpoint	Auth Required	Description
POST --	/api/auth/mobile-login	--	Login or Register
POST -- /api/tasks	--	Create Task
GET	-- /api/tasks	--	List All Tasks
PUT	-- /api/tasks/:id --	Update Task by ID

All protected routes require JWT token in the Authorization header
