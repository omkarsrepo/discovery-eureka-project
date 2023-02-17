# Eureka Discovery Service and Client services.

### Based On:
- Java 11
- Spring Boot
- Netflix Eureka

### Primary dependencies used:
- spring-boot-starter-parent
- spring-boot-starter-web
- spring-cloud-starter-netflix-eureka-client
- spring-cloud-starter-netflix-eureka-server

### Services:
- eureka server:
  - discovery-server
- eureka clients:
  - movie-catalog-service
  - movie-info-service
  - rating-service

### Key points:
- For eureka server:
  ```
  eureka.client.registerWithEureka = false
  eureka.client.fetchRegistry = false
  server.port = 8761
  ```
  ```
  @SpringBootApplication
  @EnableEurekaServer
  ```
- For eureka client:
  ```
  server.port = 8081
  eureka.client.serviceUrl.defaultZone  = http://localhost:8761/eureka
  spring.application.name = service-name
  ```
  
### Thank you for reading this!