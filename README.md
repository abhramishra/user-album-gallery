User Album Gallery
Learn and practice Redux Toolkit, Async Thunk, and RTK Query by building a simple project to explore Users, Albums, and Photos — powered by a mock backend using JSON Server.

🚀 Project Overview
This project is built to demonstrate:

State management using Redux Toolkit.

Async operations using createAsyncThunk.

Efficient data fetching and caching using RTK Query.

Working with hierarchical data (Users → Albums → Photos).

The backend APIs are simulated locally using JSON Server.

🌐 API Setup (JSON Server)
Make sure you have JSON Server installed globally:

bash
Copy
Edit
npm install -g json-server
Then create a db.json file in your project root (or use the provided one) with a structure like:

json
Copy
Edit
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
Start the server:

bash
Copy
Edit
json-server --watch db.json --port 3001
Your API will now be available at:

http://localhost:3001/users

http://localhost:3001/albums

http://localhost:3001/photos

🛠️ Tech Stack
React (Functional components + Hooks)

Redux Toolkit

createSlice

createAsyncThunk

createApi (RTK Query)

React Redux

Axios (or native Fetch)

JSON Server (Mock API)

(Optional) Tailwind CSS for styling

🧩 Project Features
Fetch and display a list of users

On selecting a user, fetch and display their albums

Expand an album to load and display its photos

Loading indicators and error handling

Separation of concerns with proper folder structure

State normalization and caching with RTK Query

📖 Learning Focus
This project is designed for developers who want to:

Understand Redux Toolkit's modern approach to Redux.

Master Async Thunks for API interaction.

Use RTK Query for auto-caching and efficient network calls.

Build scalable and organized front-end architecture.

📂 Folder Structure (Example)
bash
Copy
Edit
/src
  /app
    store.js
  /features
    /users
      usersSlice.js
      UsersList.jsx
    /albums
      albumsSlice.js
      AlbumsList.jsx
    /photos
      photosApi.js (RTK Query)
      PhotosList.jsx
  /components
    Loader.jsx
    Error.jsx
  /services
    api.js (axios setup if needed)
  App.jsx
  index.js
🛎️ Getting Started
Clone the repo:

bash
Copy
Edit
git clone https://github.com/your-username/user-album-gallery.git
cd user-album-gallery
Install dependencies:

bash
Copy
Edit
npm install
Start JSON Server:

bash
Copy
Edit
json-server --watch db.json --port 3001
Start React App:

bash
Copy
Edit
npm start
🎯 Future Improvements (Optional)
Add a search functionality for users or albums.

Add pagination for albums/photos.

Implement React Router for user/album pages.

Unit testing using Jest and React Testing Library.

📜 License
This project is licensed under the MIT License — feel free to use and adapt it!
