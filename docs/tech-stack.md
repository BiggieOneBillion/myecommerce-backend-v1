# Technology Stack

This document outlines the core technologies and tools used in the **eCommerce Backend** project.

## Backend Core
- **Runtime**: [Node.js](https://nodejs.org/) (v14.x or higher)
- **Framework**: [Express.js](https://expressjs.com/) - A fast, unopinionated, minimalist web framework for Node.js.
- **Database**: [MongoDB](https://www.mongodb.com/) with [Mongoose](https://mongoosejs.com/) - Elegant mongodb object modeling for node.js.

## Security
- **Helmet**: [helmet](https://helmetjs.github.io/) - Helps secure Express apps by setting various HTTP headers.
- **CORS**: [cors](https://www.npmjs.com/package/cors) - Middleware to enable Cross-Origin Resource Sharing.
- **NoSQL Injection Protection**: [express-mongo-sanitize](https://www.npmjs.com/package/express-mongo-sanitize) - Sanitizes user-supplied data to prevent MongoDB Operator Injection.
- **XSS Protection**: [xss-clean](https://www.npmjs.com/package/xss-clean) - Node.js Connect middleware to sanitize user input coming from POST body, GET queries, and url params.
- **HTTP Parameter Pollution**: [hpp](https://www.npmjs.com/package/hpp) - Middleware to protect against HTTP Parameter Pollution attacks.
- **Rate Limiting**: [express-rate-limit](https://www.npmjs.com/package/express-rate-limit) - Basic rate-limiting middleware for Express.
- **Password Hashing**: [bcryptjs](https://www.npmjs.com/package/bcryptjs) - Optimized bcrypt in JavaScript with zero dependencies.

## Authentication & Authorization
- **JWT**: [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken) - Implementation of JSON Web Tokens for secure session management.

## Media & Utilities
- **Image Processing**: [sharp](https://sharp.pixelplumbing.com/) - High-performance Node.js image processing.
- **File Uploads**: [multer](https://github.com/expressjs/multer) - Middleware for handling `multipart/form-data`, primarily used for uploading files.
- **Cloud Storage**: [Cloudinary](https://cloudinary.com/) - For managing and delivering optimized images and videos.
- **Email**: [Nodemailer](https://nodemailer.com/) - Module for Node.js applications to allow easy as cake email sending.
- **Validation**: [validator](https://www.npmjs.com/package/validator) - A library of string validators and sanitizers.
- **UUID**: [uuid](https://www.npmjs.com/package/uuid) - For the creation of RFC4122 UUIDs.
- **Slugify**: [slugify](https://www.npmjs.com/package/slugify) - For creating URL-friendly slugs.

## Quality & Development
- **Linting**: [ESLint](https://eslint.org/) (Airbnb config)
- **Formatting**: [Prettier](https://prettier.io/)
- **Process Manager**: [Nodemon](https://nodemon.io/) - Tool that helps develop node.js based applications by automatically restarting the node application when file changes in the directory are detected.
