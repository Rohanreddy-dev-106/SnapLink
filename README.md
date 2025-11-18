# 🚀 URL Shortener (Backend)

A backend service built with **Express** and **MongoDB** that converts
long URLs into short links.\
It stores the URL mapping in the database, redirects users from the
short link to the original URL, and keeps track of how many times each
short link is clicked.

## 📌 Features

-   Generate short URLs from long links
-   Redirect short URLs to their original destination
-   Track total clicks for each short URL
-   REST API built using Express.js
-   MongoDB database for storing URL mappings
-   Lightweight and fast

## 🛠 Tech Stack

-   **Node.js**
-   **Express.js**
-   **MongoDB**
-   **MongoDB Native Driver**
-   **NanoID** for generating unique short IDs

## 📂 Project Structure

    /project
     ├── controllers/
     ├── routes/
     ├── models/
     ├── config/
     ├── package.json
     ├── server.js
     └── README.md

## 🔄 API Endpoints

  Method   Endpoint         Description
  -------- ---------------- ------------------------------
  POST     `/shorten`       Create a new short URL
  GET      `/:shortCode`    Redirect to the original URL
  GET      `/stats/:code`   Get click count and details

## ▶️ Getting Started

### 1. Clone the repo

    git clone https://github.com/YOUR-USERNAME/URLShortener.git
    cd URLShortener

### 2. Install dependencies

    npm install

### 3. Set up environment variables

Create a `.env` file:

    MONGO_URL=your_mongodb_connection_string
    PORT=5000
    BASE_URL=http://localhost:5000

### 4. Run the server

    npm start

## 📊 Example MongoDB Document

    {
      shortCode: "abc123",
      originalUrl: "https://example.com/some/long/link",
      clickCount: 5,
      createdAt: "2025-01-01T10:00:00Z"
    }

## 🧾 License

This project is open-source and free to use.
