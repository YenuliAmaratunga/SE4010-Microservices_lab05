# SE4010-Microservices_lab05

This project implements a Polyglot Microservices architecture using Spring Cloud Gateway and three backend services, all containerized with Docker.

## 🏗️ Architecture
- **API Gateway**: Entry point (Port 9090). Routes traffic based on path predicates.
- **Item Service**: Manages product inventory (Port 8081).
- **Order Service**: Handles customer orders (Port 8082).
- **Payment Service**: Processes transactions (Port 8083).

## 🚀 How to Run
1. Ensure **Docker Desktop** is running.
2. Build the JAR files using Maven:
   `mvn clean package -DskipTests`
3. Deploy the containers:
   `docker-compose up --build -d`

## 🛠️ Testing
- **Get Items**: `GET http://localhost:9090/items`
- **Place Order**: `POST http://localhost:9090/orders`
- **Process Payment**: `POST http://localhost:9090/payments/process`
