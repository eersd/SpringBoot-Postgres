# SpringBoot-Postgres
SpringBoot Postgres CRUD

## Docker

Spin up postgres container in docker (default postgres port 5432, postgres:alpine = lightweight-docker-image)

    docker run --name postgres-SpringBoot -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:alpine
    
Find docker container id

    docker ps -a

Run bash in docker container (the id here obtained from line above)

    docker exec -it 1a4e25bd0446 bin/bash
    
Inside docker container, run postgres as user postgres

    psql -U postgres

Then can run sql queries

## Spring Boot

- API-Layer (Controller)
- Model
- DAO
- DAO Implementation
- Service

Set environment variables and configuration in application.properties

    spring.datasource.url=jdbc:postgresql://localhost:5432/demodb
    spring.datasource.username=postgres
    spring.datasource.password=password
