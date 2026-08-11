# AI-Powered Spring Boot and React Chatbot

A full-stack AI chatbot built with Java Spring Boot, React.js, Spring AI, and Groq LLaMA-3.3-70B Versatile. The application provides real-time, context-aware conversations through a REST-based architecture.

## Overview

This project demonstrates the integration of Large Language Models with a modern Java full-stack application.

The React frontend provides the chat interface, Spring Boot manages REST API communication, and Groq LLaMA processes natural-language queries and generates AI responses.

## Features

- Real-time AI-powered conversations
- Groq LLaMA-3.3-70B Versatile integration
- Spring AI integration
- Spring Boot REST API
- Responsive React interface
- Axios-based API communication
- CORS-enabled frontend and backend communication
- Modular and scalable architecture
- Cloud-ready deployment
- Context-aware AI responses

## Technology Stack

| Category | Technology |
|---|---|
| Backend | Java 21 |
| Framework | Spring Boot 3.3+ |
| AI Integration | Spring AI |
| Frontend | React.js |
| HTTP Client | Axios |
| AI Provider | Groq Cloud |
| AI Model | LLaMA-3.3-70B Versatile |
| Build Tool | Maven 3.9+ |
| Frontend Runtime | Node.js |
| API | REST |
| Testing | Postman / Thunder Client |
| Version Control | Git / GitHub |

## Architecture

```text
React Frontend
      |
      | REST API
      v
Spring Boot Backend
      |
      v
Spring AI
      |
      v
Groq Cloud API
      |
      v
LLaMA-3.3-70B Versatile
      |
      v
AI Response
      |
      v
React Chat Interface
Project Structure
AI-Powered-Spring-Boot-React-Chatbot/
|
|-- spring-boot-ai-chatbot/
|   |-- Spring Boot Backend
|
|-- chatbot-ui/
|   |-- React Frontend
|
|-- README.md
Prerequisites

Install the following before running the project:

Java 21
Maven 3.9+
Node.js
npm
Git
Groq API Key

Verify the installation:

java -version
mvn -version
node -v
npm -v
git --version
How to Run Locally
1. Clone the Repository
git clone <repository-url>
cd <project-directory>
2. Configure Groq API

Open:

spring-boot-ai-chatbot/src/main/resources/application.yml

Configure:

spring:
  ai:
    openai:
      base-url: "https://api.groq.com/openai/v1"
      api-key: "YOUR_GROQ_API_KEY"
      chat:
        options:
          model: "llama-3.3-70b-versatile"
          temperature: 0.7

Replace YOUR_GROQ_API_KEY with your actual Groq API key.

Do not commit the API key to GitHub.

3. Start the Backend

Open Terminal 1:

cd spring-boot-ai-chatbot
mvn clean install
mvn spring-boot:run

Backend:

http://localhost:8080

Chat API:

POST http://localhost:8080/api/chat
4. Start the Frontend

Open Terminal 2:

cd chatbot-ui
npm install
npm start

Frontend:

http://localhost:3000
5. Open the Application

Open the following URL in your browser:

http://localhost:3000

Enter a message and the request will be processed through:

React
  |
  v
Spring Boot
  |
  v
Spring AI
  |
  v
Groq LLaMA
  |
  v
AI Response
  |
  v
React
Local Ports
Component	Port
React Frontend	3000
Spring Boot Backend	8080
API Testing

The REST API can be tested using Postman or Thunder Client.

Main endpoint:

POST http://localhost:8080/api/chat
Application Workflow
User enters a message in the React interface.
React sends the request to Spring Boot.
Spring Boot processes the request through /api/chat.
Spring AI communicates with Groq.
LLaMA-3.3-70B generates the response.
Spring Boot returns the response to React.
React displays the AI response.
Deployment

The architecture supports cloud deployment.

Frontend
Vercel
Netlify
Backend
Render
AWS EC2
Railway
Future Enhancements
Voice-based communication
Persistent conversation memory
Multilingual support
Sentiment analysis
Adaptive learning
CRM integrations
HR system integrations
Analytics dashboard integrations
Enterprise cloud deployment
Project Highlights
Full-stack Java and React application
Generative AI integration
Spring AI and Groq integration
Real-time conversational interface
RESTful architecture
Modular and scalable design
Cloud-ready architecture
Enterprise-oriented AI application
