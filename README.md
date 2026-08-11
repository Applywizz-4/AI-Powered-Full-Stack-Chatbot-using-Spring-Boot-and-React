# AI-Powered-Full-Stack-Chatbot-using-Spring-Boot-and-React

A full-stack AI-powered conversational application built with Java Spring Boot, React.js, Spring AI, and Groq LLaMA-3.3-70B Versatile. The application provides real-time, context-aware conversations through a REST-based architecture.

## Overview

This project demonstrates the integration of Large Language Models with a modern Java full-stack application.

The React frontend provides the chat interface, Spring Boot manages the REST API and backend processing, Spring AI integrates the AI service, and Groq LLaMA processes natural-language queries and generates intelligent responses.

## Features

- Real-time AI-powered conversations
- Groq LLaMA-3.3-70B Versatile integration
- Spring AI integration
- Spring Boot REST API
- Responsive React.js interface
- Axios-based API communication
- CORS-enabled frontend and backend communication
- Context-aware AI responses
- Modular and scalable architecture
- Cloud-ready deployment

## Technology Stack

| Layer | Technology |
| --- | --- |
| Backend | Java 21 |
| Backend Framework | Spring Boot 3.3+ |
| AI Integration | Spring AI |
| Frontend | React.js |
| HTTP Client | Axios |
| AI Provider | Groq Cloud |
| AI Model | LLaMA-3.3-70B Versatile |
| Build Tool | Maven 3.9+ |
| Frontend Runtime | Node.js |
| API | REST |
| API Testing | Postman / Thunder Client |
| Version Control | Git / GitHub |

## Architecture

The application uses a three-layer architecture:

1. React.js frontend
2. Spring Boot backend
3. Groq AI service

```text
User
  |
  v
React.js Frontend
  |
  | REST API Request
  v
Spring Boot Backend
  |
  v
Spring AI
  |
  | API Request
  v
Groq Cloud API
  |
  v
LLaMA-3.3-70B Versatile
  |
  | AI Response
  v
Spring Boot Backend
  |
  v
React.js Frontend
```

## Project Structure

```text
AI-Powered-Spring-Boot-React-Chatbot/
├── spring-boot-ai-chatbot/
│   └── Spring Boot Backend
├── chatbot-ui/
│   └── React Frontend
└── README.md
```

## Prerequisites

Install the following before running the application:

- Java 21
- Maven 3.9+
- Node.js
- npm
- Git
- Groq API key

Verify the installations:

```bash
java -version
mvn -version
node -v
npm -v
git --version
```

## How to Run Locally

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd <project-directory>
```

### Step 2: Configure the Groq API

Open the Spring Boot configuration file:

```text
spring-boot-ai-chatbot/src/main/resources/application.yml
```

Add the Groq configuration:

```yaml
spring:
  ai:
    openai:
      base-url: "https://api.groq.com/openai/v1"
      api-key: "YOUR_GROQ_API_KEY"
      chat:
        options:
          model: "llama-3.3-70b-versatile"
          temperature: 0.7
```

Replace `YOUR_GROQ_API_KEY` with your actual Groq API key.

Do not commit the API key to GitHub.

### Step 3: Start the Backend

Open a terminal and run:

```bash
cd spring-boot-ai-chatbot
mvn clean install
mvn spring-boot:run
```

The Spring Boot backend will run at:

```text
http://localhost:8080
```

The chatbot API endpoint is:

```text
POST http://localhost:8080/api/chat
```

Keep this terminal running.

### Step 4: Start the Frontend

Open a second terminal and run:

```bash
cd chatbot-ui
npm install
npm start
```

The React frontend will run at:

```text
http://localhost:3000
```

### Step 5: Open the Application

Open the following URL in your browser:

```text
http://localhost:3000
```

The chatbot interface will be available for interaction.

## Application Workflow

```text
User
  |
  v
React.js Chat Interface
  |
  v
POST /api/chat
  |
  v
Spring Boot Backend
  |
  v
Spring AI
  |
  v
Groq API
  |
  v
LLaMA-3.3-70B Versatile
  |
  v
AI Generated Response
  |
  v
React.js Chat Interface
```

## Local Development Ports

| Component | URL | Port |
| --- | --- | ---: |
| React Frontend | http://localhost:3000 | 3000 |
| Spring Boot Backend | http://localhost:8080 | 8080 |
| Chat API | http://localhost:8080/api/chat | 8080 |

## API Testing

The REST API can be tested using Postman or Thunder Client.

### Chat Endpoint

```text
POST http://localhost:8080/api/chat
```

The endpoint receives user messages, sends them to the Groq LLaMA model through Spring AI, and returns the generated response.

## Application Output

The application provides a responsive conversational interface with:

- Chatbot header
- User messages
- AI responses
- Chat input field
- Send functionality
- Real-time response display

Example:

```text
User:
Tell me about Java

AI:
Java is a high-level, object-oriented programming language...
```

## Backend Verification

After starting the backend, the Spring Boot console should display startup information similar to:

```text
Tomcat started on port 8080
Started SpringBootChatBotApplication
```

When a user sends a message, the backend processes the request and communicates with Groq:

```text
POST request received on /api/chat
Calling Groq API for model: llama-3.3-70b-versatile
Response successfully returned to client
```

## Performance Targets

| Metric | Target |
| --- | ---: |
| Reduction in manual response time | 95% |
| Backend availability | 99% uptime |
| Target response time | Less than 1 second |
| Scalability target | 10,000+ concurrent users |
| User satisfaction | Positive post-deployment feedback |

These are the success targets defined in the project documentation.

## Scalability

The architecture is designed to support:

- Decoupled frontend and backend
- Horizontal scaling
- REST-based communication
- Modular backend development
- Extensible AI service integration
- Cloud deployment
- Independent frontend and backend deployment

## Deployment

The documented architecture supports the following deployment options.

### Frontend

- Vercel
- Netlify

### Backend

- Render
- AWS EC2
- Railway

### AI Service

The Groq API is cloud-hosted and accessed securely over HTTPS.





