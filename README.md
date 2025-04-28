# User Album Gallery

Learn and practice **Redux Toolkit**, **Async Thunk**, and **RTK Query** by building a simple project to explore Users, Albums, and Photos — powered by a mock backend using **JSON Server**.

---

## 🚀 Project Overview

This project is built to demonstrate:
- State management using **Redux Toolkit**.
- Async operations using **createAsyncThunk**.
- Efficient data fetching and caching using **RTK Query**.
- Working with hierarchical data (Users → Albums → Photos).

The backend APIs are simulated locally using **JSON Server**.

---

## 🌐 API Setup (JSON Server)

Make sure you have **JSON Server** installed globally:

```bash
npm install -g json-server

## Create a db.json file in your project root with a structure like:

{
  "users": [
    { "id": 1, "name": "John Doe" },
    { "id": 2, "name": "Jane Smith" }
  ],
  "albums": [
    { "id": 1, "userId": 1, "title": "John's First Album" },
    { "id": 2, "userId": 1, "title": "John's Second Album" },
    { "id": 3, "userId": 2, "title": "Jane's Album" }
  ],
  "photos": [
    { "id": 1, "albumId": 1, "title": "Photo 1", "url": "https://via.placeholder.com/150" },
    { "id": 2, "albumId": 1, "title": "Photo 2", "url": "https://via.placeholder.com/150" },
    { "id": 3, "albumId": 2, "title": "Photo 3", "url": "https://via.placeholder.com/150" }
  ]
}

## Start the server:
json-server --watch db.json --port 3001

🛎️ Getting Started
1. Clone the repo
git clone https://github.com/your-username/user-album-gallery.git
cd user-album-gallery

2. Install dependencies
npm install

3. Start JSON Server
json-server --watch db.json --port 3001

4. Start React app
npm start




