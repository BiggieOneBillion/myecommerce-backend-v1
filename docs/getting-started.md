# Getting Started

Follow these instructions to set up things and get the project running on your local machine.

## Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v14.x or higher)
- [npm](https://www.npmjs.com/) (usually comes with Node.js)
- [MongoDB](https://www.mongodb.com/try/download/community) (either local installation or MongoDB Atlas account)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd myecommerce-backend-v1
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure Environment Variables:
   Create a `.env` file in the root directory and add the following:
   ```env
   NODE_ENV=development
   PORT=5000
   DATABASE=mongodb+srv://<username>:<password>@cluster0.mongodb.net/ecommerce
   DATABASE_PASSWORD=your_database_password

   JWT_SECRET=your_secret_key
   JWT_EXPIRES_IN=90d
   JWT_COOKIE_EXPIRES_IN=90

   EMAIL_USERNAME=your_email_username
   EMAIL_PASSWORD=your_email_password
   EMAIL_HOST=smtp.mailtrap.io
   EMAIL_PORT=2525

   CLOUDINARY_CLOUD_NAME=your_cloud_name
   CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret
   ```

## Running the Application

### Development Mode
Runs the server with `nodemon` for automatic restarts:
```bash
npm run dev
```

### Production Mode
Runs the server with standard `node`:
```bash
npm start
```

### Debug Mode
```bash
npm run debug
```

## Seeding Data
If you need to seed the database with sample data, check the `dev-data/` folder for relevant scripts or use the provided JSON files with custom import logic.
