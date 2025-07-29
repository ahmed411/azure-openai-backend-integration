# azure-openai-backend-integration

## Overview

This project serves as the backend API for an Azure OpenAI Chatbot. It's responsible for handling chat requests and communicating with Azure OpenAI services to provide conversational AI capabilities.

## Features

Handles chat message requests.

Communicates with Azure OpenAI services.

Manages conversation history for contextual responses.

Provides a clear API endpoint for chat interactions.

## Setup

### Prerequisites
Node.js and npm installed.

An Azure account with access to Azure OpenAI services.

### Install Dependencies

```sh
npm install
```

### Environment Variables

Create a `.env` file in the `backend` folder:

```
PORT=3000
AZURE_OPENAI_API_KEY=your-key
AZURE_OPENAI_ENDPOINT=your-endpoint
AZURE_OPENAI_DEPLOYMENT_NAME=your-deployment
AZURE_OPENAI_API_VERSION=your-api-version
```

### Start the Server

```sh
npm start
```
or
```sh
node server.JS
```

---

## API Endpoints

### `POST /api/chat`

Send a chat message.

**Request Body:**
```json
{
  "message": "Hello",
  "conversationHistory": [
    { "role": "user", "content": "Hi" },
    { "role": "assistant", "content": "Hello! How can I help you?" }
  ]
}
```

**Response:**
```json
{
  "success": true,
  "message": "The assistant's reply",
  "usage": { ... }
}
```

---

## Notes

- Uses CORS for local development.
- Make sure your Azure OpenAI credentials are correct.

---

# License

MIT
