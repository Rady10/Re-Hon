# Re-Hon — E-Book Marketplace

<p align="center">
  <strong>A Full-Stack Cross-Platform E-Book Marketplace</strong>
</p>

<p align="center">
  Built with Flutter, Node.js, Express, and MongoDB
</p>

---

## 📖 Overview

**Re-Hon** is a full-stack, cross-platform e-book marketplace designed to provide users with a simple and seamless way to **discover, search, sell, and read digital books**.

The application combines a modern Flutter frontend with a RESTful backend built using Node.js and Express. It provides user authentication, book management, cloud file storage, and a responsive user experience across multiple platforms.

---

## ✨ Features

* 📚 **Browse Books** — Explore available e-books through a clean and intuitive interface.
* 🔍 **Search & Discover** — Find books and explore their details.
* 🛒 **E-Book Marketplace** — List and trade digital books.
* 📖 **Digital Reading** — Access and read available e-books.
* 🔐 **Authentication** — Secure registration and login using JWT.
* 🔒 **Password Security** — Passwords are securely hashed using bcrypt.
* ☁️ **Cloud Storage** — Images and files are managed through Cloudinary.
* 🌐 **Cross-Platform** — Flutter enables deployment across Android, iOS, Web, and Desktop.
* 🎨 **Modern UI** — Responsive interface with custom components, splash screens, and Google Fonts.
* ⚡ **RESTful API** — Backend services built with Express.js and MongoDB.

---

## 🏗️ System Architecture

Re-Hon follows a **client-server architecture**:

```text
┌──────────────────────────────────────┐
│            Flutter Client            │
│                                      │
│  UI → User Interaction → HTTP API   │
└──────────────────┬───────────────────┘
                   │
                   │ REST API
                   ▼
┌──────────────────────────────────────┐
│          Node.js + Express           │
│                                      │
│ Routes → Controllers → Models        │
│            │                         │
│            ▼                         │
│       Authentication                 │
└──────────────────┬───────────────────┘
                   │
          ┌────────┴────────┐
          ▼                 ▼
   ┌─────────────┐   ┌──────────────┐
   │   MongoDB   │   │  Cloudinary  │
   │  Database   │   │ File Storage │
   └─────────────┘   └──────────────┘
```

### Frontend

The Flutter client is responsible for:

* User interface
* Navigation
* User interactions
* Form handling
* API communication
* Book browsing and management
* Authentication flow
* File selection and uploads

### Backend

The Express server is responsible for:

* REST API endpoints
* Authentication and authorization
* Request validation
* Business logic
* Database operations
* File/image management

### Database

MongoDB stores application data using **Mongoose** schemas and models.

### Cloud Storage

Cloudinary is used to manage uploaded images and digital files.

---

## 🧰 Tech Stack

### Frontend

| Technology        | Purpose                                |
| ----------------- | -------------------------------------- |
| Flutter           | Cross-platform application development |
| Dart              | Programming language                   |
| HTTP              | REST API communication                 |
| Google Fonts      | Application typography                 |
| File Picker       | File selection                         |
| Cloudinary Public | Cloud file/image management            |
| Dotted Border     | UI components                          |
| Flex Color Picker | Color selection                        |

### Backend

| Technology | Purpose             |
| ---------- | ------------------- |
| Node.js    | Backend runtime     |
| Express.js | REST API framework  |
| MongoDB    | Database            |
| Mongoose   | MongoDB ODM         |
| JWT        | Authentication      |
| bcryptjs   | Password hashing    |
| Nodemon    | Development tooling |

---

## 📂 Project Structure

```text
Re-Hon/
│
├── client/                         # Flutter Application
│   │
│   ├── lib/                        # Dart source code
│   │
│   ├── assets/                     # Images and application assets
│   │
│   └── pubspec.yaml                # Flutter dependencies
│
├── server/                         # Node.js Backend
│   │
│   ├── controllers/                # Request handlers
│   ├── models/                     # Mongoose models
│   ├── routes/                     # API routes
│   ├── middlewares/                # Custom middleware
│   ├── app.js                      # Express configuration
│   └── package.json                # Backend dependencies
│
└── README.md
```

---

# 🔐 Authentication

Re-Hon uses **JWT-based authentication** to protect user accounts and authenticated operations.

### Authentication Flow

```text
User
 │
 ▼
Login / Register
 │
 ▼
Express API
 │
 ▼
Validate Credentials
 │
 ▼
bcrypt Password Verification
 │
 ▼
Generate JWT
 │
 ▼
Return Token
 │
 ▼
Flutter Client
 │
 ▼
Authenticated Requests
```

Passwords are protected using `bcryptjs`, while JSON Web Tokens are used to authenticate requests.

---

# 🔄 API Architecture

The Flutter application communicates with the backend through **RESTful APIs**.

```text
Flutter Client
      │
      │ HTTP Request
      ▼
Express Router
      │
      ▼
Controller
      │
      ▼
Mongoose Model
      │
      ▼
MongoDB
      │
      ▼
Response
      │
      ▼
Flutter Client
```

This separation allows the frontend and backend to remain independent and makes the system easier to maintain and extend.

---

# ☁️ Cloud File Management

Re-Hon uses **Cloudinary** for managing uploaded images and files.

The general workflow is:

```text
Flutter
   │
   ▼
Select File
   │
   ▼
Upload to Cloud Storage
   │
   ▼
Receive File URL
   │
   ▼
Send URL to Backend
   │
   ▼
Store Reference in MongoDB
```

This keeps large files outside the main database while allowing the application to store and retrieve their references efficiently.

---

# 🚀 Getting Started

## Prerequisites

Make sure you have the following installed:

* Flutter SDK
* Dart SDK
* Node.js
* npm
* MongoDB or MongoDB Atlas
* Git

---

## 1. Clone the Repository

```bash
git clone https://github.com/Rady10/Re-Hon.git

cd Re-Hon
```

---

# ⚙️ Backend Setup

Navigate to the server:

```bash
cd server
```

Install dependencies:

```bash
npm install
```

Create a `.env` file inside the `server` directory:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

Start the backend:

```bash
npm start
```

The backend will run on the configured port.

---

# 📱 Frontend Setup

Open another terminal and navigate to the Flutter client:

```bash
cd client
```

Install Flutter dependencies:

```bash
flutter pub get
```

Run the application:

```bash
flutter run
```

---

# 🧪 Development Workflow

A typical development workflow looks like:

```text
Create / Update Feature
        │
        ▼
Flutter UI
        │
        ▼
API Request
        │
        ▼
Express Route
        │
        ▼
Controller
        │
        ▼
MongoDB / Cloudinary
        │
        ▼
API Response
        │
        ▼
Update Flutter UI
```

---

# 🎯 Project Goals

The main goals of Re-Hon are to:

* Provide a simple digital marketplace for e-books.
* Create a smooth cross-platform reading experience.
* Practice full-stack application development.
* Implement secure user authentication.
* Build a scalable REST API.
* Integrate cloud-based file storage.
* Develop a responsive and user-friendly Flutter interface.

---

# 🔮 Future Improvements

Potential improvements include:

* 💳 Online payment integration
* ⭐ Book ratings and reviews
* ❤️ Favorites and wishlists
* 🔔 Push notifications
* 📊 Seller analytics dashboard
* 📚 Improved reading experience
* 🔎 Advanced search and filtering
* 💬 User-to-user communication
* 📱 Offline reading
* 🧪 Expanded automated testing
* 🚀 CI/CD pipeline

---

# 📸 Screenshots

Add application screenshots here to showcase the UI:

```text
screenshots/
├── splash.png
├── login.png
├── home.png
├── book-details.png
├── marketplace.png
└── profile.png
```

Example:

```markdown
![Home Screen](screenshots/home.png)
```

---

# 🧠 What This Project Demonstrates

Re-Hon demonstrates practical experience in:

* Cross-platform mobile development
* Flutter and Dart
* REST API integration
* Node.js backend development
* Express.js
* MongoDB and Mongoose
* JWT authentication
* Password hashing
* Cloudinary integration
* Client-server architecture
* Full-stack application development
* Responsive UI development

---

# 👨‍💻 Developer

**Ahmed Rady**

Flutter Developer

* GitHub: https://github.com/Rady10
* LinkedIn: https://www.linkedin.com/in/rady10

---

# ⭐ Repository

If you find this project useful or interesting, consider giving it a ⭐ on GitHub.

**Repository:**
https://github.com/Rady10/Re-Hon

---

## 📄 License

This project is available for educational and portfolio purposes.
