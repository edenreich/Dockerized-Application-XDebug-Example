## Minimalistic Dockerized Application

### Quick Start

1. Place your application in `application` directory
2. Run `cp application/.env.dist application/.env`
3. In your IDE make sure you map `"/code/public": "${workspaceFolder}/application/public"` where $workspaceFolder variable is the root of the project.
4. Run `docker-compose up -d`

### Containers

- nginx:alpine (16.1MB)
- php:7.3.3-fpm-alpine3.8 (131MB)
- mysql:5.7.25 (372MB)