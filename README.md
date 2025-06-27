# StudyHub

StudyNotion aims to provide a seamless and interactive learning experience for students, making education more accessible and engaging. Additionally, the platform serves as a platform for instructors to showcase their expertise and connect with learners across the globe.

---

## Table of Contents

- [Introduction](#introduction)
- [System Architecture](#system-architecture)
  - [Front-end](#front-end)
  - [Back-end](#back-end)
  - [Database](#database)
- [Architecture Diagram](#architecture-diagram)
- [API Design](#api-design)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)

---

## Introduction

StudyHub is a full-stack EdTech platform built to offer an immersive learning experience. It provides interfaces for both students and instructors, supporting features such as user authentication, course creation, media management, payments, and more.

---

##  System Architecture

The StudyNotion platform follows a **client-server architecture** composed of three key layers:

- **Front-end**: Built using ReactJS
- **Back-end**: Built using NodeJS and ExpressJS
- **Database**: Powered by MongoDB

---

###  Front-end

The front-end uses **ReactJS**, styled with **CSS**, **Tailwind**, and uses **Redux** for state management. It interacts with the backend via **RESTful APIs**.

#### Student Pages:
- **Homepage**: Introduction and course links
- **Course List**: Displays all available courses
- **Wishlist**: Saved courses
- **Cart Checkout**: Course purchase flow
- **Course Content**: Videos and materials
- **User Details & Edit**: Manage profile

#### Instructor Pages:
- **Dashboard**: Course overview and feedback
- **Insights**: Views, clicks, analytics
- **Course Management**: Create/edit/delete courses
- **Profile Management**: Edit instructor profile

---

### 🛠️ Back-end

The backend is developed using **Node.js** and **Express.js**, and provides robust APIs to support authentication, course handling, payments, and media management.

#### Key Features:
- **Authentication** (JWT, Bcrypt, OTP, Forgot Password)
- **Course Management**
- **Payment Integration** (Razorpay)
- **Cloudinary Media Uploads**
-  **Markdown Content Support**

#### Libraries & Tools:
- Node.js, Express.js
- MongoDB + Mongoose
- JWT, Bcrypt
- Cloudinary API

#### Schemas:
- **Student**: name, email, password, courses
- **Instructor**: name, email, password, courses
- **Course**: title, description, instructor, media

---

###  Database

StudyNotion uses **MongoDB**, a NoSQL database perfect for flexible schema needs. All user and course data is securely stored and accessed using Mongoose models.

---

##  API Design

The backend follows REST principles and uses:
- **GET**, **POST**, **PUT**, **DELETE**
- **JSON** for data exchange

> For full API reference, see: `docs/API_DOCUMENTATION.md` or Postman collection.

---

##  Installation

Clone and set up the project:

```bash
git clone https://github.com/Varsha2635/StudyHub.git
cd StudyNotion
npm install
```

## Configuration
Create a .env file in the root folder and add:
```bash
MONGODB_URI=your-mongodb-connection-url
JWT_SECRET=your-jwt-secret-key
```
## Usage
Start the backend server:
```bash
npm start
```
Start the React frontend:
```bash
cd client
npm install
npm start
```
Then, open your browser and navigate to:
```bash
http://localhost:3000
```
