# 🐳 Project Docker Environment

Welcome to the brains of the operation — the `docker/` repo! This is your one-stop shop to spin up the entire dev environment using Docker Compose. Whether you're hacking on `gateway`, tweaking `sensor-sim`, or running full system tests — you're in the right place.

---

## 📁 Project Structure

Here’s how the repos should be structured locally:
```
root/
 │ 
 ├── docker/ -- This repo!
 │      ├── docker-compose.yml 
 │      └── log4j.properties
 │ 
 ├── sensor-sim/
 │      ├── .env 
 │      └── Dockerfile 
 │      
 ├── pathfinding/ 
 │      ├── .env 
 │      └── Dockerfile 
 │ 
 └── gateway/
        ├── .env 
        └── Dockerfile
```

Each service has its own Dockerfile. The `docker-compose.yml` in the `docker/` folder manages and connects all services.

---

## Requirements

- Docker
- Docker Compose v2+
- Git (to make sure you're on the correct branch)

---

## Getting Started

1. **Ensure you have above project structure**:
Please check that all repos are up to date (at least dev or newer)

2. **Starting the system**:
from docker dir, run below command to start containers
```bash
docker compose up --build
```
To stop and remove containers run below command:
```bash
docker compose down -v
```
To clean up unused resources, run below command:
```bash
docker system prune -a --volumes
```
