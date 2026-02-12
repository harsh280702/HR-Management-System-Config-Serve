 HR Management System - Config Server

Welcome to the **HR Management System - Config Server**, a centralized configuration service designed to manage application properties across microservices in a scalable and maintainable way.

## Overview

This repository hosts the configuration server for the HR Management System. It leverages Spring Cloud Config to provide externalized configuration for various services in the HR ecosystem. By centralizing configuration, we ensure consistency, ease of management, and seamless updates across environments (development, staging, production).

## Features

- **Centralized Configuration**: Store all application properties in a single, version-controlled location.
- **Environment-Specific Profiles**: Support for multiple environments using Spring profiles.
- **Git Integration**: Configuration files are stored in Git, enabling version control and audit tracking.
- **Secure Access**: Configurations are protected and accessible only through secure channels.
- **Dynamic Updates**: Support for configuration refreshes without service restarts.

## Repository Structure
/hr-management-config-server │ ├── src/ │ └── main/ │ └── java/ │ └── com/ │ └── hr/ │ └── config/ │ └── ConfigServerApplication.java │ ├── src/ │ └── main/ │ └── resources/ │ └── application.yml │ ├── application.yml └── README.md


## Getting Started

### Prerequisites

- Java 11 or higher
- Maven or Gradle
- Git
- Spring Cloud Config Server

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/harsh280702/HR-Management-System-Config-Serve.git
Navigate to the project directory:

bash

Copy
cd HR-Management-System-Config-Serve
Build the project:

bash

Copy
mvn clean install
Run the Config Server:

bash

Copy
mvn spring-boot:run
Access the configuration endpoint:

The server will be available at http://localhost:8081.
You can access configurations using the endpoint: /{application}/{profile}/{label}.
Configuration
All configurations are stored in the config folder within the repository. You can add or modify configuration files as needed:

application.yml: Default application settings.
application-{profile}.yml: Environment-specific configurations.
Example:

yaml

Copy
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/hr_db
    username: root
    password: password
Environment Variables
Set the following environment variables for deployment:

SPRING_PROFILES_ACTIVE: Set to dev, staging, or prod based on the environment.
GIT_REPOSITORY_URL: URL of the Git repository containing configurations.
GIT_USERNAME and GIT_PASSWORD: Credentials for accessing the Git repository.
Contributing
We welcome contributions! Please follow these steps:

Fork the repository.
Create a new branch for your feature or bug fix.
Make your changes and ensure tests pass.
Submit a pull request with a detailed description of your changes.
Support
For any issues or questions, please open an issue in the repository or contact the maintainers.

License: MIT
Author: Harsh (harsh280702)
Contact: harshrajput5629@gmail.com
