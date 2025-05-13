# Real-Time Chat Application

A simple real-time chat application built using **Spring Boot**, **WebSockets**, **SockJS**, **STOMP**, and **Bootstrap**. The app allows users to communicate in real-time by sending messages that are instantly visible to all connected users.

---

## Features

- Real-time communication using WebSockets.
- STOMP protocol for message exchange.
- User-friendly UI built with Bootstrap.
- Support for multiple users.
- Auto-scrolling chat window.

---

## Technologies Used

### Backend:
- **Spring Boot**: For creating the backend REST and WebSocket server.
- **Spring WebSocket**: To enable real-time WebSocket communication.

### Frontend:
- **HTML5**: Structure of the chat application.
- **CSS (Bootstrap)**: Styling and responsive layout.
- **SockJS**: Fallback for WebSocket support.
- **STOMP.js**: Protocol to handle real-time message delivery.

---

## Project Structure

### `ChatApplication`
The main class that starts the Spring Boot application.

### `WebSocketConfig`
Configures the WebSocket endpoints and message brokers.  
- Endpoint: `/chat`  
- Message Broker: `/topic`  
- Application Destination Prefix: `/app`

### `ChatController`
Handles incoming and outgoing chat messages.  
- **Endpoints**:
  - `/app/sendMessage`: Maps incoming messages.
  - `/topic/messages`: Broadcasts messages to all subscribers.

### `ChatMessage`
The model class representing a chat message with:
- `id` (Long): Unique identifier.
- `sender` (String): Name of the sender.
- `content` (String): Message content.
