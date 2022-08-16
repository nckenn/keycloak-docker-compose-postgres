# Keycloak Docker setup with PostgreSQL

A Keycloak setup for development and production.

## Guide

### Download and build the latest versions of the images
```docker-compose build --pull --no-cache```

## Start Docker Compose in detached mode:

### Development
```docker compose up -d```

### Production
```docker compose -f docker-compose.yml -f docker-compose.prod.yml --env-file .env.prod up -d```
