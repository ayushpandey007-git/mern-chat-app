# Real-Time MERN Chat Application

A full-stack real-time messaging application built with **MongoDB, Express.js, React, Node.js**, and **Socket.io**.

## Live Demo
- **Frontend (Vercel):** `<paste-your-vercel-url-here>`
- **Backend Health Check (Render):** `<paste-your-render-url-here>/ping`

## Key Features
- User registration and login with **bcrypt** password hashing
- Custom avatar selection powered by `@multiavatar/multiavatar`
- Real-time one-to-one messaging via **Socket.io** WebSockets
- Persistent chat history stored in **MongoDB** using Mongoose schemas
- Emoji picker support and responsive dark UI with `styled-components`

## Tech Stack
- **Frontend:** React 17, React Router v6, Axios, Socket.io Client, Styled Components, React Toastify
- **Backend:** Node.js, Express.js, Socket.io, Mongoose, Bcrypt, CORS, Dotenv
- **Database & Hosting:** MongoDB Atlas, Render (Backend), Vercel (Frontend)

## Local Setup

### 1. Backend (`server/`)
```bash
cd server
cp .env.example .env
# Update MONGO_URL in server/.env with your local MongoDB or MongoDB Atlas URI
npm install
npm run dev
```

### 2. Frontend (`public/`)
```bash
cd public
cp .env.example .env
npm install --legacy-peer-deps
npm start
```

## Cloud Deployment Summary
- **Database:** MongoDB Atlas (M0 Free Tier)
- **Backend (Render Web Service):** Root Directory `server`, Build `npm install`, Start `node index.js`, Env Vars `MONGO_URL` and `ORIGIN` (your Vercel URL)
- **Frontend (Vercel):** Root Directory `public`, Install `npm install --legacy-peer-deps`, Env Vars `REACT_APP_API_URL` (your Render URL) and `REACT_APP_LOCALHOST_KEY=chat-app-current-user`
