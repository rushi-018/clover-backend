# Rushiraj Backend - Messaging & Video Conferencing

Backend API for Rushiraj messaging and video conferencing application built with Node.js, Express, Socket.IO, and WebRTC.

## Features

- 🔐 **User Authentication** - JWT-based authentication system
- 💬 **Real-time Messaging** - Socket.IO powered chat
- 📹 **Video Conferencing** - WebRTC with Mediasoup
- 🎥 **Group Calls** - Multi-user video conferences
- 📧 **Email Integration** - Gmail SMTP for notifications
- 🗄️ **MongoDB Database** - User data and message storage
- 🔒 **Security** - Password hashing with Argon2

## Tech Stack

- **Runtime**: Node.js 18+
- **Framework**: Express.js
- **Database**: MongoDB Atlas
- **Real-time**: Socket.IO
- **WebRTC**: Mediasoup
- **Authentication**: JWT + Passport
- **Email**: Nodemailer
- **Security**: Argon2 password hashing

## Environment Variables

Create a `.env` file with the following variables:

```env
PORT=4000
PUBLIC_IP_ADDRESS=0.0.0.0
MAPPED_IP=false
AUTH_SECRET=your-jwt-secret-key

# Root User
ROOT_USER_USERNAME=admin
ROOT_USER_EMAIL=your-email@gmail.com
ROOT_USER_PASSWORD=your-admin-password
ROOT_USER_FIRST_NAME=Admin
ROOT_USER_LAST_NAME=User

# MongoDB
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/database?retryWrites=true&w=majority
MONGO_DATABASE=rushiraj

# Email (Gmail)
MAILER_ENABLED=true
MAILER_FROM="Rushiraj <your-email@gmail.com>"
MAILER_USERNAME=your-email@gmail.com
MAILER_PASSWORD=your-app-password
MAILER_SERVICE=gmail
SUPPORT_EMAIL_ADDRESS=your-email@gmail.com
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/rushi-018/clover-backend.git
cd clover-backend
```

2. Install dependencies:

```bash
npm install
```

3. Create `.env` file with your configuration

4. Start the server:

```bash
npm start
```

## API Endpoints

- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `GET /api/users` - Get users list
- `POST /api/rooms/create` - Create chat room
- `GET /api/rooms` - Get user's rooms
- WebSocket endpoints for real-time messaging

## Deployment

### Railway Deployment

1. Push code to GitHub
2. Connect to [Railway](https://railway.app)
3. Add environment variables
4. Deploy automatically

### Environment Variables for Production

Set these in your hosting platform:

- All variables from `.env.example`
- Update `MONGO_URI` with production database
- Use strong `AUTH_SECRET` (32+ characters)
- Configure email settings for notifications

## License

This project is licensed under the CodeCanyon license.

---

**Created by Rushiraj** - Full-stack messaging and video conferencing solution
