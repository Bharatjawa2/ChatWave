# ChatWave

A modern real-time chat application with channels, direct messages, file uploads, and user profiles. Built with React (frontend) and Node.js/Express/MongoDB (backend).

---

## Features
- User authentication (JWT, cookies)
- Create and join channels
- Direct messaging
- File uploads (images, files)
- User profile with avatar
- Real-time messaging (Socket.io)
- Responsive UI

---

## Folder Structure

```
ChatWave/
  backend/      # Node.js/Express/MongoDB API
  frontend/     # React client app
```

---

## Getting Started

### 1. Clone the repository
```bash
git clone <repo-url>
cd ChatWave
```

### 2. Backend Setup
```bash
cd backend
npm install
```

#### Create a `.env` file in `backend/` with:
```
PORT=4000
MONGO_URI=mongodb://localhost:27017/ChatWave
JWT_SECRET=your_jwt_secret
ORIGIN=http://localhost:5173
```

#### Start the backend server
```bash
npm start
```

### 3. Frontend Setup
```bash
cd ../frontend
npm install
npm run dev
```

The frontend will run on [http://localhost:5173](http://localhost:5173) by default.

---

## Usage
- Register and log in.
- Set up your profile and avatar.
- Create channels or start direct messages.
- Upload and download files in chat.

---

## Troubleshooting
- **File upload issues:** Ensure the `backend/upload/files/` and `backend/upload/profiles/` directories exist and are writable.
- **Channel not appearing after creation:** Make sure MongoDB is running and the backend is connected.
- **CORS errors:** Check the `ORIGIN` variable in your backend `.env` matches your frontend URL.
- **Long channel creation time:** Backend now uses optimized member validation for faster channel creation.

---

## License
MIT
