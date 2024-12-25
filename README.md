# .NET Microservices Architecture with Kubernetes

## Project Overview
This project demonstrates a microservices architecture built with .NET 8, implementing synchronous and asynchronous communication patterns, deployed on Kubernetes with RabbitMQ message broker.

### Architecture Components
- **Platform Service**: Manages platform data
- **Command Service**: Handles command operations
- **RabbitMQ**: Message broker for async communication
- **SQL Server**: Database for Platform Service
- **Kubernetes**: Container orchestration

## Technology Stack
- .NET 8
- Entity Framework Core
- gRPC
- RabbitMQ
- SQL Server
- Kubernetes
- Docker
- NGINX Ingress Controller

## Communication Patterns
### Synchronous
- REST APIs between services
- gRPC for efficient inter-service communication

### Asynchronous
- RabbitMQ message broker for event-driven communication
- Publisher/Subscriber pattern

## Kubernetes Setup

### Core Services
1. **Platform Service**
   - Main API service
   - Exposes HTTP and gRPC endpoints
   - Ports: 8080 (HTTP), 666 (gRPC)

2. **Command Service**
   - Secondary API service
   - Consumes Platform Service data
   - Port: 8080

### Infrastructure Services

3. **SQL Server**
   - Persistent storage for Platform Service
   - Uses PersistentVolumeClaim
   - Port: 1433

4. **RabbitMQ**
   - Message broker
   - Management UI Port: 15672
   - Message Port: 5672

### Kubernetes Components
- Deployments
- Services (ClusterIP, LoadBalancer, NodePort)
- Persistent Volume Claims
- Ingress Configuration
- Secrets Management

## API Endpoints
- Platform Service: `http://acme.com/api/platforms`
- Command Service: `http://acme.com/api/c/platforms`

## Development Setup

### Prerequisites
- Docker Desktop
- Kubernetes enabled
- .NET 8 SDK
- SQL Server
- RabbitMQ

## Features
- ✅ Microservices Architecture
- ✅ Multi-Database Support
- ✅ Message Queue Integration
- ✅ Synchronous & Asynchronous Communication
- ✅ Container Orchestration
- ✅ Service Discovery
- ✅ Load Balancing
- ✅ API Gateway Pattern

### Local Development
1. Clone the repository
2. Apply Kubernetes configurations
3. Configure the environment variables
4. Run the services


