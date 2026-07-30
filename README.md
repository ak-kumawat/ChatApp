# TalkFlow - Full-Stack Realtime Chat Application

A full-stack, real-time messaging application built to enable seamless 1-on-1 communication. Engineered with a focus on low latency, secure authentication, and a responsive, dynamic user interface.

## 🚀 Features

- **Real-time Messaging:** Instant message delivery powered by WebSockets (`Socket.io`).
- **Secure Authentication:** Stateful user authentication and authorization using JSON Web Tokens (JWT) stored in HttpOnly cookies.
- **Live User Status:** In-memory socket mapping to broadcast and display online/offline status in real-time.
- **Media Sharing:** Integration with Cloudinary API for secure image and profile picture uploads.
- **Global State Management:** Efficient client-side state handling utilizing `Zustand`.
- **Dynamic UI Themes:** Modern, responsive design using `Tailwind CSS` and `DaisyUI` with dynamic client-side theme selection.

## 💻 Tech Stack

- **Frontend:** React.js, Vite, Tailwind CSS, DaisyUI, Zustand, Socket.io-client
- **Backend:** Node.js, Express.js, Socket.io
- **Database:** MongoDB, Mongoose
- **Image Hosting:** Cloudinary

## 🛠️ Local Development Setup

### 1. Prerequisites
- Node.js (v18 or higher)
- A MongoDB cluster or local instance
- A free Cloudinary account (for image uploads)

### 2. Install Dependencies
Run the build script from the root directory to automatically install dependencies for both the frontend and backend:
```bash
npm run build
```

### 3. Environment Configuration
Create a `.env` file inside the `backend` directory and add the following variables:

```env
MONGODB_URI=your_mongodb_connection_string
PORT=5001
JWT_SECRET=your_random_secret_string

# Cloudinary Credentials (Optional for text-only chat)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

NODE_ENV=development
```

### 4. Start the Application
To run the backend server and frontend development server simultaneously:

**Terminal 1 (Backend):**
```bash
npm start
```

**Terminal 2 (Frontend):**
```bash
cd frontend
npm run dev
```
The application will be accessible at `http://localhost:5173`.
