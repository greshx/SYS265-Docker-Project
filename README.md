# SYS265 Docker Compose Project  
**VM:** docker01-miller  
**IP Address:** 10.0.5.12  

## Overview
This project demonstrates a multi-container Docker setup using Docker Compose.

It includes:
- Postgres database container
- pgAdmin web interface container

The pgAdmin container connects to the Postgres container over Docker's internal network and allows database management through a web browser.

## Technologies Used
- Docker
- Docker Compose
- Postgres
- pgAdmin

## How to Run
From inside the project folder:

docker compose up -d

To verify containers:

docker ps

## Accessing pgAdmin
Open a browser and go to:

http://10.0.5.12:8080

Login:
Email: admin@admin.com  
Password: admin  

## Container Interaction
The pgAdmin container connects to the Postgres container using the service name "db" defined in docker-compose.yml.  
This demonstrates container networking and service dependency.

## Persistence
A Docker volume is used to store Postgres data so that it remains after containers are stopped and restarted.

## Stopping Containers
docker compose down
