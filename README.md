# 🚀 High-Performance Distributed URL Shortener

![Java](https://img.shields.io/badge/Java-17-orange) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.0-green) ![Redis](https://img.shields.io/badge/Redis-Cache-red) ![MySQL](https://img.shields.io/badge/MySQL-DB-blue) ![Docker](https://img.shields.io/badge/Docker-Enabled-blue)

A scalable, industrial-level URL shortening service (similar to TinyURL) designed to handle high concurrency. Built with a focus on distributed system principles, preventing cache stampede, and ensuring data consistency.

## ✨ Key Features

- **High Performance**: Utilizes **Redis** (Cache Aside pattern) to reduce database load and ensure low-latency reads.
- **Distributed ID Generation**: Implements Twitter's **Snowflake Algorithm** to generate globally unique, time-ordered 64-bit IDs without database locks.
- **Data Persistence**: Uses **MySQL** for reliable long-term storage of URL mappings.
- **Shortening Algorithm**: Custom **Base62 encoding** converts numeric IDs into compact, user-friendly short codes (e.g., `jWaBPznd1S`).
- **Containerization**: Fully Dockerized environment (Application + Redis + MySQL) using `docker-compose` for one-click deployment.
- **API Documentation**: Integrated **Swagger UI** for interactive API testing and documentation.

## 🛠 Tech Stack

- **Backend**: Java 17, Spring Boot 3
- **Database**: MySQL 8.0 (Persistent Storage)
- **Cache**: Redis 7.0 (High-speed caching)
- **DevOps**: Docker & Docker Compose
- **Tools**: Lombok, Spring Data JPA, OpenAPI (Swagger)

## 🚀 How to Run

### Prerequisites
- Docker & Docker Compose installed

### Quick Start

1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/tiny-url.git](https://github.com/jjs7233/tiny-url.git)
   
