

# 🛒 E-Commerce Product API

**Assignment 2 – Express.js (In-Memory REST API)**

---

## 📌 Project Overview

This project is a simple **RESTful API** built using **Express.js** that manages product listings for an e-commerce platform.

The data is stored in an **in-memory JSON array** (No database used).

The API implements:

* ✅ 3 GET routes
* ✅ 1 POST route
* ✅ 3 PUT routes
* ✅ Proper REST principles
* ✅ Correct HTTP status codes

---

## 🚀 Tech Stack

* Node.js
* Express.js
* CORS
* In-Memory JSON Array

---

## 📂 Project Structure

```
ecommerce-product-api/
│
├── server.js
├── package.json
└── README.md
```

---

## 📦 Sample Product Structure

Each product follows this structure:

```js
{
  id: 1,
  name: "Wireless Mouse",
  category: "Electronics",
  price: 799,
  stock: 25,
  rating: 4.3
}
```

---

## 📊 Sample Initial Data

```js
const products = [
  {
    id: 1,
    name: "Wireless Mouse",
    category: "Electronics",
    price: 799,
    stock: 25,
    rating: 4.3
  },
  {
    id: 2,
    name: "Running Shoes",
    category: "Footwear",
    price: 2499,
    stock: 40,
    rating: 4.5
  },
  {
    id: 3,
    name: "Laptop Stand",
    category: "Accessories",
    price: 999,
    stock: 30,
    rating: 4.2
  },
  {
    id: 4,
    name: "Smart Watch",
    category: "Electronics",
    price: 4999,
    stock: 12,
    rating: 4.4
  },
  {
    id: 5,
    name: "Backpack",
    category: "Fashion",
    price: 1599,
    stock: 50,
    rating: 4.1
  }
];
```

---

# 📌 API Routes

---

## 🔹 GET Routes

---

### 1️⃣ GET `/products`

Returns all products.

**Status Code:** `200 OK`

Response:

```json
[
  { ...all products }
]
```

---

### 2️⃣ GET `/products/:id`

Returns product by ID.

Example:

```
GET /products/3
```

**If Found:**

* Status `200`
* Returns product object

**If Not Found:**

* Status `404`
* Message: `"Product not found"`

---

### 3️⃣ GET `/products/category/:categoryName`

Returns products by category.

Example:

```
GET /products/category/Electronics
```

**If Products Found:**

* Status `200`
* Returns filtered array

**If None Found:**

* Status `200`
* Returns empty array `[]`

---

## 🔹 POST Route

---

### 4️⃣ POST `/products`

Adds a new product.

Request Body:

```json
{
  "name": "Bluetooth Speaker",
  "category": "Electronics",
  "price": 2999,
  "stock": 20,
  "rating": 4.6
}
```

**Expected:**

* Auto-generate ID
* Add to products array
* Status `201 Created`
* Return created product

---

## 🔹 PUT Routes

---

### 5️⃣ PUT `/products/:id`

Replaces entire product (except ID).

Example:

```
PUT /products/2
```

Request Body:

```json
{
  "name": "Updated Shoes",
  "category": "Footwear",
  "price": 2699,
  "stock": 35,
  "rating": 4.7
}
```

**If Found:**

* Status `200`
* Return updated product

**If Not Found:**

* Status `404`

---

### 6️⃣ PUT `/products/:id/stock`

Updates only stock value.

Example:

```
PUT /products/2/stock
```

Request Body:

```json
{
  "stock": 60
}
```

**If Found:**

* Status `200`
* Return updated product

**If Not Found:**

* Status `404`

---

### 7️⃣ PUT `/products/:id/price`

Updates only price value.

Example:

```
PUT /products/3/price
```

Request Body:

```json
{
  "price": 1299
}
```

**If Found:**

* Status `200`
* Return updated product

**If Not Found:**

* Status `404`

---

# ⚙️ How to Run Locally

### 1️⃣ Clone Repository

```bash
git clone <your-repository-link>
cd ecommerce-product-api
```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Run Server

```bash
node server.js
```

Server will start at:

```
http://localhost:3000
```

---

# 🌐 Deployment

This API is deployed on Render.

🔗 **Live API Link:**
`https://server-assignment-02.onrender.com/`

---

# 📬 Postman Documentation

🔗 **Postman Collection Link:**
`https://documenter.getpostman.com/view/50840755/2sBXcGFfng`

All 7 routes are documented with:

* Sample Requests
* Sample Responses
* Proper Status Codes

---

# ✅ Features Implemented

* RESTful API design
* Proper middleware order
* express.json() usage
* CORS enabled
* Dynamic ID generation
* Clean route structure
* Correct HTTP status codes

---

# 👩‍💻 Author

**Name:** Mahi Patel

