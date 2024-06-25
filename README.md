## What is Spring Actuators? 
Spring Actuator is a set of production-ready features in Spring Boot that provides endpoints for monitoring and managing your application's health, metrics, and other operational aspects.

### Key Features and Usage
#### key features:

#### Health Checks: 
Actuator endpoints give you application health information, such as whether it's operating normally or having problems. For systems that monitor and alert users, this is crucial.

#### Metrics: 
Actuators gather and display a range of application metrics, including memory consumption, request counts, and thread pool utilization. These metrics aid in comprehending your application's behavior and performance.

#### Endpoints: 
Actuators expose several management endpoints (e.g., /actuator/health, /actuator/metrics) that provide insights into different aspects of your application. These endpoints can be customized and secured based on your requirements.

### Getting Started
To add Spring Actuators to your Spring Boot project:

#### 1. Dependency: 
Include the Actuator dependency in your pom.xml or build.gradle file:

MAVEN:
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
GRADLE:
```
implementation 'org.springframework.boot:spring-boot-starter-actuator'
```
#### 2. Configuration: 
Configure Actuator endpoints in your application.properties or application.yml file. 
For example, to expose all endpoints except env and beans, and enable shutdown:
```
management.endpoints.web.exposure.include=*
management.endpoints.web.exposure.exclude=env,beans
management.endpoint.shutdown.enabled=true
```

#### 3. How to Use:
Once configured, you can access Actuator endpoints to monitor your application's health, metrics, and other management information. For example, using Postman or any HTTP client, you can check the health of your application by accessing /actuator/health.

### About Project:
In the above Simple Maven Project It is just for understanding the concept of Spring Actuators, Hence I have only developed one controller GreetingController and added the service layer logic in the controller itself.
(We should never do this but it is just for understanding purpose, always develop project in the Layered Structure). 

It's a simple logic in which the controller will greet the user according to the Local time of the users system.

Use POSTMAN tool to inspect the output and endpoints for monitoring and managing your application's health, metrics, and other operational aspects.


