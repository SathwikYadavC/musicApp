# 🎵 MusicApp Backend

A Spotify-inspired music platform backend built using **Node.js, Express.js, and MongoDB**. The application supports user authentication, role-based authorization, music uploads, album management, and cloud-based media storage.

## 🚀 Tech Stack

| Technology | Purpose                   |
|------------|---------------------------|
| Node.js    | JavaScript runtime        |
| Express.js | Backend framework         |
| MongoDB    | Database                  |
| Mongoose   | ODM and data modelling    |
| JWT        | Authentication            |
| bcryptjs   | Password hashing          |
| Multer     | File upload handling      |
| ImageKit   | Cloud media storage       |
| dotenv     | Environment configuration |

## ✨ Features

### 1. Authentication
- User registration and login.
- Password hashing using bcrypt.
- JWT-based authentication.
- Token storage using cookies.

### 2. Role-Based Authorization
- Separate user and artist roles.
- Custom authentication middleware.
- Protected endpoints based on user roles.
- Artists can upload music and create albums.
- Users can access music and album retrieval endpoints.

### 3. Music Management
- Upload music files using Multer.
- Store uploaded media in ImageKit.
- Save music metadata and cloud URLs in MongoDB.
- Retrieve available music tracks.

### 4. Album Management
- Create albums associated with artists.
- Associate multiple music records with an album.
- Retrieve all albums.
- Fetch individual albums with populated music and artist information.

## 🏗️ Project Structure

```text
musicApp/
│
├── server.js
│
├── src/
│   ├── app.js
│   │
│   ├── controllers/
│   │   ├── auth.controller.js
│   │   └── music.controller.js
│   │
│   ├── db/
│   │   └── db.js
│   │
│   ├── middlewares/
│   │   └── auth.middleware.js
│   │
│   ├── models/
│   │   ├── user.model.js
│   │   ├── music.model.js
│   │   └── album.model.js
│   │
│   ├── routes/
│   │   ├── auth.routes.js
│   │   └── music.routes.js
│   │
│   └── services/
│       └── storage.service.js
│
├── .env
├── .gitignore
└── package.json
```

## 🔌 API Endpoints

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new account |
| POST | `/api/auth/login` | Authenticate an existing account |

### Music

| Method | Endpoint | Access | Description |
|---|---|---|---|
| POST | `/api/music/upload` | Artist | Upload a music file |
| GET | `/api/music/` | User | Retrieve all music |

### Albums

| Method | Endpoint | Access | Description |
|---|---|---|---|
| POST | `/api/music/album` | Artist | Create an album |
| GET | `/api/music/albums` | User | Retrieve all albums |
| GET | `/api/music/album/:id` | User | Retrieve album details |

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/SathwikYadavC/musicApp.git
cd musicApp
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the root directory:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
```

### 4. Start the application

Development mode:

```bash
npm run dev
```

Production mode:

```bash
npm start
```

The server currently listens on port **3000**.

## 🧠 Key Learning Outcomes

- Building RESTful APIs using Express.js.
- Implementing JWT authentication and role-based authorization.
- Designing MongoDB schemas and document relationships.
- Handling multipart file uploads using Multer.
- Integrating third-party cloud storage using ImageKit.
- Structuring backend applications using routes, controllers, models, middleware, and services.

## 📌 Project Status

Under development. Additional features and improvements will be added.

## 👨‍💻 Author

**Sathwik Yadav**

GitHub: [SathwikYadavC](https://github.com/SathwikYadavC)

Repository: [MusicApp](https://github.com/SathwikYadavC/musicApp)
