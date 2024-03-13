# Two-Tier Application Containerization with Docker

## Project Overview

This is a simple Flask web application built using Docker and Docker Compose. It interacts with a MySQL database to allow users to submit messages. Messages are stored in the database and displayed on the frontend.

## Prerequisites

Before you begin, make sure you have the following installed:

- Docker
- Git (optional, for cloning the repository)

## Setup

1. Clone this repository:
```bash
git clone https://github.com/kevalhingu/two-tier-flask-to-do.git
```
2. Navigate to the project directory:
```bash
cd two-tier-flask-to-do
```
3. Start the containers using Docker Compose:
```bash
docker-compose up --build
```

4. Access the Flask app in your web browser:

- Frontend: [http://localhost](http://localhost)
- Backend: [http://localhost:5000](http://localhost:5000)

5. Create the messages table in your MySQL database:

Use a MySQL client or tool (e.g., phpMyAdmin) to execute the following SQL commands:

```sql
CREATE TABLE messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    message TEXT
);
```

## Cleaning Up

To stop and remove the Docker containers, press Ctrl+C in the terminal where the containers are running, or use the following command:

```bash
docker-compose down
```

## Docker Image

The Docker image for this Flask app is available on Docker Hub at: [kevalhingu/flaskapp](https://hub.docker.com/repository/docker/kevalhingu/flaskapp/general)

## About Docker and Docker Compose

### Docker

Docker is a platform that enables developers to build, package, and deploy applications in lightweight, portable containers. Containers encapsulate everything needed to run an application, including libraries, dependencies, and configuration files. Docker provides a consistent environment for developing and running applications across different systems.

### Docker Compose

Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to define your application's services, networks, and volumes in a single YAML file, making it easy to manage complex setups. With Docker Compose, you can start, stop, and scale your application with a single command, simplifying the development and deployment process.
