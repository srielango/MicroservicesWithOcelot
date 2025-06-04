# 🧩 Microservices with Ocelot - .NET Sample Project

A **learning and demo repository** demonstrating microservices architecture using ASP.NET Core, Ocelot API Gateway, gRPC, RabbitMQ, Redis, PostgreSQL, and SQL Server — designed for modular, scalable backend systems like an **e-commerce platform**.

> ✅ Target Audience: Recruiters & Clients  
> 🧪 Purpose: Showcase clean architecture, distributed system design, and .NET proficiency

---

## 🏗️ Architecture Overview

This solution is based on **domain-driven design principles** with each microservice responsible for a single business capability. The key architectural elements include:

- 🔀 **Ocelot API Gateway** for routing and request aggregation
- 🧾 **Ordering Service**: Implements Clean Architecture with SQL Server
- 🛒 **Basket Service**: Caches data using Redis
- 📦 **Catalog Service**: Uses PostgreSQL as backend
- 💸 **Discount Service**: Exposes functionality via gRPC
- 📬 **RabbitMQ** for asynchronous messaging between services


---

## 🚀 Getting Started

You can run the solution either using Docker (preferred) or manually using the .NET CLI/Visual Studio.

### 🐳 Option 1: Docker Compose (Recommended)

Make sure Docker and Docker Compose are installed.

```bash
git clone https://github.com/srielango/MicroservicesWithOcelot.git
cd MicroservicesWithOcelot
docker-compose up --build
```

This will spin up:

All microservices (Catalog, Basket, Discount, Ordering)

API Gateway

PostgreSQL, Redis, SQL Server

RabbitMQ

### 🧰 Option 2: Manual Setup (Using .NET CLI)
Clone the repo

Open the solution in Visual Studio or VS Code

Ensure PostgreSQL, Redis, RabbitMQ, and SQL Server are running

Set multiple startup projects (API Gateway, Services) in your IDE

Build and run each project individually

🔧 Technologies Used
- API Gateway	Ocelot
- Microservices	ASP.NET Core 7.0
- Inter-service Comm	HTTP, gRPC (for Discount Service)
- Messaging	RabbitMQ
- Caching	Redis
- Databases	PostgreSQL (Catalog), SQL Server (Ordering)
- Containerization	Docker, Docker Compose

🧼 Clean Architecture
- The Ordering Service is structured using Clean Architecture principles:

- Domain layer for business logic

- Application layer for use cases

- Infrastructure layer for database access

- API layer as the entry point

This structure improves testability, maintainability, and separation of concerns.
