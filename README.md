



# Server Registry (Eureka Server)

## Overview

The Server Registry, implemented using Eureka Server, acts as a service registry and discovery server for microservices. It provides a centralized location for managing and monitoring service instances.

## Features

- **Service Registration**: Microservices register themselves with the Eureka Server upon startup.
- **Service Discovery**: Clients can discover available service instances from the Eureka Server.
- **Dashboard**: Eureka Server provides a web-based UI dashboard for monitoring registered services.
- **Load Balancing**: Integrates with Ribbon for client-side load balancing.
- **High Availability**: Supports clustering for redundancy and fault tolerance.

## Technologies Used

- **Spring Cloud Netflix Eureka**: For building the Eureka Server.
- **Java**: Programming language used for development.
- **Git**: Version control system for source code management.

## Setup

To run the Server Registry locally, ensure you have the following installed:

- Java Development Kit (JDK) 8 or higher
- Maven (for building and managing dependencies)

### Configuration

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd server-registry
   ```

2. Configure Eureka Server in `application.properties`:

   ```properties
   server.port=8761
   eureka.client.register-with-eureka=false
   eureka.client.fetch-registry=false
   ```

3. Start the application using Maven:

   ```bash
   mvn spring-boot:run
   ```

## Usage

### Dashboard

Access the Eureka Server dashboard at `http://localhost:8761` after starting the server. The dashboard displays information about registered microservices.

## Integration

Integrate microservices with Eureka Server by configuring them to register with the server upon startup. Example configuration in `bootstrap.properties`:

```properties
spring.application.name=your-microservice
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka/
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

