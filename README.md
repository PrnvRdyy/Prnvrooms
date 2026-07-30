# 🎥 PrnvRooms — Real-Time Communication & Collaboration Platform

> A production-deployed video conferencing & collaboration platform inspired by Zoom, Google Meet & Microsoft Teams. Built as a full-stack portfolio project.

🔗 **Live Demo:** [YOUR_VERCEL_URL](https://YOUR_VERCEL_URL)  
📦 **Backend API:** [prnvrooms.up.railway.app](https://prnvrooms.up.railway.app/api/health)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔐 **Auth** | JWT Register / Login with access + refresh tokens |
| 📅 **Meetings** | Create, join, leave & end meetings with unique room codes |
| 🎥 **Video Calling** | Multi-user P2P video via WebRTC |
| 💬 **Real-Time Chat** | In-meeting chat with emoji & typing indicators |
| 🖥️ **Screen Sharing** | Share your screen with all participants |
| 🎨 **Whiteboard** | Collaborative live-sync canvas drawing |
| 📁 **File Sharing** | Upload, preview & download files in-meeting |
| 🔔 **Notifications** | Real-time event notifications via Socket.io |

---

## 🛠 Tech Stack

![React](https://img.shields.io/badge/React_18-61DAFB?style=flat&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat&logo=socket.io&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat&logo=webrtc&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB_Atlas-47A248?style=flat&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat&logo=railway&logoColor=white)

---

## 🏗 Architecture

```
┌──────────────────────────────────────────┐
│              CLIENT (Vercel)             │
│   React 18 + Vite + React Router v6     │
└──────────┬───────────────────┬──────────┘
           │ REST API          │ WebSocket
           ▼                   ▼
┌──────────────────────────────────────────┐
│             SERVER (Railway)             │
│   Node.js + Express + Socket.io          │
│   WebRTC Signaling Server                │
└──────────────────────┬───────────────────┘
                       │
                       ▼
              ┌─────────────────┐
              │  MongoDB Atlas  │
              └─────────────────┘
```

---

## 🚀 Getting Started Locally

### Prerequisites
- Node.js 18+
- MongoDB Atlas account

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/PrnvRooms.git
cd PrnvRooms
```

### 2. Setup the Server
```bash
cd server
npm install
cp .env.example .env   # fill in your values
npm run dev
```

### 3. Setup the Client
```bash
cd client
npm install
cp .env.example .env
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 🔧 Environment Variables

### Server (`server/.env.example`)
```env
MONGO_URI=your_mongodb_atlas_uri
PORT=5000
NODE_ENV=development
JWT_SECRET=your_jwt_secret
JWT_REFRESH_SECRET=your_refresh_secret
JWT_EXPIRES_IN=15m
JWT_REFRESH_EXPIRES_IN=7d
CLIENT_URL=http://localhost:5173
```

### Client (`client/.env.example`)
```env
VITE_API_URL=http://localhost:5000/api
VITE_SOCKET_URL=http://localhost:5000
```

---

## 📂 Project Structure

```
PrnvRooms/
├── client/                  # React + Vite SPA
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Route-level pages
│   │   ├── services/        # API & socket layers
│   │   └── hooks/           # Custom React hooks
│   └── vercel.json
│
└── server/                  # Node.js + Express API
    ├── src/
    │   ├── routes/          # Express routes
    │   ├── controllers/     # Handler logic
    │   ├── middleware/      # Auth, error handling
    │   ├── models/          # Mongoose schemas
    │   └── sockets/         # Socket.io handlers
    └── railway.json
```

---

## 🌐 Deployment

| Service | Platform | URL |
|---|---|---|
| Frontend | Vercel | `YOUR_VERCEL_URL` |
| Backend | Railway | `https://prnvrooms.up.railway.app` |
| Database | MongoDB Atlas | Cloud-hosted |

---

## 📄 License

MIT — feel free to fork and build on top of this!

---

<p align="center">Built with ❤️ by Pranav</p>
