# MongoDB + Node.js Integration Template

A beginner-friendly REST API template demonstrating how to connect **Node.js** with **MongoDB** using **Mongoose**. Covers full CRUD operations on a `Users` collection.

---

## 📁 Project Structure

```
Mongodb/
├── models/
│   └── User.js       # Mongoose schema for Users
├── server.js         # Express server + all API routes
├── package.json      # Project metadata & scripts
└── .gitignore
```

---

## ⚙️ Prerequisites

Make sure you have the following installed before running this project:

- [Node.js](https://nodejs.org/) (v16 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community) (running locally)
- [Postman](https://www.postman.com/) or any API testing tool (optional)

---

## 🚀 How to Run

Follow these steps in order:

### Step 1 — Clone or Download the Project

```bash
git clone <your-repo-url>
cd Mongodb
```

> If you already have the folder, just open it in your terminal.

---

### Step 2 — Install Dependencies

```bash
npm install
```

This installs **Express** and **Mongoose** listed in `package.json`.

---

### Step 3 — Start MongoDB Locally

Make sure your local MongoDB server is running. Open a **separate terminal** and run:

```bash
mongod
```

> By default, it runs on `mongodb://localhost:27017`. The project connects to a database named `mycoursesdb`.

---

### Step 4 — Start the Server

**For development** (auto-restarts on file changes):
```bash
npm run dev
```

**For production / normal run:**
```bash
npm start
```

You should see:
```
✅ MongoDB Connected
🚀 Server running on http://localhost:3000
```

---

## 🔌 API Endpoints

| Method   | Endpoint       | Description          |
|----------|----------------|----------------------|
| `POST`   | `/users`       | Create a new user    |
| `GET`    | `/users`       | Get all users        |
| `GET`    | `/users/:id`   | Get a user by ID     |
| `PUT`    | `/users/:id`   | Update a user by ID  |
| `DELETE` | `/users/:id`   | Soft delete a user   |

---

## 📦 Example Request — Create a User

**POST** `http://localhost:3000/users`

```json
{
  "name": "Vivek Pandey",
  "email": "vivek@example.com",
  "age": 22,
  "phone": "9876543210"
}
```

---

## 🧩 User Schema

| Field       | Type    | Required | Default |
|-------------|---------|----------|---------|
| `name`      | String  | ✅ Yes   | —       |
| `email`     | String  | ✅ Yes   | —       |
| `age`       | Number  | ❌ No    | —       |
| `phone`     | String  | ❌ No    | —       |
| `isDeleted` | Boolean | ❌ No    | `false` |

> **Note:** Delete is a **soft delete** — it sets `isDeleted: true` instead of removing the document.

---

## 🛠 Tech Stack

- **Runtime:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB (local)
- **ODM:** Mongoose

---

## 📄 License

This project is for **educational purposes** only.
