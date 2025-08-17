# Keycloak Docker Compose Project

This project provides a simple way to run [Keycloak](https://www.keycloak.org/) using Docker Compose.

## Getting Started

1. **Clone the repository**  
   ```
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```

2. **Configure environment variables**  
   Create a `.env` file in the project root with the necessary Keycloak environment variables.  
   Example:
   ```
   KEYCLOAK_ADMIN=admin
   KEYCLOAK_ADMIN_PASSWORD=admin
   ```

3. **Start Keycloak**  
   ```
   docker-compose up
   ```

   Keycloak will be available at [http://localhost:8080](http://localhost:8080).

4. **Data Persistence**  
   The Keycloak data is persisted in a Docker volume named `keycloak_data`.

## Docker Compose Reference

The `docker-compose.yml` uses the official Keycloak image (`quay.io/keycloak/keycloak:26.3.2`) and starts Keycloak in development mode.

## Stopping and Removing Containers

To stop the service:
