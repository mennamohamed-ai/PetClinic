# 🐾 Pet Clinic Management System

A robust, enterprise-grade **Microservices-based** application for managing pet clinic operations. This project implements advanced software engineering principles, including distributed systems architecture, predictive analytics, and secure authentication.

---

## 🏗️ System Architecture

The system is built on a **Cloud-Native Microservices** architecture using **Spring Cloud**, ensuring high scalability and fault tolerance.

- **API Gateway (8080):** Centralized entry point using Spring Cloud Gateway for routing and load balancing.
- **Eureka Server (8761):** Service Registry for dynamic service discovery.
- **Main Service (9090):** Handles core business logic (Owners, Pets, Appointments, Billing).
- **ML Service (8000):** A Python-based service for predictive analytics (e.g., appointment attendance).
- **MySQL Database:** Relational data persistence with separate schemas for services.



---

## 🚀 Key Technical Features (The 7 Pillars)

### 1. RESTful API Implementation
Exposes a clean REST interface with proper HTTP methods (`GET`, `POST`, `PUT`, `DELETE`) and standard status codes.

### 2. OCL & Data Constraints
Strict data integrity is enforced using **Jakarta Validation (JSR 380)**. 
- Example: `@PastOrPresent` for birth dates, `@Positive` for fees, and complex regex for password strength.

### 3. Aspect-Oriented Programming (AOP)
Utilizes **Spring AOP** for cross-cutting concerns.
- **LoggingAspect:** Automatically logs method execution and exceptions across the service layer without cluttering business logic.

### 4. Docker & Orchestration
Full containerization using **Docker** and **Docker Compose**.
- Multi-stage builds for optimized images.
- Automated service orchestration with health checks.

### 5. Clean Code & SOLID Principles
Follows **Clean Code** practices:
- **SRP:** Each service and class has one responsibility.
- **Dependency Injection:** Extensive use of Constructor Injection for testability.

### 6. Design Patterns
Implemented industry-standard patterns:
- **Repository Pattern:** For clean data access abstraction.
- **Guard Pattern:** Centralized security logic (`AuthGuard`, `RoleGuard`).
- **Builder Pattern:** Fluent object creation for Entities.
- **Strategy Pattern:** For dynamic role-based permissions.

### 7. Microservices & Cloud-Native
- **Service Discovery:** Netflix Eureka.
- **Load Balancing:** Client-side load balancing via API Gateway.
- **Centralized Configuration:** Managed through environment variables.

---

## 🔐 Security & Authentication

- **Stateless JWT Authentication:** Secure token-based access.
- **HttpOnly Cookies:** Protection against XSS attacks.
- **RBAC (Role-Based Access Control):** Granular permissions for `ADMIN`, `VET`, `RECEPTIONIST`, and `PET_OWNER`.

---

## 🛠️ Tech Stack

- **Backend:** Java 21, Spring Boot 3.x, Spring Security, Spring Data JPA.
- **Microservices:** Spring Cloud Gateway, Netflix Eureka.
- **Frontend:** React.js, Tailwind CSS.
- **Database:** MySQL 8.4.
- **DevOps:** Docker, Docker Compose.
- **ML Layer:** Python, Flask/FastAPI.

---

## 🔧 Getting Started

### Prerequisites
- Docker & Docker Compose
- Java 21 (optional for local build)

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/pet-clinic-microservices.git](https://github.com/mennamohamed-ai/PetClinic)


2. Navigate to the project root and run:
```bash
docker-compose up --build

```


3. Access the services:
* Frontend: `http://localhost:5173`
* API Gateway: `http://localhost:8080`
* Eureka Dashboard: `http://localhost:8761`

---


