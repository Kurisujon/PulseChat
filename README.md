# PulseChat – Real-Time Chat Application

> **PulseChat – Instant. Real-Time. Connected.**

PulseChat is a modern real-time messaging platform built using Next.js, Socket.IO, and Prisma ORM. It allows users to communicate instantly through private or group chats while maintaining message history and online user presence.

**Goal:** Demonstrate modern full-stack web development, real-time communication, and database-driven applications.

---

## Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Medium-Complexity AI Features](#medium-complexity-ai-features)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## Features

- **User Authentication** – Register, login, logout with secure sessions. Session management with NextAuth.js or JWT.
- **Real-Time Messaging** – Instant message delivery without page refresh. Live updates with Socket.IO.
- **Private Chat** – One-to-one conversations with chat history and timestamps.
- **Group Chat Rooms** – Multiple users in a room with real-time group messaging.
- **Online Status** – See which users are online.
- **Message History** – All messages stored in the database for persistence.
- **Responsive UI** – Clean, mobile-friendly interface using Tailwind CSS.

---

## Technology Stack

| Layer          | Technology                        |
| -------------- | --------------------------------- |
| Frontend       | Next.js, React, Tailwind CSS      |
| Backend        | Next.js API Routes, Socket.IO     |
| Authentication | NextAuth.js or JWT                |
| Database       | PostgreSQL or MySQL               |
| ORM            | Prisma                            |

---

## System Architecture

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

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Kurisujon/PulseChat.git
cd PulseChat
```

### 2. Install Dependencies

```bash
pnpm install
```

### 3. Configure Environment Variables

Create a `.env.local` file in the root directory:

```env
DATABASE_URL=your_database_url
NEXTAUTH_SECRET=your_secret_key
NEXTAUTH_URL=http://localhost:3000
```

### 4. Setup Database

```bash
npx prisma migrate dev
```

### 5. Run the Development Server

```bash
pnpm dev
```

Visit: [http://localhost:3000](http://localhost:3000)

---

## Project Structure

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

## API Endpoints

### Authentication

| Method | Endpoint              |
| ------ | --------------------- |
| POST   | `/api/auth/register`  |
| POST   | `/api/auth/login`     |

### Messages

| Method | Endpoint       |
| ------ | -------------- |
| GET    | `/api/messages` |
| POST   | `/api/messages` |

### Users

| Method | Endpoint    |
| ------ | ----------- |
| GET    | `/api/users` |

---

## Medium-Complexity AI Features

PulseChat focuses on medium-complexity AI features to enhance user experience without overcomplicating development.

### 1. Smart Reply Suggestions

Provides quick, rule-based reply suggestions.

**Example:**
> User: "I can't attend the meeting"
> Suggestions: `["No worries", "Can we reschedule?", "Thanks for letting me know!"]`

### 2. Sentiment Detection with Emojis

Basic keyword-based sentiment detection for visual feedback.

**Examples:**
- "I love this project!" → 😊
- "I'm frustrated with this bug" → 😡

### Removed High-Complexity Features

For simplicity and faster development, these features are deferred:

- ❌ Real-time multilingual translation
- ❌ AI chatbot integration

---

## Future Improvements

- AI chatbot assistant
- Real-time translation
- File & image sharing
- Voice & video calls
- Push notifications
- End-to-end encryption
- Mobile application (React Native)

---

## Author

**Cris John Labiaga**
Full-Stack Developer
