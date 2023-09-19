# Starter Spring Boot - Keycloak Implementation

## Configuration:
 - application.properties defines keycloak url, realm, and client for spring boot app
 - docker-compose provides credentials for keycloak admin console
 - SecurityConfig.java defines restricted endpoints and required roles
 - WebController.java defines endpoints and passes Principal as appropriate

## Instructions:
 - Clone and cd into directory (spring-keycloak)
 - mvn clean install # builds target jar for spring boot app
 - docker-compose up # pulls base images for app and keycloak containers

## Using:
 - open browser to localhost:8081 # should return "external"
 - open browser to localhost:8081/customers # should return server error
 - login to keycloak admin localhost:8080 with admin/admin
 - create realm "webby" and client "webby-app" 
 - create role "user"
 - create a user and assign the user the role "user"
 - refresh localhost:8081/customers # should present login page
 - login with user credentials # should return "customers"

 ## Dependencies
  - docker-ce
  - docker-compose
  - maven


TODO:
