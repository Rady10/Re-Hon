# 📚 EBook App - Digital Library

A full-stack, cross-platform ebook application built with **Flutter** and **Node.js (Express)**. This project provides a seamless digital reading experience, allowing users to browse, search, and read their favorite books on any device.

---

## 🚀 Features

- **Cross-Platform Support**: Built with Flutter to run on Android, iOS, Web, and Desktop.
- **User Authentication**: Secure login and registration using **JWT** and **bcrypt**.
- **Book Management**: Browse a wide collection of ebooks with detailed information.
- **Cloud Integration**: Image and file management powered by **Cloudinary**.
- **Modern UI**: Clean and intuitive interface with custom splash screens and Google Fonts.
- **Robust Backend**: High-performance REST API built with Express and MongoDB.

---

## 🛠️ Tech Stack

### Frontend (Client)
- **Framework**: [Flutter](https://flutter.dev/)
- **UI Components**: `google_fonts`, `dotted_border`, `flex_color_picker`
- **File Handling**: `file_picker`
- **Cloud Services**: `cloudinary_public`
- **Networking**: `http`

### Backend (Server)
- **Framework**: [Express.js](https://expressjs.com/) (Node.js)
- **Database**: [MongoDB](https://www.mongodb.com/) with [Mongoose](https://mongoosejs.com/)
- **Authentication**: [JSON Web Token (JWT)](https://jwt.io/) & [bcryptjs](https://www.npmjs.com/package/bcryptjs)
- **Development Tools**: `nodemon`

---

## 📂 Project Structure

```text
EBook-App/
├── client/                # Flutter Application
│   ├── lib/               # Dart source code
│   ├── assets/            # Images and fonts
│   └── pubspec.yaml       # Flutter dependencies
└── server/                # Node.js Backend
    ├── controllers/       # Request handlers
    ├── models/            # Mongoose schemas
    ├── routes/            # API endpoints
    ├── middlewares/       # Custom middlewares
    ├── app.js             # Express app configuration
    └── package.json       # Node.js dependencies
```

---

## ⚙️ Getting Started

### Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install)
- [Node.js](https://nodejs.org/) (v14+)
- [MongoDB](https://www.mongodb.com/try/download/community) (Local or Atlas)

### Backend Setup
1. Navigate to the server directory:
   ```bash
   cd server
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables (create a `.env` file):
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   ```
4. Start the server:
   ```bash
   npm start
   ```

### Frontend Setup
1. Navigate to the client directory:
   ```bash
   cd client
   ```
2. Install Flutter dependencies:
   ```bash
   flutter pub get
   ```
3. Run the application:
   ```bash
   flutter run
   ```
