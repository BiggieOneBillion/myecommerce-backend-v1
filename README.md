# eCommerce Backend API

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)

A robust, secure, and scalable RESTful API built for e-commerce platforms. This backend handles everything from authentication, product management, shopping carts, and order processing to review management and secure payments.

## 🚀 Overview

This project is built using **Node.js**, **Express**, and **MongoDB**. It provides a full-featured API for e-commerce applications with a focus on security, performance, and maintainability.

## 📚 Documentation

Detailed documentation is available in the `docs/` directory:

- 🛠 **[Tech Stack](./docs/tech-stack.md)**: Detailed breakdown of technologies used.
- 🏗 **[Architecture](./docs/architecture.md)**: MVC patterns, error handling, and project structure.
- 🏁 **[Getting Started](./docs/getting-started.md)**: Local setup and environment configuration.
- 🔌 **[API Reference](./docs/api-reference.md)**: Comprehensive list of endpoints and usage.
- 🚀 **[Deployment Guide](./docs/deployment.md)**: Instructions for Vercel, Render, and more.

## ✨ Key Features

- **User Authentication**: Secure signup/login with JWT and automated password hashing.
- **Product Management**: Full CRUD for products and categories with advanced filtering, sorting, and pagination.
- **Review System**: Users can leave reviews and ratings for products.
- **Shopping Cart**: Manage cart items with persistence.
- **Order Processing**: Workflow for handling customer orders.
- **Security**: Built-in protection against XSS, NoSQL Injection, and HTTP Parameter Pollution.
- **Media Management**: Image uploads and optimization with Multer, Sharp, and Cloudinary.
- **Error Handling**: Centralized error management for clean and consistent API responses.

## 🚦 Quick Start

```bash
# Install dependencies
npm install

# Run in development mode
npm run dev

# Run in production mode
npm start
```

## 📄 License

This project is licensed under the ISC License.
