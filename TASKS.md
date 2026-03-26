# PulseChat – Task Management

> ⚡ **PulseChat – Instant. Real-Time. Connected.**
>
> A modern real-time messaging platform built with Next.js, Socket.IO, and Prisma ORM.
>
> **Author:** Cris John Labiaga · Full-Stack Developer  
> **Repository:** [github.com/Kurisujon/PulseChat](https://github.com/Kurisujon/PulseChat)

---

## 📋 Project Overview

PulseChat allows users to communicate instantly through private or group chats while maintaining message history and online user presence.

**Goal:** Demonstrate modern full-stack web development, real-time communication, and database-driven applications.

---

## ✅ Feature Tasks

- [ ] **User Authentication** – Register, login, logout with secure sessions via NextAuth.js or JWT
- [ ] **Real-Time Messaging** – Instant message delivery without page refresh using Socket.IO
- [ ] **Private Chat** – One-to-one conversations with history and timestamps
- [ ] **Group Chat Rooms** – Multiple users in a room with real-time group messaging
- [ ] **Online Status** – Display which users are currently online
- [ ] **Message History** – Persist all messages in the database via Prisma
- [ ] **Responsive UI** – Mobile-friendly interface using Tailwind CSS

---

## 🛠️ Technology Stack

| Layer          | Technology                        |
| -------------- | --------------------------------- |
| Frontend       | Next.js, React, Tailwind CSS      |
| Backend        | Next.js API Routes, Socket.IO     |
| Authentication | NextAuth.js or JWT                |
| Database       | PostgreSQL or MySQL               |
| ORM            | Prisma                            |

---

## 🏗️ System Architecture

```
User Browser
     ⬇
Next.js Frontend (UI)
     ⬇
Next.js API Routes
     ⬇
Socket.IO Real-Time Server
     ⬇
Database (PostgreSQL / MySQL)
```

**Message Flow:**

1. User types a message
2. Frontend sends the message to Socket.IO
3. Socket.IO broadcasts the message to other users
4. Message is stored in the database via Prisma
5. All users receive the message instantly

---

## ⚙️ Installation Tasks

- [x] **Clone the Repository**
  ```bash
  git clone https://github.com/Kurisujon/PulseChat.git
  cd PulseChat
  ```

- [x] **Install Dependencies**
  ```bash
  pnpm install
  ```

- [ ] **Configure Environment Variables** – Create `.env.local` in the root directory
  ```env
  DATABASE_URL=your_database_url
  NEXTAUTH_SECRET=your_secret_key
  NEXTAUTH_URL=http://localhost:3000
  ```

- [ ] **Setup Database**
  ```bash
  npx prisma migrate dev
  ```

- [ ] **Run the Development Server**
  ```bash
  pnpm dev
  ```
  Visit: [http://localhost:3000](http://localhost:3000)

---

## 📁 Project Structure

```
pulsechat/
├── app/
│   ├── _components/
│   │   ├── ChatWindow.tsx
│   │   ├── MessageList.tsx
│   │   └── Sidebar.tsx
│   ├── _lib/
│   │   ├── prisma.ts
│   │   └── socket.ts
│   ├── layout.tsx
│   └── page.tsx
├── prisma/
│   └── schema.prisma
├── public/
├── .env.local
├── next.config.ts
├── package.json
├── tsconfig.json
└── README.md
```

---

## 🔌 API Endpoints

### Authentication

| Method | Endpoint              | Description           |
| ------ | --------------------- | --------------------- |
| POST   | `/api/auth/register`  | Register a new user   |
| POST   | `/api/auth/login`     | Login an existing user|

### Messages

| Method | Endpoint       | Description          |
| ------ | -------------- | -------------------- |
| GET    | `/api/messages`| Fetch message history|
| POST   | `/api/messages`| Send a new message   |

### Users

| Method | Endpoint    | Description   |
| ------ | ----------- | ------------- |
| GET    | `/api/users`| List all users|

---

## 🤖 AI Features

### 1. Smart Reply Suggestions

Provides quick, rule-based reply suggestions based on incoming messages.

> 💬 **Example:**
> 
> User: "I can't attend the meeting"  
> Suggestions: `["No worries", "Can we reschedule?", "Thanks for letting me know!"]`

### 2. Sentiment Detection with Emojis

Basic keyword-based sentiment detection for visual feedback.

- "I love this project!" → 😊
- "I'm frustrated with this bug" → 😡

### ❌ Deferred Features

- Real-time multilingual translation
- AI chatbot integration

---

## 🚀 Future Improvements

- [ ] AI chatbot assistant
- [ ] Real-time translation
- [ ] File & image sharing
- [ ] Voice & video calls
- [ ] Push notifications
- [ ] End-to-end encryption
- [ ] Mobile application (React Native)

---

## 📝 Development Progress

Track your progress by checking off tasks as you complete them. Update this file regularly to maintain visibility on project status.
