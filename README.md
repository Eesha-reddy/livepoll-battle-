Live Poll Battle
A real-time polling application that enables users to create or join rooms, participate in polls, and view live results instantly. The application utilizes React for the frontend and Node.js with WebSockets on the backend to facilitate real-time interactions.

Setup

Frontend:

Navigate to the client/ directory.

Execute npm install to install the necessary dependencies.

Run npm start to launch the React application locally.

Backend:

Navigate to the server/ directory.

Execute npm install to install the necessary dependencies.

Run npm start to launch the Node.js server locally.

Features

Frontend (ReactJS):

Allow users to input a unique name (no password required) and either:

Create a new poll room, or

Join an existing poll room using a room code.

Display a poll question with two options (e.g., "Cats or Dogs").

Enable users to vote for one option.

Provide real-time vote updates as other participants vote.

Indicate when a user has already voted and restrict further voting.

Implement a countdown timer, disabling voting after 60 seconds.

Utilize local storage to retain the user's vote across page refreshes.

Backend (NodeJS + WebSocket):

Manage the creation and storage of poll rooms.

Receive and broadcast votes to all connected clients within a room.

Maintain the poll state in memory (no database required).

Support multiple concurrent rooms with different users.

Vote State Sharing and Room Management

When a user creates a new room, a unique roomCode is generated and displayed. Other participants may join the same room by entering this code. Within the room, all users can vote on the poll question in real time. The vote state, which includes the count for each option, is synchronized across all users. The backend handles vote state management and a countdown timer using WebSockets. Once the first user joins, the countdown begins, and voting is disabled after 60 seconds. This architecture ensures real-time synchronization and transparency in poll results for all users within the same room.

Thank you.
