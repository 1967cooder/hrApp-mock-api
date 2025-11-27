# hrApp-mock-api

📘 HR App — README Template
📌 Overview

This project is a simple HR management application built with React (frontend) and a JSON Server backend deployed on Render.
It allows you to view, add, edit, and delete employees through a mock API.

📂 Project Structure
Frontend (React App)

Displays employee list

Allows CRUD operations

Fetches data from the deployed backend on Render

Backend (JSON Server)

Contains db.json with the employee data

Custom server setup using server.cjs

Serves API under /api prefix

Deployed on Render as a web service

🌐 Live URLs
🔵 Frontend Live App

## Live Demo

You can view the deployed frontend here: [HR App Live](https://1967cooder.github.io/hrApp/#/)

🟠 Backend Live API

Your deployed JSON Server on Render:

https://hrapp-mock-api.onrender.com/api/employees

📦 Repositories
🔵 Frontend GitHub Repo
https://github.com/1967cooder/hrApp

🟠 Backend GitHub Repo
https://github.com/1967cooder/hrApp-mock-api

⚙️ Backend Setup (JSON Server)
Files included:
db.json
server.cjs
package.json

Start command
npm start

server.cjs
const jsonServer = require("json-server");
const server = jsonServer.create();
const router = jsonServer.router("db.json");
const middlewares = jsonServer.defaults();

server.use("/api", middlewares, router);

server.listen(10000, () => {
console.log("JSON Server is running");
});

⚛️ Frontend Setup (React)
Install dependencies
npm install

Start dev server
npm start

API configuration (example)
const API_BASE =
process.env.NODE_ENV === "production"
? "https://hrapp-mock-api.onrender.com/api"
: "http://localhost:3000/api";

export default API_BASE;

🧪 Final Check

Frontend loads employee list from Render backend

Create, update, delete employee → works

API responds correctly at /api/employees

All URLs added to README

## Submission

**Frontend GitHub repo:** [HR App Frontend](https://github.com/1967cooder/hrApp)  
**Backend GitHub repo:** [HR App Backend](https://github.com/1967cooder/hrApp-mock-api)  
**Live frontend page:** [HR App Live](https://1967cooder.github.io/hrApp/#/)

**Live backend API:** [HR App Live API](https://hrapp-mock-api.onrender.com/api/employees)
