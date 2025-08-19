# Keycloak Docker Compose Project

This project provides an easy way to run [Keycloak](https://www.keycloak.org/) using Docker Compose.

## Getting Started

1. **Clone the repository**
   ```sh
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```

2. **Set up environment variables**
   
   Create a `.env` file in the project root directory and define the required Keycloak and database environment variables.  
   Example:
   ```
   KEYCLOAK_ADMIN=admin
   KEYCLOAK_ADMIN_PASSWORD=admin
   KC_DB=postgres
   KC_DB_HOST=localhost
   KC_DB_PORT=5432
   KC_DB_NAME=keycloak
   KC_DB_USERNAME=keycloak
   KC_DB_PASSWORD=keycloak
   KC_HOSTNAME=localhost
   KC_HOSTNAME_PORT=8080
   KC_HEALTH_ENABLED=true
   KC_HTTP_ENABLED=true
   KC_HOSTNAME_STRICT_HTTPS=false
   KC_HOSTNAME_STRICT_BACKCHANNEL=false
   ```

   > **Note:** Adjust these values as needed for your environment and database setup.

3. **Start Keycloak**
   ```sh
   docker-compose up
   ```

   Keycloak will be accessible at [http://localhost:8080](http://localhost:8080).

4. **Data Persistence**
   
   Keycloak data is stored in a Docker volume named `keycloak_data`, ensuring your data persists across container restarts.

## Docker Compose Reference

The `docker-compose.yml` file uses the official Keycloak image (`quay.io/keycloak/keycloak:26.3.2`) and starts Keycloak with environment variables defined in your `.env` file.

## Stopping and Removing Containers

To stop the Keycloak service and remove containers, run:
