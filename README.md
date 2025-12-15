# 🎓 Student Management System (Memory Version)

This is a **Student Management System** built using **Node.js, Express, and EJS** where student data is stored in an **in-memory JavaScript array** instead of a database.

> ⚠️ **Important Note**
> This project was intentionally built **without a database** to focus on understanding **backend fundamentals** such as routing, CRUD operations, and partial updates.

A **database-backed version (MySQL)** of this same project is available here 👉
🔗 [https://github.com/nitishyadav108/studentManagement2](https://github.com/nitishyadav108/studentManagement2)

---

## 🚀 Features

* ➕ Add new students
* 📋 View all students
* ✏️ Edit student details
* ♻️ Update **only selected fields** (PATCH)
* 🗑️ Delete students
* 🧠 Clean handling of request data
* 🎯 Focus on backend logic without database complexity

---

## 🛠️ Tech Stack

| Technology          | Description            |
| ------------------- | ---------------------- |
| **Node.js**         | Backend runtime        |
| **Express.js**      | Web framework          |
| **EJS**             | Template engine        |
| **UUID**            | Unique student IDs     |
| **Method-Override** | Enables PATCH & DELETE |
| **HTML / CSS**      | Frontend styling       |

---

## 📂 Project Structure

```text
studentManagement/
│
├── views/              # EJS templates
│   ├── home.ejs
│   ├── add.ejs
│   └── edit.ejs
│
├── public/             # Static files
│   └── style.css
│
├── index.js            # Main server file
├── package.json
├── package-lock.json
└── README.md
```

---

## ⚙️ Installation & Setup

### 🔹 1️⃣ Clone the Repository

```bash
git clone https://github.com/nitishyadav108/studentManagement.git
cd studentManagement
```

---

### 🔹 2️⃣ Install Dependencies

```bash
npm install
```

---

### 🔹 3️⃣ Start the Server

```bash
nodemon index.js
```

or

```bash
node index.js
```

Server runs on:

```
http://localhost:8080
```

---

## 🧠 How Data is Stored

All student data is stored in a **JavaScript array**:

```js
let students = [];
```

⚠️ This means:

* Data resets when the server restarts
* No database is used
* Perfect for learning backend logic

---

## 🔁 Routes Overview

| Method | Route            | Description            |
| ------ | ---------------- | ---------------------- |
| GET    | `/home`          | View all students      |
| GET    | `/home/new`      | Add student form       |
| POST   | `/home`          | Add new student        |
| GET    | `/home/:id/edit` | Edit student           |
| PATCH  | `/home/:id`      | Update selected fields |
| DELETE | `/home/:id`      | Delete student         |

---

## ♻️ Partial Update Logic (PATCH)

This project correctly implements **PATCH** logic:

* Only the fields sent from the form are updated
* Fields not sent remain unchanged

### Example

```json
{
  "course": "BCA",
  "maths": 78
}
```

✔ Updates only `course` and `maths`
✔ Other values remain the same

---

## 📌 Key Learnings

* Express routing & middleware
* CRUD operations without database
* Difference between **PUT vs PATCH**
* Request body handling
* Server-side logic building
* Clean backend architecture

---

> ✅ A MySQL version of this project is already implemented here:
> 🔗 [https://github.com/nitishyadav108/studentManagement2](https://github.com/nitishyadav108/studentManagement2)

---

## 👨‍💻 Author

**Nitish Yadav**
Aspiring **Full-Stack Web Developer**

* GitHub: [@nitishyadav108](https://github.com/nitishyadav108)

---

## ⭐ Support

If you find this project useful:

* ⭐ Star the repository
* 🍴 Fork it
* 🧠 Learn and build on it

---

