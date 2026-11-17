# TaskFlow – DevOps Deployment Project

A full-stack task management application containerized with Docker and Docker Compose, with a focus on DevOps practices, automation, and AWS deployment.

## Project Overview

TaskFlow is a task management application built using the MERN stack.

This project demonstrates how to containerize a full-stack application and prepare it for automated CI/CD deployment.

## Technology Stack

- **Frontend:** React, Vite, Nginx
- **Backend:** Node.js, Express
- **Database:** MongoDB
- **Containerization:** Docker, Docker Compose
- **Version Control:** Git, GitHub
- **Cloud:** AWS (deployment planned)
- **CI/CD:** GitHub Actions (planned)

## Architecture

The application uses three Docker containers:

1. **Frontend:** React application served through Nginx.
2. **Backend:** Node.js and Express REST API.
3. **Database:** MongoDB for persistent data storage.

Nginx forwards API requests to the backend, while the backend connects to MongoDB through the Docker network.

## Project Structure

```text
taskflow/
├── client/
│   ├── Dockerfile
│   ├── nginx.conf
│   └── .dockerignore
├── server/
│   ├── Dockerfile
│   └── .dockerignore
├── docker-compose.yml
├── README.md
└── .gitignore
```

## Docker Implementation

### Backend Image

```bash
docker build -t taskflow-backend:latest ./server
```

### Frontend Image

```bash
docker build -t taskflow-frontend:latest ./client
```

### Start All Containers

```bash
docker compose up -d
```

### Check Container Status

```bash
docker compose ps
```

### View Logs

```bash
docker compose logs
```

### Stop Containers

```bash
docker compose down
```

## Security

- Environment variables are used for sensitive configuration.
- `.env` files are excluded from Git using `.gitignore`.
- Docker images use production dependencies for the backend.
- MongoDB data is stored in a Docker volume.

## Current Progress

- [x] Application repository cloned
- [x] Backend Dockerfile created
- [x] Frontend Dockerfile created
- [x] Nginx reverse proxy configured
- [x] Docker Compose configured
- [x] MongoDB container configured
- [x] Docker images built successfully
- [x] All containers started successfully
- [x] Backend database connection verified
- [x] API health endpoint verified
- [x] Project pushed to GitHub portfolio repository
- [ ] GitHub Actions CI/CD pipeline
- [ ] AWS infrastructure deployment
- [ ] Monitoring and logging

## Author

DevOps Portfolio Project

GitHub: [suhailarshid29-ops](https://github.com/suhailarshid29-ops)