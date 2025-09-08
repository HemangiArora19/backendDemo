# 📝 Notes API

A simple **RESTful API** built with **Node.js**, **Express**, and **MongoDB** that allows users to create, read, update, and delete notes.

---

## 🚀 Features

- 📄 Create new notes  
- 📥 Retrieve all notes  
- ✏️ Update a note by ID  
- ❌ Delete a note by ID  

---

## 🛠️ Tech Stack

- **Backend:** Node.js, Express.js  
- **Database:** MongoDB with Mongoose  
- **Environment:** dotenv  

---

## 📦 Installation


Install dependencies

bash
Copy code
npm install
Configure environment variables

Create a .env file in the root directory:

env
Copy code
PORT=5000
MONGODB_URI=your_mongodb_connection_string
Start the development server

bash
Copy code
npm start
Server will run on: http://localhost:5000

📡 API Endpoints
➕ POST /notes
Create a new note.

Request Body:

json
Copy code
{
  "title": "My Note",
  "content": "This is the content of the note."
}
Response:

json
Copy code
{
  "_id": "note_id",
  "title": "My Note",
  "content": "This is the content of the note.",
  "createdAt": "timestamp"
}
📥 GET /notes
Fetch all notes.

Response:

json
Copy code
[
  {
    "_id": "note_id",
    "title": "My Note",
    "content": "This is the content of the note.",
    "createdAt": "timestamp"
  },
  ...
]
✏️ PUT /notes/:id
Update a note by ID.

Request Body:

json
Copy code
{
  "title": "Updated Title",
  "content": "Updated Content"
}
Response:

json
Copy code
{
  "message": "Note updated successfully"
}
❌ DELETE /notes/:id
Delete a note by ID.

Response:

json
Copy code
{
  "message": "Note deleted successfully"
}
