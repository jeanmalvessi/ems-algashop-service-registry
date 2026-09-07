# service-registry

Microservice responsible for service discovery in the [AlgaShop](https://github.com/jeanmalvessi/ems-algashop-meta) platform.

Built with **Netflix Eureka** server, allowing every other microservice to register itself and discover the location of its collaborators at runtime instead of relying on hardcoded hosts/ports.

## Responsibilities

- Service registration (`registerWithEureka`) for client microservices
- Service discovery, enabling client-side and gateway load balancing (`lb://` URIs)
- Instance health tracking through Eureka heartbeats

## Tech Stack

- **Java 25**, Spring Boot 4.0.7
- **Spring Cloud Netflix Eureka Server** (service registry)
- **Spring Boot Actuator** (monitoring and health checks)

## Running

```bash
./gradlew bootRun
```

Default port: **8761** (development profile)

Dashboard: `http://localhost:8761`
