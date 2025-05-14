# Live Poll Battle

A real-time polling application that enables users to create or join rooms, participate in polls, and view live results instantly. The application utilizes **React** for the frontend and **Node.js with WebSockets** on the backend to facilitate real-time interactions.

---

## 🔧 Setup

### Frontend
1. Navigate to the `client/` directory.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the React app locally.

### Backend
1. Navigate to the `server/` directory.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the Node.js server locally.

---

## 🚀 Features

### Frontend (ReactJS)
- Allow users to enter a unique name (no password required) and either:
  - Create a new poll room, or
  - Join an existing poll room using a room code.
- Display a poll question with two options (e.g., "Cats or Dogs").
- Enable users to vote for one option.
- Provide real-time vote updates as users vote.
- Indicate that a user has already voted and prevent re-voting.
- Implement a countdown timer that disables voting after 60 seconds.
- Use local storage to persist the user's vote across page refreshes.

### Backend (NodeJS + WebSocket)
- Handle creation and storage of poll rooms.
- Accept and broadcast votes to all clients in the room.
- Keep poll state in memory (no database required).
- Support multiple rooms with different users.

---

## 🔄 Vote State Sharing and Room Management

When a user creates a new room, a unique `roomCode` is generated and displayed. Other users can join the same room by entering this code. Once in the room, all users can vote on the poll question in real time.

The vote state, which includes the count for each option, is synchronized across all connected users. The backend manages this vote state and the countdown timer using WebSockets. The timer begins once the first user joins the room, and voting is disabled after 60 seconds.

This architecture ensures that all participants in the same room are synchronized and can view live poll results as others vote.

---

Thank you.
