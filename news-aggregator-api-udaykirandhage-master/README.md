
```markdown
# 📰 Personalized News Aggregator API

A RESTful API built using **Node.js**, **Express.js**, **JWT**, **bcrypt**, and **MongoDB** for delivering personalized news articles based on user preferences. This guided project is ideal for mastering authentication, input validation, middleware, secure API design, and external API integration.

## 🚀 Features

- ✅ **User Registration & Login**
  - Secure password hashing with bcrypt
  - Token-based authentication using JWT

- 🛡️ **Authentication Middleware**
  - Protect routes using JWT verification

- ⚙️ **User Preferences**
  - Store and retrieve user-specific news preferences
  - Update preferences (e.g., categories, language)

- 🌐 **News Integration**
  - Fetch top headlines via an external News API (like NewsAPI)
  - Serve personalized news content

- 📬 **Input Validation & Error Handling**
  - Validate requests (e.g., email format, password strength)
  - Graceful handling of API errors, authentication failures, and invalid inputs

## 📁 Project Structure

```
├── app.js           # Entry point
├── controllers/     # Route logic (auth, preferences, news)
├── routes/          # API endpoints
├── middlewares/     # JWT authentication & validation
├── Database/        # Database connection/config
├── test/            # API test cases (Postman or Jest)
├── .env             # Environment variables
└── README.md        # You're reading it!
```

## 🔐 Authentication Flow

1. **POST /register**: Create a user with hashed password 
2. **POST /login**: Authenticate and receive a JWT 
3. **JWT Middleware**: Protects `/preferences` and `/news` routes 

## 🧪 API Endpoints

| Endpoint          | Method | Auth Required | Description                             |
|-------------------|--------|---------------|-----------------------------------------|
| `/register`       | POST   | ❌            | Register a new user                    |
| `/login`          | POST   | ❌            | Authenticate user and return JWT       |
| `/preferences`    | GET    | ✅            | Get user preferences                    |
| `/preferences`    | PUT    | ✅            | Update user preferences                 |
| `/news`           | GET    | ✅            | Fetch personalized news articles        |

## 🔧 Technologies Used

- **Node.js** & **Express.js**
- **MongoDB** with **Mongoose**
- **bcrypt** for password hashing
- **jsonwebtoken** (JWT) for secure access control
- **axios** for external API calls
- **dotenv** for environment config
- **Postman** or `curl` for testing

## 📦 Setup & Installation

```bash
# Clone the repo
git clone https://github.com/your-username/news-aggregator-api.git
cd news-aggregator-api

# Install dependencies
npm install

# Set environment variables
cp .env.example .env

# Run the app
npm start
```

## 🔐 .env Example

```
PORT=3000
MONGO_URI=mongodb://localhost:27017/news-app
JWT_SECRET=your_jwt_secret
NEWS_API_KEY=your_newsapi_key
```


