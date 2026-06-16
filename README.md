# User Management CRUD Application

A simple CRUD (Create, Read, Update, Delete) web application built using **Node.js**, **Express.js**, **MongoDB**, **Mongoose**, and **EJS**. Users can be created, viewed, updated, and deleted through a clean web interface.

---

## Features

* Create new users
* View all users
* Edit existing user details
* Delete users
* Server-side rendering using EJS
* MongoDB database integration with Mongoose

---

## Tech Stack

* Node.js
* Express.js
* MongoDB
* Mongoose
* EJS
* HTML/CSS

---

## Project Structure

```
project/
│
├── models/
│   └── user.js
│
├── views/
│   ├── index.ejs
│   ├── read.ejs
│   └── edit.ejs
│
├── public/
│
├── app.js
├── package.json
└── README.md
```

---

## Installation

### 1. Clone the repository

### 2. Install dependencies

```bash
npm install
```

### 3. Configure MongoDB

Create a MongoDB connection file and ensure your database is connected before starting the server.

Example:

```javascript
const mongoose = require("mongoose");

mongoose.connect("mongodb://127.0.0.1:27017/userdb");

module.exports = mongoose.connection;
```

### 4. Start the server

```bash
node app.js
```

or

```bash
nodemon app.js
```

---

## Routes

### Home Page

| Method | Route | Description      |
| ------ | ----- | ---------------- |
| GET    | /     | Render home page |

### Create User

| Method | Route   | Description       |
| ------ | ------- | ----------------- |
| POST   | /create | Create a new user |

### Read Users

| Method | Route | Description       |
| ------ | ----- | ----------------- |
| GET    | /read | Display all users |

### Update User

| Method | Route           | Description         |
| ------ | --------------- | ------------------- |
| GET    | /edit/:userid   | Open edit form      |
| POST   | /update/:userid | Update user details |

### Delete User

| Method | Route       | Description   |
| ------ | ----------- | ------------- |
| GET    | /delete/:id | Delete a user |

---

## User Schema Example

```javascript
const mongoose = require("mongoose");

const userSchema = mongoose.Schema({
    name: String,
    email: String,
    image: String
});

module.exports = mongoose.model("User", userSchema);
```

---

### Home Page

* Add a new user using the form.

### Users Page

* View all users.
* Edit user details.
* Delete users.

---

## Future Improvements

* Form validation
* User authentication
* Search functionality
* Pagination
* Profile image uploads using Multer
* REST API support

---

## Author

Developed using Node.js, Express, MongoDB, and EJS as a beginner-friendly CRUD project.
