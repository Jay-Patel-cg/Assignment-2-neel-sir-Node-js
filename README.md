# 🛒 Assignment 2  
# E-Commerce Product REST API  
### (Express.js – In-Memory Database | GET, POST, PUT)

---

## 📌 Project Title  

E-Commerce Product Management REST API

---

## 🎯 Objective  

The objective of this assignment is to build a REST API using Node.js and Express.js that manages product data for an e-commerce platform using an in-memory JSON array.

This project demonstrates:

- REST API design principles  
- Implementation of GET, POST, and PUT routes  
- Route parameters handling  
- Filtering and update logic  
- Proper HTTP status codes  
- Middleware usage (CORS, express.json)  
- Professional API deployment  

No database, validation library, or authentication is used.  
All data is stored dynamically in a JSON array inside the project.

---

# 📦 Product Structure  

Each product follows this format:

{
  id: 1,
  name: "Wireless Mouse",
  category: "Electronics",
  price: 799,
  stock: 25,
  rating: 4.3
}

All logic works dynamically using the in-memory array.

---

# 🚀 List of Implemented Routes  

## ✅ GET Routes (3)

### 1️⃣ GET /products  
Returns all products.

- Status Code: 200  
- Returns full array  

---

### 2️⃣ GET /products/:id  

Example:
GET /products/3  

- Returns product by ID  
- If not found → 404  
- Uses req.params and find()  

---

### 3️⃣ GET /products/category/:categoryName  

Example:
GET /products/category/Electronics  

- Returns filtered products by category  
- If none found → returns empty array  
- Case-insensitive filtering implemented  

---

# ➕ POST Route (1)

### 4️⃣ POST /products  

Adds a new product.

Example Body:

{
  "name": "Bluetooth Speaker",
  "category": "Electronics",
  "price": 2999,
  "stock": 20,
  "rating": 4.6
}

Expected Behavior:

- Auto-generate ID  
- Push new product to array  
- Return 201 Created  
- Return created product  

---

# 🔄 PUT Routes (3)

### 5️⃣ PUT /products/:id  

Replaces entire product except ID.

- Status Code: 200  
- If not found → 404  
- Demonstrates full object replacement (PUT semantics)  

---

### 6️⃣ PUT /products/:id/stock  

Example:
PUT /products/2/stock  

Body:
{
  "stock": 60
}

- Updates only stock field  
- Returns updated product  
- 404 if not found  

---

### 7️⃣ PUT /products/:id/price  

Example:
PUT /products/3/price  

Body:
{
  "price": 1299
}

- Updates only price field  
- Returns updated product  
- 404 if not found  

---

# 🌐 Sample API URLs  

## 🔹 Base URL (Deployed)
https://assignment-2-neel-sir-node-js.onrender.com

## 🔹 Get All Products
https://assignment-2-neel-sir-node-js.onrender.com/products

## 🔹 Get Product by ID
https://assignment-2-neel-sir-node-js.onrender.com/products/1

## 🔹 Get Products by Category
https://assignment-2-neel-sir-node-js.onrender.com/products/category/Electronics

---

# 📬 Postman Documentation  

Public Postman Documentation Link:

https://documenter.getpostman.com/view/50839294/2sBXcGFLTd

Includes:

- All 7 routes  
- Sample request bodies  
- Sample responses  
- Proper HTTP status codes  

---

# 💻 Steps to Run Locally  

1️⃣ Clone Repository  

git clone https://github.com/your-username/ecommerce-product-api.git  

2️⃣ Navigate to Project Folder  

cd ecommerce-product-api  

3️⃣ Install Dependencies  

npm install  

4️⃣ Run Server  

npm start  

OR (if using nodemon)

npx nodemon index.js  

5️⃣ Open in Browser  

http://localhost:3000/products  

---

# 🛠 Technologies Used  

- Node.js  
- Express.js  
- CORS Middleware  
- In-Memory JSON Array  
- Render (Deployment)  
- Postman (Documentation)  

---

# 📂 Project Structure  

ecommerce-product-api/
│
├── node_modules/
├── package.json
├── package-lock.json
├── index.js
├── routes/
│   └── productRoutes.js
├── .gitignore
└── README.md

---

# ✅ Technical Requirements Fulfilled  

✔ Implemented 3 GET routes  
✔ Implemented 1 POST route  
✔ Implemented 3 PUT routes  
✔ Used express.json()  
✔ Used CORS middleware  
✔ Correct middleware order  
✔ Used proper HTTP status codes (200, 201, 404)  
✔ Fully in-memory logic  
✔ No database used  
✔ No validation library used  
✔ No authentication used  

---

# 📌 Submission Links  

GitHub Repository:
https://github.com/your-username/ecommerce-product-api

Postman Documentation:
https://documenter.getpostman.com/view/50839294/2sBXcGFLTd

Render Deployment:
https://assignment-2-neel-sir-node-js.onrender.com

---

# 🎓 Learning Outcomes  

After completing this assignment:

- Implemented RESTful GET, POST, and PUT APIs  
- Handled dynamic route parameters  
- Performed filtering and update logic  
- Understood PUT semantics  
- Used proper HTTP status codes  
- Deployed backend API professionally  
- Documented APIs using Postman  
