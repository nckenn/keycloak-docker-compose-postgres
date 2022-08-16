
# Keycloak Docker setup with PostgreSQL
A Keycloak setup for development and production.

## Guide

### Download and build the latest versions of the images
```docker-compose build --pull --no-cache```

## Start Docker Compose in detached mode:

### For Development
```docker compose up -d```

### For Production
Create a .env.prod file and paste the code below :
```
SERVER_NAME=example.com
POSTGRES_DB=keycloak
POSTGRES_USER=keycloak
POSTGRES_PASSWORD=keycloak
```
Then run :
```docker compose -f docker-compose.yml -f docker-compose.prod.yml --env-file .env.prod up -d```
