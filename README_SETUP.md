# Hekaya App Setup Instructions

Welcome to the Hekaya app! This README will guide you through the setup process, using the Gemini API, deploying to GitHub Pages, and an overview of all features.

## Table of Contents
- [1. Prerequisites](#1-prerequisites)
- [2. Setup Instructions](#2-setup-instructions)
- [3. Gemini API Usage](#3-gemini-api-usage)
- [4. Deploying to GitHub Pages](#4-deploying-to-github-pages)
- [5. Features Overview](#5-features-overview)

## 1. Prerequisites
Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm (Node package manager)

## 2. Setup Instructions
1. **Clone the repository**
   ```bash
   git clone https://github.com/wiwiwi135/Hekaya-app.git
   cd Hekaya-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run the application locally**
   ```bash
   npm start
   ```
   Open your browser and navigate to `http://localhost:3000`.

## 3. Gemini API Usage
To integrate with the Gemini API:
1. Sign up at [Gemini API](https://www.gemini.com) and get your API key.
2. In your application, create a file named `.env` and add your API key as follows:
   ```plaintext
   GEMINI_API_KEY=your_api_key_here
   ```
3. Use the API in your code:
   ```javascript
   const Gemini = require('gemini-api');
   const client = new Gemini({key: process.env.GEMINI_API_KEY});
   // Call Gemini API functions here
   ```

## 4. Deploying to GitHub Pages
1. **Build your application**
   ```bash
   npm run build
   ```
2. **Install GitHub Pages package** (if not already installed)
   ```bash
   npm install gh-pages --save-dev
   ```
3. **Add deployment scripts** in your `package.json`:
   ```json
   "scripts": {
       "deploy": "gh-pages -d build"
   }
   ```
4. **Deploy your application**
   ```bash
   npm run deploy
   ```
   Your app will be live at `https://<username>.github.io/Hekaya-app/`.

## 5. Features Overview
- **User Authentication**: Secure login and registration.
- **Real-time Data**: Get live updates from the Gemini API.
- **Responsive Design**: Works on desktop and mobile devices.
- **User Dashboard**: A personalized dashboard with user data.

For more information, check the documentation and explore the codebase!

Happy coding!