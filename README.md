# SIT323 - 2025 - Practical 5P: Dockerised Node.js Web Application

This project demonstrates how to containerise a simple Node.js web application using Docker and Docker Compose as part of the SIT323 Practical Task 5P.

---

## 📚 Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Running the App](#running-the-app)
- [Dockerfile Explanation](#dockerfile-explanation)
- [Docker Compose Explanation](#docker-compose-explanation)
- [Pushing to GitHub](#pushing-to-github)
- [Submission Checklist](#submission-checklist)

---

## 📌 Project Overview

This Node.js web application:
- Uses the Express framework
- Serves a "Hello from Dockerized Node App!" message on `http://localhost:3000`
- Is fully Dockerised using a `Dockerfile` and `docker-compose.yml`

---

## ✅ Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/)
- A GitHub account

---

## ⚙️ Installation & Setup

### 1. Clone this repository

```bash
git clone https://github.com/oyeyuvii/sit323-2025-prac5p.git
cd sit323-2025-prac5p
2. Install dependencies (Optional if not using Docker)
npm install
🚀 Running the App

Using Docker Compose
docker-compose up
Then open your browser and go to:

http://localhost:3000

You should see:

Hello from Dockerized Node App!

🐳 Dockerfile Explanation

FROM node:18
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
Uses official Node.js v18 base image
Copies code and installs dependencies
Exposes port 3000
Starts the app using npm start
🧩 Docker Compose Explanation

version: "3"
services:
  web:
    build: .
    ports:
      - "3000:3000"
Defines a single service called web
Builds the image from the local Dockerfile
Maps container port 3000 to host port 3000
☁️ Pushing to GitHub

Initial Commit & Push
git init
git add .
git commit -m "Initial commit - SIT323 Prac5P"
git branch -M main
git remote add origin https://github.com/oyeyuvii/sit323-2025-prac5p.git
git push -u origin main
📝 Submission Checklist

 Application built with Node.js and Express
 Dockerfile created and working
 Docker Compose file created and tested
 Code pushed to GitHub repository
 README file created with documentation
 Link submitted to OnTrack
