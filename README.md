# SleekChat Backend

A real-time chat application backend built with Node.js, Express, and Socket.IO. This server provides the foundation for a modern chat application with features like room-based messaging and user management.

## Features

- Real-time messaging using Socket.IO
- Room-based chat functionality
- User management (join, leave, disconnect)
- CORS enabled for cross-origin requests
- Automatic user status updates
- Admin notifications for user events

## Prerequisites

- Node.js (v12 or higher)
- npm (Node Package Manager)

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd SleekChat_Backend
```

2. Install dependencies:

```bash
npm install
```

## Available Scripts

- `npm start` - Runs the server in production mode
- `npm run dev` - Runs the server in development mode with nodemon for auto-reloading

## Environment Variables

The server uses the following environment variables:

- `PORT` - The port number the server will listen on (defaults to 5000)

## API Endpoints

The server provides WebSocket connections for real-time communication. Here are the main events:

### Socket Events

- `join` - Join a chat room

  - Parameters: `{ name, room }`
  - Callback: `(error) => void`

- `sendMessage` - Send a message to the current room

  - Parameters: `message`
  - Callback: `() => void`

- `disconnect` - Handle user disconnection

## Dependencies

- express: ^4.17.1
- socket.io: ^4.3.1
- cors: ^2.8.5
- nodemon: ^2.0.14 (dev dependency)

## Project Structure

```
SleekChat_Backend/
├── index.js          # Main server file
├── users.js          # User management utilities
├── router.js         # Express router configuration
├── package.json      # Project dependencies and scripts
└── Procfile         # Heroku deployment configuration
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.
