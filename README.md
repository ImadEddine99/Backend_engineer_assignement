E-commerce Product API – Developer Assignment

This is a simple RESTful API for an e-commerce platform to retrieve products filtered by category. It is built using Node.js, Express, and MongoDB (via Mongoose).

=======================   Tech Stack:
- Node.js
- Express.js
- MongoDB with Mongoose

=======================   How to Run the Project:
1. Clone the repository:
   git clone https://bitbucket.org/ecommerce-assignment/ecommerce.git
   cd ecommerce

2. (Optional) Switch to the assignment branch:
   git checkout product-api-assignment

3. Install the project dependencies:
   npm install

4. Start the server:
   npm start

The server will run on http://localhost:4000 or http://localhost:4001 if 4000 is used

=======================   API Endpoint:
GET /api/products/category/:category (route in ecommerce\api\routes\productRoute.js)


function "getProductsByCategory" in api\controllers\productController.js

This endpoint returns all products within a specific category.

=======================   Example request using curl:
curl http://localhost:4000/api/products/category/Apparel

=======================   Example successful response:
{
  "success": true,
  "filteredProducts": [
    {
      "_id": "60f7df0f5b4c1c3adcb67890",
      "name": "T-Shirt",
      "description":"This is a T-shirt",
      "highlights":"highlights...",
      ....
      "category": "Apparel",
      "price": 29.99
    }
  ]
}

=======================   Example error response (if no products found):
{
  "success": false,
  "message": "No products found in this category"
}

=======================   Notes:
- The newly added API endpoint : GET /products/category/:category to filter products by the 'category' field
- If no matching products are found, it returns a 404 error.
- Make sure your database has products with valid 'category' values (e.g., Apparel, Electronics).


