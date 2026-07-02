# 🤖 JavaAI ChatBot

<p align="center">
  <img src="https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
    <img src="https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" />
      <img src="https://img.shields.io/badge/LangChain4j-0.27-1C3C3C?style=for-the-badge" />
        <img src="https://img.shields.io/badge/OpenAI-GPT--4-412991?style=for-the-badge&logo=openai&logoColor=white" />
          <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>p>

> A production-ready **conversational AI chatbot** built with Java 17, Spring Boot 3, and LangChain4j. Supports multi-turn conversations, memory management, and seamless OpenAI GPT-4 integration via a REST API.
>
> ---
>
> ## ✨ Features
>
> - 💬 **Multi-turn Conversations** — maintains context across messages using in-memory conversation history
> - - 🧠 **LangChain4j Integration** — leverages LangChain4j for LLM orchestration and prompt management
>   - - ⚡ **Spring Boot REST API** — clean, documented RESTful endpoints for chat interactions
>     - - 🔌 **OpenAI GPT-4 / GPT-3.5** — pluggable model support with easy configuration
>       - - 🛡️ **Rate Limiting** — built-in request throttling to manage API costs
>         - - 📝 **Conversation Logging** — persists chat history to PostgreSQL for analytics
>           - - 🐳 **Docker Ready** — containerized with Docker Compose for easy deployment
>            
>             - ---
>
> ## 🛠️ Tech Stack
>
> | Layer | Technology |
> |-------|------------|
> | Language | Java 17 |
> | Framework | Spring Boot 3.2 |
> | AI Orchestration | LangChain4j 0.27 |
> | LLM Provider | OpenAI (GPT-4 / GPT-3.5-turbo) |
> | Database | PostgreSQL 15 |
> | Build Tool | Maven 3.9 |
> | Containerization | Docker & Docker Compose |
> | API Docs | Swagger / OpenAPI 3 |
>
> ---
>
> ## 🚀 Getting Started
>
> ### Prerequisites
>
> - Java 17+
> - - Maven 3.9+
>   - - Docker & Docker Compose
>     - - OpenAI API Key
>      
>       - ### Installation
>      
>       - ```bash
>         # Clone the repository
>         git clone https://github.com/Pcveldi22/javaai-chatbot.git
>         cd javaai-chatbot
>
>         # Set your OpenAI API key
>         export OPENAI_API_KEY=your_api_key_here
>
>         # Run with Docker Compose
>         docker-compose up -d
>
>         # Or run locally with Maven
>         mvn spring-boot:run
>         ```
>
> ### API Usage
>
> ```bash
> # Start a conversation
> curl -X POST http://localhost:8080/api/chat \
>   -H "Content-Type: application/json" \
>   -d '{"sessionId": "user-123", "message": "Hello! What can you help me with?"}'
>
> # Response
> {
>   "sessionId": "user-123",
>   "response": "Hello! I can help you with a wide range of topics...",
>   "timestamp": "2026-07-02T10:30:00Z"
> }
> ```
>
> ---
>
> ## 📁 Project Structure
>
> ```
> javaai-chatbot/
> ├── src/main/java/com/chanduveldi/chatbot/
> │   ├── controller/          # REST API controllers
> │   │   └── ChatController.java
> │   ├── service/             # Business logic
> │   │   ├── ChatService.java
> │   │   └── ConversationMemoryService.java
> │   ├── config/              # LangChain4j & OpenAI config
> │   │   └── AIConfig.java
> │   ├── model/               # Request/Response DTOs
> │   └── repository/          # JPA repositories
> ├── src/main/resources/
> │   └── application.yml
> ├── docker-compose.yml
> └── pom.xml
> ```
>
> ---
>
> ## ⚙️ Configuration
>
> ```yaml
> # application.yml
> app:
>   openai:
>     api-key: ${OPENAI_API_KEY}
>     model: gpt-4
>     temperature: 0.7
>     max-tokens: 1024
>   chat:
>     max-history-size: 20
>     session-timeout-minutes: 30
> ```
>
> ---
>
> ## 🤝 Contributing
>
> Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) and submit pull requests.
>
> ## 📄 License
>
> This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
>
> ---
>
> <p align="center">Made with ❤️ by <a href="https://github.com/Pcveldi22">Pc Veldi</a>a></p>p>
