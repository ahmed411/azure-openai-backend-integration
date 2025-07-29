# azure-openai-backend-integration

## Overview

This is the backend API for the Azure OpenAI Chatbot project.  
It handles chat requests and communicates with Azure OpenAI.

---

## Setup

### 1. Install Dependencies

```sh
npm install
```

### 2. Environment Variables

Create a `.env` file in the `backend` folder:

```
PORT=5000
AZURE_OPENAI_API_KEY=your-key
AZURE_OPENAI_ENDPOINT=your-endpoint
AZURE_OPENAI_DEPLOYMENT_NAME=your-deployment
AZURE_OPENAI_API_VERSION=your-api-version
```

### 3. Start the Server

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
