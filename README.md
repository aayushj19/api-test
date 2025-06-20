# 📚 Book API Server

A custom Node.js + Express server exposing CRUD APIs to manage a list of books using MongoDB.

---

## 🚀 Features
- Custom REST API with 5 endpoints
- MongoDB database integration
- Modular code structure (MVC)
- Ready to extend with a frontend or deploy

---

## 🛠️ How to Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com/aayushj19/api-test.git
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set Up .env
Create a .env file in the server/ directory:

```bash
PORT = 5000
MONGO_URI=your-mongo-db-url  
```

### 4.Run the Server
```bash
npm start
```
Server runs on http://localhost:5000


### API ENDPOINTS

| Method | Endpoint     | Description      |
| ------ | ------------ | ---------------- |
| GET    | `/books`     | Get all books    |
| GET    | `/books/:id` | Get a book by ID |
| POST   | `/books`     | Add a new book   |
| PUT    | `/books/:id` | Update a book    |
| DELETE | `/books/:id` | Delete a book    |

🔍 Sample Book Object
```json
{
  "title": "The Hobbit",
  "author": "J.R.R. Tolkien",
  "publishedYear": 1937,
  "genre": "Fantasy"
}
```

### 🧪 Testing with curl
Create a book:
```bash

curl -X POST http://localhost:5000/books \
-H "Content-Type: application/json" \
-d '{"title":"1984","author":"George Orwell","publishedYear":1949,"genre":"Dystopian"}'
```
