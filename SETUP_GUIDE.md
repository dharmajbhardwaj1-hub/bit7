# Mushify B2B Platform Setup Guide with Google OAuth

## Introduction
This guide provides a complete setup for the Mushify B2B platform with Google OAuth integration.

## Prerequisites
- Node.js (version 14 or higher)
- npm (Node Package Manager)
- MongoDB (or any database of your choice)
- A Google Cloud account for OAuth configuration

## Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/dharmajbhardwaj1-hub/bit7.git
   cd bit7
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Set Up Environment Variables**
   Create a `.env` file in the root directory and add the following:
   ```
   PORT=3000
   MONGODB_URI=mongodb://<username>:<password>@localhost:27017/mushify
   GOOGLE_CLIENT_ID=<your-google-client-id>
   GOOGLE_CLIENT_SECRET=<your-google-client-secret>
   CALLBACK_URL=http://localhost:3000/auth/google/callback
   ```

4. **Start the Application**
   ```bash
   npm start
   ```

## Google OAuth Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project or select an existing one.
3. Navigate to "APIs & Services" > "Credentials".
4. Click on "Create Credentials" and select "OAuth 2.0 Client IDs".
5. Configure the consent screen.
6. Set the application type to "Web application".
7. Add the authorized redirect URI as specified in the `.env` file.
8. Save your Client ID and Client Secret.

## File Structure Overview

```
bit7/
│
├── src/
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── middlewares/
│   └── app.js
├── .env
├── package.json
└── README.md
```

## Running the Application
- Once you have completed the steps above, you can run the application by executing:
  ```bash
  npm start
  ```
- Visit `http://localhost:3000` to see the application in action.
