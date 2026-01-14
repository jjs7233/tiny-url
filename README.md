# 🚀 High-Performance Distributed URL Shortener

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.0-green)
![Redis](https://img.shields.io/badge/Redis-Cache-red)
![MySQL](https://img.shields.io/badge/MySQL-DB-blue)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue)

A scalable, industrial-level URL shortening service (similar to TinyURL) designed to handle high concurrency. Built with a focus on distributed system principles, preventing cache stampede, and ensuring data consistency.

## ✨ Key Features

- **High Performance**: Utilizes **Redis** (Cache Aside pattern) to reduce database load and ensure low-latency reads.
- **Distributed ID Generation**: Implements Twitter's **Snowflake Algorithm** to generate globally unique, time-ordered 64-bit IDs without database locks.
- **Data Persistence**: Uses **MySQL** for reliable long-term storage of URL mappings.
- **Shortening Algorithm**: Custom **Base62 encoding** converts numeric IDs into compact, user-friendly short codes (e.g., `jWaBPznd1S`).
- **Containerization**: Fully Dockerized environment (Application + Redis + MySQL) using `docker-compose` for one-click deployment.
- **API Documentation**: Integrated **Swagger UI** for interactive API testing and documentation.

## 🛠 Tech Stack

- **Backend**: Java 17, Spring Boot 3 (RESTful API)
- **Database**: MySQL 8.0 (Docker volume persistence)
- **Cache**: Redis 7.0 (URL mapping cache)
- **DevOps**: Docker, Docker Compose (multi-container orchestration)
- **Persistence**: Spring Data JPA (MySQL)
- **API Docs**: OpenAPI 3 (Swagger UI)

## 🚀 How to Run

### Prerequisites
- Docker & Docker Compose installed

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/jjs7233/tiny-url.git
   cd tiny-url
2. **Start the application**
   Run the following command to build and start all services (App, MySQL, Redis):
   ```bash
   docker-compose up -d --build
   #or
   docker compose up -d --build
3. **Access the Application**
   - **Service Base URL**: http://localhost:8080
   - **Swagger UI (API Documentation)**: http://localhost:8080/swagger-ui.html

## 🧪 API Usage Example

   ```bash
   curl -X POST http://localhost:8080/api/shorten \
     -H "Content-Type: application/json" \
     -d '{"originalUrl": "https://www.google.com"}'
   ```
   Response example:
   ```json
   {
  "shortUrl": "http://localhost:8080/abc123"
   }
   ```

   
