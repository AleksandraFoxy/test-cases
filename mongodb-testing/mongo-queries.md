# 🍃 MongoDB Practical Operations

Examples of working with NoSQL collections, filtering data, and performing CRUD operations using **MongoDB Compass** and **Shell**.

---

### 🔹 Task 1: Find All Documents
Request: Retrieve all products from the collection.

```javascript
db.products.find({});


🔹 Task 2: Filter by Price
Request: Find products with a price greater than 500.

JavaScript

db.products.find({ 
  price: { $gt: 500 } 
});


🔹 Task 3: Insert a New Product
Request: Add a new document to the products collection.

JavaScript

db.products.insertOne({
  name: "iPhone 15 Pro",
  manufacturer: "Apple",
  price: 1099,
  category: "Smartphones",
  inStock: true
});


🔹 Task 4: Delete Document
Request: Remove a product from the database by its name.

JavaScript

db.products.deleteOne({ name: "iPhone 15 Pro" });```