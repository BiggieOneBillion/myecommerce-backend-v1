# API Reference

The **eCommerce Backend** provides a robust RESTful API for managing an online store. All endpoints are prefixed with `/api/v1`.

## Authentication
Most endpoints require authentication. Include the JWT token in the `Authorization` header:
`Authorization: Bearer <your_token>`

---

## Endpoints

### Users
- `POST /users/signup` - Register a new user
- `POST /users/login` - Login user
- `GET /users/logout` - Logout user
- `GET /users/me` - Get current user profile
- `PATCH /users/updateMe` - Update current user profile
- `DELETE /users/deleteMe` - Deactivate current user account

### Products
- `GET /products` - Get all products (supports filtering, sorting, pagination)
- `GET /products/:id` - Get a single product
- `POST /products` - Create a new product (Admin only)
- `PATCH /products/:id` - Update a product (Admin only)
- `DELETE /products/:id` - Delete a product (Admin only)

### Categories
- `GET /categories` - Get all categories
- `GET /categories/:id` - Get a single category
- `POST /categories` - Create a new category (Admin only)
- `PATCH /categories/:id` - Update a category (Admin only)
- `DELETE /categories/:id` - Delete a category (Admin only)

### Cart
- `GET /carts` - Get the current user's cart
- `POST /carts` - Add item to cart
- `PATCH /carts/:id` - Update cart item quantity
- `DELETE /carts/:id` - Remove item from cart

### Orders
- `GET /orders` - Get current user's orders
- `GET /orders/:id` - Get order details
- `POST /orders` - Place a new order

### Reviews
- `GET /reviews` - Get all reviews
- `GET /products/:productId/reviews` - Get reviews for a specific product
- `POST /reviews` - Create a new review
- `PATCH /reviews/:id` - Update a review
- `DELETE /reviews/:id` - Delete a review

### Payments
- `POST /payments/checkout-session` - Create a payment checkout session (Stripe integration)

---

## Standard Features
- **Filtering**: `GET /products?price[gte]=500`
- **Sorting**: `GET /products?sort=-price,ratingsAverage`
- **Field Limiting**: `GET /products?fields=name,price,description`
- **Pagination**: `GET /products?page=2&limit=10`
