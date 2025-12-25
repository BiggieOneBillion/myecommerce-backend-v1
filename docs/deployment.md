# Deployment Guide

This guide provides instructions on how to deploy the **eCommerce Backend** to various platforms.

## General Requirements
Before deploying, ensure:
- Your database is hosted (e.g., MongoDB Atlas).
- All environment variables are properly set in your hosting provider's configuration.

## Vercel
Since this project includes a `vercel.json` file, it is optimized for Vercel.

1. Install Vercel CLI or use the Vercel Dashboard.
2. Link your repository.
3. Configure environment variables in the Vercel dashboard.
4. Deploy:
   ```bash
   vercel --prod
   ```

## Render
1. Create a "Web Service" on Render.
2. Connect your GitHub repository.
3. Select "Node" as the Environment.
4. Set the Build Command: `npm install`
5. Set the Start Command: `node server.js`
6. Add your Environment Variables in the "Environment" tab.

## Heroku
1. Create a new app on Heroku.
2. Set the config vars:
   ```bash
   heroku config:set DATABASE=mongodb+srv://...
   heroku config:set DATABASE_PASSWORD=...
   # ... other variables
   ```
3. Push your code:
   ```bash
   git push heroku main
   ```

## Netlify (Functions)
While this is a full Express app, it can be adapted for Netlify Functions using `serverless-http`, though Vercel or Render are recommended for primary hosting.
